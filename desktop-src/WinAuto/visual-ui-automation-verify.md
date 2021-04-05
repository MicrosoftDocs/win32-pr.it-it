---
title: Verifica automazione interfaccia utente visiva
description: Verifica di automazione interfaccia utente visuale (Visual UIA Verify) è una finestra \ 32; Driver GUI per la libreria di test di UIA progettata per il test manuale dell'automazione dell'interfaccia utente.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e224a52d243427af86c6cd27a3add3be03d9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713771"
---
# <a name="visual-ui-automation-verify"></a>Verifica automazione interfaccia utente visiva

Visual UI Automation Verify (Visual UIA Verify) è un driver GUI Windows per la libreria di test di UIA progettata per il test manuale dell'automazione dell'interfaccia utente. Fornisce un'interfaccia per la funzionalità della libreria di test UIA che elimina l'overhead di codifica di uno strumento da riga di comando.

-   [Comandi di menu](#menu-commands)
-   [Riquadri funzionali](#functional-panes)
    -   [Riquadro dell'albero elementi di automazione](#automation-elements-tree-pane)
    -   [Riquadro test](#tests-pane)
    -   [Riquadro Risultati test](#test-results-pane)
    -   [Riquadro proprietà](#properties-pane)

Visual UIA Verify supporta solo il logger di verifica di UIA (WUIALoggerXml.dll) in modo nativo. Le trasformazioni XML selezionabili dall'utente sono incorporate in Visual UIA Verify per presentare diverse visualizzazioni del report del logger XML nel riquadro **risultati test** .

Per impostazione predefinita, Visual UIA Verify carica il provider del lato client di automazione interfaccia utente fornito con la versione originale di automazione interfaccia utente. È possibile scegliere di non caricare il provider aggiungendo **/NOCLIENTSIDEPROVIDER** nell'opzione della riga di comando di VisualUIVerifyNative.exe.

Lo screenshot seguente mostra le principali aree funzionali dell'interfaccia utente di verifica di Visual UIA.

![principali aree funzionali dell'interfaccia utente di verifica di Visual UIA](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a>Comandi di menu

Nella tabella seguente vengono descritti i comandi del menu di verifica di visuali.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Menu</th>
<th>Comando</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>File</strong></td>
<td><strong>Esci</strong></td>
<td>Uscire da Visual UIA Verify.</td>
</tr>
<tr class="even">
<td><strong>Visualizzazione</strong></td>
<td><strong>Evidenziazione</strong></td>
<td>Evidenziare il rettangolo delimitatore dell'elemento selezionato nel riquadro <strong>dell'albero degli elementi di automazione</strong> . Sono disponibili le seguenti opzioni.
<ul>
<li><strong>Rettangolo</strong>: linea rossa continua.</li>
<li><strong>Rettangolo di dissolvenza</strong>: una linea rossa continua che scompare dopo pochi secondi.</li>
<li><strong>Rays e rettangolo</strong>, una linea rossa continua con linee di evidenziazione blu aggiuntive che si irradiano da ogni angolo del rettangolo di delimitazione.</li>
<li><strong>None</strong>: Nessuna evidenziazione visibile.</li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><strong>Albero degli elementi di automazione</strong>$ {Remove} $<br />
</td>
<td><strong>Aggiorna elemento selezionato</strong></td>
<td>Aggiornare gli elementi figlio dell'elemento selezionato nel riquadro <strong>dell'albero degli elementi di automazione</strong> . L'elenco di elementi è statico e non viene aggiornato dinamicamente (automaticamente) se l'albero degli elementi viene modificato.</td>
</tr>
<tr class="even">
<td><strong>Spostamento</strong></td>
<td>Spostarsi nella gerarchia della struttura ad albero degli elementi in uno dei seguenti elementi.
<ul>
<li><strong>Parent</strong>: passa all'elemento padre.</li>
<li><strong>Primo elemento figlio</strong>— passa al primo elemento figlio.</li>
<li><strong>Fratello di pari livello successivo</strong>-Vai al primo elemento di pari livello.</li>
<li><strong>Precedente elemento di pari livello</strong>-passa a elemento di pari livello precedente.</li>
<li><strong>Ultimo elemento figlio</strong>: passa all'ultimo elemento figlio.</li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><strong>Modalità</strong>$ {Remove} $<br />
</td>
<td><strong>Always On Top</strong></td>
<td>La finestra di verifica di visuale UIA rimane nella parte superiore dell'ordine z del desktop.</td>
</tr>
<tr class="even">
<td><strong>Modalità hover (usare Ctrl)</strong></td>
<td>Quando si preme il tasto CTRL, l'elemento sotto il cursore del mouse viene identificato come elemento di interesse. Il riquadro dell' <strong>albero degli elementi di automazione</strong> viene aggiornato e viene evidenziato l'elemento corrispondente nell'elenco di elementi.</td>

</tr>
<tr class="odd">
<td><strong>Rilevamento dello stato attivo</strong></td>
<td>Quando viene modificato lo stato attivo, l'elemento con lo stato attivo viene identificato come elemento di interesse. Il riquadro dell' <strong>albero degli elementi di automazione</strong> viene aggiornato e viene evidenziato l'elemento corrispondente nell'elenco di elementi.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Test</strong>$ {Remove} $<br />
</td>
<td><strong>Vai a sinistra</strong></td>
<td>Spostare un nodo a sinistra nell'albero dei <strong>test</strong> .</td>
</tr>
<tr class="odd">
<td><strong>Vai su</strong></td>
<td>Spostare un nodo verso l'alto nell'albero dei <strong>test</strong> .</td>

</tr>
<tr class="even">
<td><strong>Vai giù</strong></td>
<td>Spostare un nodo verso il basso nell'albero dei <strong>test</strong> .</td>

</tr>
<tr class="odd">
<td><strong>Vai a destra</strong></td>
<td>Spostare un nodo direttamente nell'albero dei <strong>test</strong> .</td>

</tr>
<tr class="even">
<td><strong>Esegui i test selezionati sull'elemento selezionato</strong></td>
<td>Esegue i test selezionati dall'albero dei <strong>test</strong> nell'elemento selezionato.</td>

</tr>
<tr class="odd">
<td><strong>Filtra problemi noti</strong></td>
<td>Filtrare i bug noti di automazione interfaccia utente dai risultati del test.</td>

</tr>
<tr class="even">
<td><strong>?</strong></td>
<td><strong>Informazioni sulle verifiche di automazione interfaccia utente visiva</strong></td>
<td>Visualizza la versione del software e le informazioni sul copyright per la verifica di Visual UIA.</td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a>Riquadri funzionali

Questa sezione descrive i riquadri funzionali nell'interfaccia utente di verifica di Visual UIA.

-   [Riquadro dell'albero elementi di automazione](#automation-elements-tree-pane)
-   [Riquadro test](#tests-pane)
-   [Riquadro Risultati test](#test-results-pane)
-   [Riquadro proprietà](#properties-pane)

### <a name="automation-elements-tree-pane"></a>Riquadro dell'albero elementi di automazione

Il riquadro dell' **albero degli elementi di automazione** contiene uno snapshot gerarchico di oggetti elemento di automazione disponibili per il test. Il primo elemento della struttura ad albero rappresenta il desktop.

Questa vista è una raccolta statica compilata al momento dell'avvio di Visual UIA Verify. Per aggiornare la visualizzazione nel nodo selezionato, utilizzare il comando di menu **Aggiorna elemento selezionato** o il pulsante della barra degli strumenti.

Lo screenshot seguente mostra il riquadro dell' **albero degli elementi di automazione** .

![riquadro dell'albero degli elementi di automazione della verifica di Visual UIA](images/automation-elements-tree-pane.png)

Un nodo grigio (non disponibile) nell' **albero degli elementi di automazione** indica che l'elemento è un membro della visualizzazione non elaborata di automazione interfaccia utente, ma non soddisfa le condizioni necessarie per essere considerato un membro della visualizzazione contenuto o della visualizzazione controlli. Tuttavia, l'elemento può comunque essere testato dalla verifica di automazione interfaccia utente visuale. Per altre informazioni, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).

I comandi disponibili dalla barra degli strumenti dell' **albero degli elementi di automazione** includono:

-   **Aggiorna**: consente di aggiornare il nodo selezionato e i relativi elementi figlio. Questo comando non aggiorna l'intero albero degli elementi a meno che non sia selezionato il nodo radice.
-   **Padre (CTRL + MAIUSC + F6)**: consente di passare all'elemento padre del nodo corrente.
-   **Primo elemento figlio (CTRL + MAIUSC + F7)**: passa al primo elemento figlio del nodo corrente.
-   Elemento di **pari livello successivo (CTRL + MAIUSC + F8)**: passa al figlio di pari livello successivo del nodo corrente.
-   Elemento di **pari livello precedente (CTRL + MAIUSC + F9)**: consente di passare all'elemento di pari livello precedente del nodo corrente.
-   **Ultimo elemento figlio (CTRL + MAIUSC + F10)**: passa all'ultimo elemento figlio del nodo corrente.
-   **Rilevamento dello stato attivo**: attiva o disattiva la selezione dei nodi in base al rilevamento dello stato attivo.

### <a name="tests-pane"></a>Riquadro test

Il riquadro **test** contiene un elenco di test di automazione interfaccia utente organizzati per tipo di test (**elemento di automazione**, **controllo** e **modello**) e priorità (**Verifica della compilazione**, **priorità 0**, **priorità 1**, **priorità 2** e **priorità 3**). Questo elenco viene generato in base al tipo di controllo dell'elemento selezionato nel riquadro **dell'albero degli elementi di automazione** . Per altre informazioni, vedere [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

Lo screenshot seguente mostra il riquadro **test** .

![riquadro test](images/test-pane.png)

I comandi disponibili dalla barra degli strumenti **test** includono:

-   **Mostra**: specifica i test di automazione interfaccia utente da visualizzare; ovvero visualizzare tutti i test o solo i test adatti al tipo di controllo dell'elemento selezionato nell' **albero degli elementi di automazione** (impostazione predefinita).
-   **Tipo**: specifica i tipi di test da visualizzare: **elemento di automazione**, **modello** o **controllo**.
-   **Priorità**— specifica le priorità di test da visualizzare **: verifica della compilazione**, **priorità 0**, **priorità 1**, **priorità 2** o **priorità 3**.
-   **Vai a sinistra**: consente di passare all'elemento padre del nodo corrente.
-   **Go up**: passare all'elemento di pari livello precedente del nodo corrente.
-   **Vai giù**— passa all'elemento di pari livello successivo del nodo corrente.
-   **Vai a destra**: passa al primo elemento figlio del nodo corrente.
-   **Esegui test selezionati**: esegue i test sull'elemento selezionato nell' **albero degli elementi di automazione**.

### <a name="test-results-pane"></a>Riquadro Risultati test

Il riquadro **risultati test** contiene la funzionalità di registrazione per la verifica degli oggetti visivi. Lo screenshot seguente mostra il riquadro **risultati test** .

![riquadro risultati test](images/test-results-pane.png)

I comandi disponibili dalla barra degli strumenti **risultati test** includono:

-   **Back**-pagina precedente nella cronologia di visualizzazione del report.
-   In **diretta**: pagina in futuro nella cronologia di visualizzazione del report.
-   **Complessiva**— Visualizza un riepilogo dei risultati del test (errore **passato**, **non riuscito** e **imprevisto**). Il risultato del test è collegato alla visualizzazione **tutti i risultati** . Il comando **generale** Visualizza una tabella come quella riportata di seguito.

    ![tabella dei risultati del test complessiva](images/overall-test-results.png)

-   **Tutti i risultati**: Visualizza un log dettagliato per ogni risultato del test, come illustrato nelle tabelle seguenti.

    ![Dettagli risultati log di esempio dalla vista tutti i risultati](images/all-results-log.png)

    Il nome del test nella tabella **tutti i risultati** è collegato a una descrizione test case per l'elemento, come nella tabella seguente.

    ![test case dettagli](images/test-case-detail.png)

-   **Log completo**— Visualizza una visualizzazione alternativa del log dettagliato per ogni risultato del test, come illustrato nella schermata seguente.

    ![visualizzazione alternativa di un test case dettaglio](images/alt-view-of-test-case-detail.png)

-   **XML**-Visualizza il codice XML non elaborato generato dal logger XML.
-   Ricerca **veloce**: ricerca di testo semplice della visualizzazione corrente nel riquadro **risultati test** .
-   **Apri in una nuova finestra**— apre la visualizzazione corrente in una nuova istanza di Internet Explorer.

### <a name="properties-pane"></a>Riquadro delle proprietà

Il riquadro **Proprietà** contiene un elenco di proprietà di automazione interfaccia utente e i valori di proprietà organizzati per tipo di proprietà: **accessibilità generale**, **Identificazione**, **modelli** (pattern di controllo), **stato** e **visibilità**. I valori delle proprietà vengono popolati dinamicamente in base al tipo di controllo dell'oggetto selezionato nel riquadro **dell'albero degli elementi di automazione** . Lo screenshot seguente mostra il riquadro **Proprietà** .

![riquadro proprietà](images/properties-pane.png)

Se il controllo selezionato supporta un pattern di controllo specifico, Visual UIA Verify fornisce la possibilità di chiamare metodi supportati da tale pattern di controllo. Ad esempio, il [tipo di controllo Window](uiauto-supportwindowcontroltype.md) supporta il [pattern di controllo Window](uiauto-implementingwindow.md), che dispone di un metodo [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) che può essere richiamato dal riquadro **Proprietà** , come illustrato nello screenshot seguente. Per altre informazioni, vedere [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

![Metodo Close del pattern di controllo Window richiamato dal riquadro proprietà](images/close-invoked-from-properties-pane.png)

I comandi disponibili nella barra degli strumenti **Proprietà** includono:

-   **Aggiorna**: consente di aggiornare l'albero delle **Proprietà** .
-   **Espandi tutto**— espande tutti i nodi nella struttura ad albero delle **Proprietà** .

 

 




