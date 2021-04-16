---
title: Interfaccia utente grafica di AccChecker
description: Questo argomento descrive gli elementi che costituiscono l'interfaccia utente grafica di AccChecker.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26d847d1bc198958ca28dd77d67b0e99b9d7745
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104550314"
---
# <a name="the-accchecker-graphical-user-interface"></a>Interfaccia utente grafica di AccChecker

Questo argomento descrive gli elementi che costituiscono l'interfaccia utente grafica di AccChecker.

-   [Scheda verifiche](#verifications-tab)
-   [Scheda risultati](#results-tab)
-   [Schede MSAA ed UIA screen reader](#msaa-and-uia-screen-reader-tabs)
-   [Schede di albero MSAA e UIA](#msaa-and-uia-tree-tabs)
-   [Menu file](#file-menu)
-   [Argomenti correlati](#related-topics)

## <a name="verifications-tab"></a>Scheda verifiche

AccChecker inizia con la visualizzazione predefinita della scheda **verifiche** :

![Screenshot che mostra la scheda "verifiche" nel controllo di accessibilità U I.](images/accchecker-verifications-tab.png)

La scheda **verifiche** contiene i componenti seguenti.

-   **Selettore destinazione verifica** Offre le opzioni seguenti per selezionare un'applicazione o un controllo di destinazione.
    -   Scegliere una destinazione dall'elenco a discesa pre-popolato. Questo elenco contiene tutti gli HWND di primo livello identificati all'avvio.
    -   Scegliere un HWND in base alla posizione del cursore del mouse (i controlli selezionabili sono evidenziati con un rettangolo rosso). Questa opzione consente di selezionare qualsiasi oggetto visibile con HWND.
    -   Immettere un HWND specifico.
-   **Elenco di controllo routine di verifica** Consente di selezionare la routine di verifica desiderata da eseguire su un'applicazione o un controllo. Per ulteriori informazioni, vedere routine di verifica.
-   **Selettore file di eliminazione di errori e avvisi** I file di eliminazione vengono generati dalla scheda **risultati** verifica. Facendo clic con il pulsante destro del mouse su un messaggio di errore o di avviso e selezionando **Elimina** dal menu di scelta rapida, viene impostato un flag per il messaggio. Se la casella di controllo di **eliminazione** è selezionata, le voci non vengono visualizzate nell'elenco. Una voce eliminata può essere annullata usando lo stesso menu di scelta rapida usato per eliminarlo.

    Un file di eliminazione viene salvato in formato XML selezionando **Salva eliminazione** dal menu **file** . Questo file viene utilizzato nelle esecuzioni successive della verifica in cui i messaggi verranno nascosti. Per rimuovere il file di eliminazione, fare clic su **Cancella**. Per informazioni su messaggi specifici, vedere messaggi di log di verifica. Usare **Save log** dal menu **file** per salvare l'intero elenco come file di log in formato XML o come file di testo formattato.

    ![scheda risultati AccChecker con l'elemento di contesto non selezionato evidenziato](images/accchecker-results-tab-with-suppress.png)

    Nell'esempio seguente viene illustrato il contenuto di un file di eliminazione generato eseguendo le verifiche delle **Proprietà** nell'applicazione del pannello di controllo Windows Firewall. In questo esempio è stato scelto l'errore con ID "ElementHasNoName" per la soppressione.

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   **Mostra risultati classificati** in ordine di priorità In sono disponibili le opzioni seguenti per filtrare i risultati della verifica in base alla priorità.
    -   **Tutto** Includi tutti i risultati indipendentemente dalla priorità.
    -   **Solo P1** Includere solo i risultati con priorità 0 e priorità 1.
    -   **Solo P1 P2** Includere la priorità 0 tramite i risultati con priorità 2.
-   **Esegui verifiche selezionate** Fornisce il pulsante **Esegui verifiche** per avviare il processo di verifica. Mentre le verifiche sono in esecuzione, il pulsante cambia per **annullare le verifiche** e può essere usato per arrestare le verifiche dopo il completamento di quello corrente.

## <a name="results-tab"></a>Scheda Risultati

La scheda **risultati** viene popolata dopo il completamento delle attività di verifica selezionate. È costituito dai componenti seguenti.

-   Elenco dei messaggi, che consente di visualizzare i messaggi di errore, di avviso e informativi generati dalle attività di verifica selezionate. I messaggi visualizzati possono essere filtrati in base al tipo usando le caselle di controllo sopra l'elenco dei messaggi.
-   I dettagli del messaggio e un'acquisizione schermo della destinazione di verifica. La selezione di un messaggio dall'elenco dei messaggi Mostra ulteriori dettagli ed evidenzia l'elemento corrispondente nel riquadro acquisizione schermo. Il pulsante **Visualizza** , passa AccChecker alla scheda **albero MSAA** . Se viene evidenziato un errore nella scheda **risultati** , l'elemento corrispondente viene evidenziato nella scheda **albero MSAA** .

Facendo clic con il pulsante destro del mouse su un messaggio viene esposto un menu di scelta rapida con gli elementi seguenti.

-   Non **visualizzare** Aggiunge il messaggio all'elenco di eliminazione.
-   **Copia negli Appunti** Copia i dettagli del messaggio negli Appunti.
-   **Visualizza** Passa AccChecker alla scheda **albero MSAA** . L'elemento che corrisponde all'errore selezionato è evidenziato.
-   **Guida** di Visualizza informazioni aggiuntive sul messaggio.

## <a name="msaa-and-uia-screen-reader-tabs"></a>Schede MSAA ed UIA screen reader

Le schede lettore schermo MSAA e lettore schermata UIA sono simili. In entrambi i casi viene visualizzata una trascrizione di elementi rilevati in un attraversamento simulato della destinazione di verifica da parte di un'applicazione per la lettura dello schermo, ad eccezione del fatto che viene mostrata l'implementazione di MSAA e l'altra l'implementazione di

Gli elementi vengono spostati e registrati nello stesso modo in cui vengono letti dal lettore dello schermo. Le informazioni presentate in questa scheda sono essenziali per confermare che sono state annunciate solo informazioni utili e rilevanti. Ad esempio, un nome di controllo di normalizzazione, ad esempio "MenuItem Edit" o "close pulsante", è accettabile. Tuttavia, un nome di controllo che non ha senso, ad esempio "CPNavPanel22" o "DefaultValue1", non è accettabile. Il pulsante **Visualizza** , fa in modo che AccChecker passi all' **albero MSAA** o alla scheda **albero UIA** . Se un elemento viene evidenziato nella scheda **Visualizzatore schermo** , l'elemento corrispondente viene evidenziato nella scheda **albero MSAA** o **albero** di.

La  routine di verifica ScreenReader **in conformità deve** essere selezionata nella scheda **verifiche** per la visualizzazione della **scheda lettore schermata MSAA** . Analogamente, è necessario selezionare la routine di verifica **UiaScreenReader** per visualizzare la scheda di **lettura dello schermo di UIA** .

La schermata seguente mostra la scheda lettore schermata UIA con una verifica di esempio del blocco note.

![scheda lettore schermo AccChecker che Visualizza i risultati della verifica di esempio](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a>Schede di albero MSAA e UIA

L'esecuzione di una routine di verifica causa la compilazione di tutti gli elementi visibili nella destinazione di verifica da parte di AccChecker e la relativa visualizzazione gerarchica nella scheda **albero MSAA** e nella scheda dell' **albero** di gestione dei problemi. Lo screenshot seguente mostra la scheda albero MSAA con la gerarchia di elementi per blocco note.

![scheda albero MSAA AccChecker](images/accchecker-tree-tab.png)

## <a name="file-menu"></a>Menu File



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
<td rowspan="5"><strong>File</strong>$ {Remove} $<br />
</td>
<td><strong>Apri</strong></td>
<td>In sono disponibili le opzioni seguenti.<br/>
<ul>
<li><strong>Dll di verifica</strong> Apre una DLL di verifica. Le verifiche AccChecker native sono incapsulate in una DLL autonoma (VerificationRoutines.dll). Questa progettazione consente ai team di test di creare un proprio set di verifiche basate sulla piattaforma dell'interfaccia utente sottoposta a test.</li>
<li><strong>File di log</strong> Consente di scegliere un file di log di verifica da aprire.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Carica automaticamente le verifiche disponibili</strong></td>
<td>Carica automaticamente tutte le verifiche AccChecker disponibili.</td>

</tr>
<tr class="odd">
<td><strong>Salva log</strong></td>
<td>Salvare il log di verifica come XML o come testo normale. Il testo normale è più leggibile.</td>

</tr>
<tr class="even">
<td><strong>Salva eliminazione</strong></td>
<td>Salvare il log di eliminazione come XML. Questo file specifica i messaggi di verifica da ignorare nei test di regressione.</td>

</tr>
<tr class="odd">
<td><strong>Esci</strong></td>
<td>Chiude lo strumento AccChecker.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Verifiche</strong>$ {Remove} $<br />
</td>
<td><strong>Esegui adesso</strong></td>
<td>Eseguire le routine di verifica come specificato per la destinazione di verifica scelta.</td>
</tr>
<tr class="odd">
<td><strong>Abilita tutto</strong></td>
<td>Selezionare le caselle di controllo di tutte le routine di verifica.</td>

</tr>
<tr class="even">
<td><strong>Disabilita tutto</strong></td>
<td>Deselezionare tutte le caselle di controllo della routine di verifica.</td>

</tr>
<tr class="odd">
<td><strong>Opzioni</strong></td>
<td><strong>Always On Top</strong></td>
<td>Rendere AccChecker la finestra in primo piano nell'ordine z.</td>
</tr>
<tr class="even">
<td rowspan="2"><strong>Guida</strong>$ {Remove} $<br />
</td>
<td><strong>?</strong></td>
<td>Visualizzare le informazioni della guida.</td>
</tr>
<tr class="odd">
<td><strong>Informazioni</strong></td>
<td>Visualizzare la versione di AccChecker e un indirizzo di posta elettronica per contattare Microsoft su AccChecker.</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
</dt> </dl>

 

 





