# Tesi
Dinamiche vegetazionali sul fiume Tagliamento

Questo repository contiene i file necessari alla compilazione con Latex
della tesi di laurea magistrale in Ingegneria per l'Ambiente e il Territorio
di Robin Castellani.
Vi sono cartelle che comprendono dati, grafici, immagini, licenza e altro.

Per compilare correttamente tutto il lavoro occorre eseguire i seguenti comandi:
- `lualatex -shell-escape -synctex=1 -interaction=nonstopmode 00-main.tex` per compilare tutti i grafici, anche quelli con una grande quantità di punti, ed esternalizzarli in file `.PDF` che saranno utilizzati nelle compilazioni successive; viene inoltre creato il file `00-main-frn.tex` del frontespizio;
- `xelatex -synctex=1 -interaction=nonstopmode 00-main-frn.tex` per creare il file `.PDF` del frontespizio con i caratteri di UNITN (occorre aver installato la famiglia di font **Quadrat Serial Regular**);
- `makeglossaries 00-main.ist` per creare il glossario
- `biber 00-main` per compilare la bibliografia
- `pdflatex -shell-escape -synctex=1 -interaction=nonstopmode 00-main.tex` due volte per sistemare i riferimenti

Il lavoro è distribuito sotto la licenza **Creative Commons 4.0** con limitazioni
di Attribuzione, Non Commerciale e Condividi allo Stesso Modo 
(vedi il file LICENSE.md).
