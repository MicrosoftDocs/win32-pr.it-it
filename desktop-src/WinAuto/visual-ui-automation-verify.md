---
title: Verifica Automazione interfaccia utente visuale
description: Visual Automazione interfaccia utente Verify (Visual UIA Verify) è un Windows \ 32; Driver GUI per la libreria di test uia progettata per il test manuale dell'automazione interfaccia utente.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e8c6118914c791e04226dfa11d2c3bd9548368
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466848"
---
# <a name="visual-ui-automation-verify"></a>Verifica Automazione interfaccia utente visuale

Visual Automazione interfaccia utente Verify (Visual UIA Verify) è un driver dell'interfaccia utente grafica di Windows per la libreria di test uia progettata per il test manuale dell'automazione interfaccia utente. Fornisce un'interfaccia alla funzionalità della libreria di test dell'interfaccia utente che elimina l'overhead di scrittura del codice di uno strumento da riga di comando.

-   [Comandi di menu](#menu-commands)
-   [Riquadri funzionali](#functional-panes)
    -   [Riquadro albero elementi di automazione](#automation-elements-tree-pane)
    -   [Riquadro Test](#tests-pane)
    -   [Riquadro Risultati test](#test-results-pane)
    -   [Riquadro Proprietà](#properties-pane)

Visual UIA Verify supporta solo il logger XML di verifica UIA (WUIALoggerXml.dll) in modo nativo. Le trasformazioni XML selezionabili dall'utente sono incorporate in Visual UIA Verify per presentare diverse visualizzazioni del report del logger XML nel **Risultati test** controllo.

Per impostazione predefinita, Visual UIA Verify carica Automazione interfaccia utente provider sul lato client fornito con la versione originale di Automazione interfaccia utente. È possibile scegliere di non caricare questo provider aggiungendo **/NOCLIENTSIDEPROVIDER nell'opzione** della riga di comando di VisualUIVerifyNative.exe.

Lo screenshot seguente mostra le aree funzionali principali dell'interfaccia utente di verifica dell'interfaccia utente visiva.

![aree funzionali principali dell'interfaccia utente visivaa interfaccia utente di verifica](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a>Comandi di menu

La tabella seguente descrive i comandi del menu Verifica dell'interfaccia utente di Visual.




| Menu | Comando | Descrizione | 
|------|---------|-------------|
| <strong>File</strong> | <strong>Esci</strong> | Uscire da Visual UIA Verify. | 
| <strong>Visualizzazione</strong> | <strong>Evidenziazione</strong> | Evidenziare il rettangolo di delimitazione dell'elemento selezionato nel riquadro <strong>Albero degli elementi di</strong> automazione. Sono disponibili le seguenti opzioni.<ul><li><strong>Rettangolo:</strong>linea rossa continua.</li><li><strong>Rettangolo scompaia:</strong>linea rossa continua che scompare dopo alcuni secondi.</li><li><strong>Raggi e rettangolo: linea</strong>rossa continua con linee di evidenziazione blu aggiuntive che si esalano da ogni angolo del rettangolo di delimitazione.</li><li><strong>Nessuno: nessuna</strong>evidenziazione visibile.</li></ul> | 
| <strong>Albero degli elementi di automazione</strong>${REMOVE}$<br /> | <strong>Aggiorna elemento selezionato</strong> | Aggiornare gli elementi figlio dell'elemento selezionato nel riquadro <strong>Albero degli elementi di</strong> automazione. L'elenco di elementi è statico e non viene aggiornato dinamicamente (automaticamente) se l'albero degli elementi cambia. | 
| <strong>Spostamento</strong> | Spostarsi all'interno della gerarchia dell'albero degli elementi fino a uno degli elementi seguenti.<ul><li><strong>Parent:</strong>consente di passare all'elemento padre.</li><li><strong>First Child :</strong>consente di passare al primo elemento figlio.</li><li><strong>Successivo elemento di pari livello</strong>: consente di passare al primo elemento di pari livello.</li><li><strong>Precedente elemento di pari livello</strong>: consente di passare all'elemento di pari livello precedente.</li><li><strong>Last Child :</strong>consente di passare all'ultimo elemento figlio.</li></ul> | 
| <strong>Modalità</strong>${REMOVE}$<br /> | <strong>Always On superiore</strong> | La finestra Verifica dell'interfaccia utente visiva rimane nella parte superiore dell'ordine Z del desktop. | 
| <strong>Modalità al passaggio del mouse (usare CTRL)</strong> | Quando si preme CTRL, l'elemento sotto il cursore del mouse viene identificato come elemento di interesse. Il <strong>riquadro Albero degli elementi di</strong> automazione viene aggiornato e l'elemento corrispondente nell'elenco degli elementi viene evidenziato. | 
| <strong>Rilevamento dello stato attivo</strong> | Quando lo stato attivo cambia, l'elemento con lo stato attivo viene identificato come elemento di interesse. Il <strong>riquadro Albero degli elementi di</strong> automazione viene aggiornato e l'elemento corrispondente nell'elenco degli elementi viene evidenziato. | 
| <strong>Testa</strong>${REMOVE}$<br /> | <strong>Vai a sinistra</strong> | Spostare un nodo a sinistra <strong>nell'albero Test.</strong> | 
| <strong>Vai su</strong> | Spostare un nodo verso l'alto <strong>nell'albero</strong> Test. | 
| <strong>Vai in basso</strong> | Spostare un nodo verso il basso <strong>nell'albero Test.</strong> | 
| <strong>Vai a destra</strong> | Spostare un nodo a destra <strong>nell'albero</strong> Test. | 
| <strong>Esegui test selezionati sull'elemento selezionato</strong> | Eseguire i test selezionati <strong>dall'albero Test</strong> sull'elemento selezionato. | 
| <strong>Problemi noti del filtro</strong> | Filtrare i Automazione interfaccia utente noti dai risultati del test. | 
| <strong>?</strong> | <strong>Informazioni su Visual Automazione interfaccia utente Verify</strong> | Visualizzare la versione del software e le informazioni sul copyright per Visual UIA Verify. | 




 

## <a name="functional-panes"></a>Riquadri funzionali

Questa sezione descrive i riquadri funzionali nell'interfaccia utente di Verifica dell'interfaccia utente di Visual.

-   [Riquadro albero elementi di automazione](#automation-elements-tree-pane)
-   [Riquadro Test](#tests-pane)
-   [Riquadro Risultati test](#test-results-pane)
-   [Riquadro Proprietà](#properties-pane)

### <a name="automation-elements-tree-pane"></a>Riquadro albero elementi di automazione

Il **riquadro Albero degli elementi di automazione** contiene uno snapshot gerarchico degli oggetti elemento di automazione disponibili per il test. L'elemento superiore dell'albero rappresenta il desktop.

Questa visualizzazione è una raccolta statica che viene compilata all'avvio di Visual UIA Verify. Per aggiornare la visualizzazione nel nodo selezionato, usare il comando di menu **Aggiorna** elemento selezionato o il pulsante della barra degli strumenti.

Lo screenshot seguente mostra il riquadro **Albero degli elementi di** automazione.

![riquadro della struttura ad albero degli elementi di automazione dell'interfaccia utente visiva](images/automation-elements-tree-pane.png)

Un nodo in grigio (non  disponibile) nell'albero degli elementi di automazione indica che l'elemento è un membro della visualizzazione non elaborata di Automazione interfaccia utente, ma non soddisfa le condizioni necessarie per essere considerato un membro della visualizzazione contenuto o della visualizzazione controlli. Tuttavia, l'elemento può comunque essere testato da Visual Automazione interfaccia utente Verify. Per altre informazioni, vedere [cenni preliminari Automazione interfaccia utente albero di .](uiauto-treeoverview.md)

I comandi disponibili nella barra degli **strumenti Albero degli elementi di** automazione includono:

-   **Aggiorna:** aggiorna il nodo selezionato e i relativi elementi figlio. Questo comando non aggiorna l'intero albero degli elementi a meno che non sia selezionato il nodo radice.
-   **Padre (CTRL+MAIUSC+F6):** consente di passare al nodo padre del nodo corrente.
-   **Primo figlio (CTRL+MAIUSC+F7):** consente di passare al primo figlio del nodo corrente.
-   **Successivo elemento di pari livello (CTRL+MAIUSC+F8):** consente di passare al successivo elemento figlio di pari livello del nodo corrente.
-   **Precedente elemento di pari livello (CTRL+MAIUSC+F9):** consente di passare all'elemento di pari livello precedente del nodo corrente.
-   **Last Child (CTRL+MAIUSC+F10):** consente di passare all'ultimo elemento figlio del nodo corrente.
-   **Rilevamento dello stato attivo:** attiva o disattiva la selezione dei nodi in base al rilevamento dello stato attivo.

### <a name="tests-pane"></a>Riquadro Test

Il  riquadro Test contiene un elenco di test Automazione interfaccia utente organizzati per tipo di test **(** Elemento di automazione **,** Controllo e **Modello**) e priorità (**Verifica** compilazione , Priorità 0 , Priorità **1**, Priorità **2** e Priorità **3**).  Questo elenco viene generato in base al tipo di controllo dell'elemento selezionato nel riquadro **Albero degli elementi di** automazione. Per altre informazioni, vedere [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

Lo screenshot seguente mostra il **riquadro** Test.

![riquadro di test](images/test-pane.png)

I comandi disponibili nella barra **degli strumenti Test** includono:

-   **Mostra:** specifica i Automazione interfaccia utente test da visualizzare. ovvero visualizzare tutti i test o solo i test adatti al tipo di controllo dell'elemento selezionato nell'albero **degli elementi** di automazione (impostazione predefinita).
-   **Tipo:** specifica i tipi di test da visualizzare: **Elemento di automazione,** **Modello** o **Controllo**.
-   **Priorità:** specifica le priorità del test da **visualizzare:** Verifica compilazione, Priorità **0,** Priorità **1,** **Priorità 2** o **Priorità 3.**
-   **Vai a sinistra:** passare all'elemento padre del nodo corrente.
-   **Vai su:** consente di passare al nodo di pari livello precedente del nodo corrente.
-   **Vai giù:** passare al nodo di pari livello successivo del nodo corrente.
-   **Vai a destra:** passare al primo elemento figlio del nodo corrente.
-   **Esegui test selezionati: esegue** i test sull'elemento selezionato nell'albero **degli elementi di automazione**.

### <a name="test-results-pane"></a>Riquadro Risultati test

Il **Risultati test** contiene la funzionalità di registrazione Di verifica dell'interfaccia utente visiva. La schermata seguente mostra il riquadro **Risultati test.**

![riquadro risultati test](images/test-results-pane.png)

I comandi disponibili nella barra degli **strumenti Risultati** test includono:

-   **Indietro:** pagina indietro nella cronologia di visualizzazione del report.
-   **Avanti:** consente di inoltrare la pagina nella cronologia di visualizzazione del report.
-   **Generale:** visualizza un riepilogo dei risultati del test (**Superato,** **Non** riuscito e **Errore imprevisto**). Il risultato del test è collegato alla **visualizzazione Tutti i** risultati. Il **comando Generale** visualizza una tabella simile alla seguente.

    ![tabella dei risultati complessivi dei test](images/overall-test-results.png)

-   **Tutti i risultati:** visualizza un log dettagliato per ogni risultato del test, come illustrato nelle tabelle seguenti.

    ![Dettagli del risultato del log di esempio dalla visualizzazione tutti i risultati](images/all-results-log.png)

    Il nome del test nella **tabella Tutti i** risultati è collegato a una test case descrizione dell'elemento, come nella tabella seguente.

    ![test case dettagli](images/test-case-detail.png)

-   **Log completo:** visualizza una visualizzazione alternativa del log dettagliato per ogni risultato del test, come illustrato nello screenshot seguente.

    ![visualizzazione alternativa di un test case dettagli](images/alt-view-of-test-case-detail.png)

-   **XML:** visualizza il codice XML non elaborato generato dal logger XML.
-   **Ricerca rapida:** ricerca testuale semplice della visualizzazione corrente nel **riquadro** Risultati test ricerca.
-   **Apri in nuova finestra:** apre la visualizzazione corrente in una nuova istanza di Internet Explorer.

### <a name="properties-pane"></a>Riquadro delle proprietà

Il **riquadro** Proprietà contiene un elenco di Automazione interfaccia utente proprietà e valori di proprietà organizzati in base al tipo di proprietà: **Accessibilità** generale , **Identificazione**, **Pattern** (pattern di controllo), **Stato** e **Visibilità**. I valori delle proprietà vengono popolati dinamicamente in base al tipo di controllo dell'oggetto selezionato nel riquadro **Albero degli elementi di** automazione. Lo screenshot seguente mostra il **riquadro** Proprietà.

![riquadro delle proprietà](images/properties-pane.png)

Se il controllo selezionato supporta un pattern di controllo specifico, Visual UIA Verify offre la possibilità di chiamare i metodi supportati da tale pattern di controllo. Ad esempio, il [tipo di](uiauto-supportwindowcontroltype.md) controllo Window supporta il pattern di controllo [Window](uiauto-implementingwindow.md), che dispone di un metodo [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) che può essere richiamato dal riquadro Proprietà, come illustrato nello screenshot seguente.  Per altre informazioni, vedere [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

![Metodo close del pattern di controllo della finestra richiamato dal riquadro delle proprietà](images/close-invoked-from-properties-pane.png)

I comandi disponibili nella barra **degli strumenti** Proprietà includono:

-   **Aggiorna:** aggiornare **l'albero** Proprietà.
-   **Espandi tutto:** espande tutti i nodi **nell'albero** Proprietà.

 

 




