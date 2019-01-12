# Tesi
##Dinamiche della vegetazione riparia sul fiume Tagliamento: traiettorie evolutive e relazioni piene - vegetazione

Questo repository contiene i file necessari alla compilazione con LaTeX della tesi di laurea magistrale in Ingegneria per l'Ambiente e il Territorio di Robin Castellani.
Questa tesi può essere composta in accordo con gli standard di archiviabilità PDF/A: tabella di colori standard RGB, nessun collegamento ipertestuale a fonti esterne e font, metadati e licenza inclusi nel documento. Il report di [`veraPDF`](verapdf.org), applicativo *opensource* per validare la compatibilità di file `.PDF` con lo standard PDF/A, è presente tra i file del progetto.

Per compilare correttamente tutto il lavoro occorre eseguire i seguenti comandi:
- `lualatex -shell-escape -synctex=1 -interaction=nonstopmode 00-main.tex` per compilare tutti i grafici, anche quelli con una grande quantità di punti, ed esternalizzarli in file `.PDF` che saranno utilizzati nelle compilazioni
successive; viene inoltre creato il file `00-main-frn.tex` del frontespizio; se si desidera comporre un file compatibile con gli standard PDF/A, occorre commentare con `%` la terza riga, dove è presente `\usepackage[a-1b]{pdfx}`;
- `xelatex -synctex=1 -interaction=nonstopmode 00-main-frn.tex` per creare il file `.PDF` del frontespizio con i caratteri di UNITN (occorre aver installato la famiglia di font **Quadrat Serial Regular**);
- `makeglossaries 00-main` per creare il glossario;
- `biber 00-main` per compilare la bibliografia;
- `pdflatex -shell-escape -synctex=1 -interaction=nonstopmode 00-main.tex` due volte per sistemare i riferimenti.

Alternativamente, se non si desidera la compatibilità con gli standard di PDF/A si può usare Arara 4.0 tramite il comando
`arara -p arara_commands 00-main.tex`, il quale esegue quanto descritto sopra automaticamente (il primo comando, tuttavia, è `pdflatex`).

È stata utilizzata la distribuzione [TeX Live](http://http://tug.org/texlive) version 2017.

Il lavoro è distribuito sotto la licenza **Creative Commons 4.0** con limitazioni di Attribuzione, Non Commerciale e Condividi allo Stesso Modo (vedi il file LICENSE.md).
