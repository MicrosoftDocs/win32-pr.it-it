---
title: Interfaccia grafica AccChecker Interfaccia utente
description: In questo argomento vengono descritti gli elementi che costituiscono l'interfaccia utente grafica di AccChecker.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf645a3afd35bdd906d1ab26453d16672311cb4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473387"
---
# <a name="the-accchecker-graphical-user-interface"></a>Interfaccia grafica AccChecker Interfaccia utente

In questo argomento vengono descritti gli elementi che costituiscono l'interfaccia utente grafica di AccChecker.

-   [Scheda Verifiche](#verifications-tab)
-   [Scheda Risultati](#results-tab)
-   [Schede dell'utilità per la lettura dello schermo MSAA e UIA](#msaa-and-uia-screen-reader-tabs)
-   [Schede dell'albero MSAA e UIA](#msaa-and-uia-tree-tabs)
-   [File Menu](#file-menu)
-   [Argomenti correlati](#related-topics)

## <a name="verifications-tab"></a>Scheda Verifiche

AccChecker inizia con la visualizzazione predefinita **della scheda Verifiche:**

![Screenshot che mostra la scheda "Verifiche" in Controllo accessibilità UI.](images/accchecker-verifications-tab.png)

La **scheda Verifiche** contiene i componenti seguenti.

-   **Selettore della destinazione di verifica** Offre le opzioni seguenti per la selezione di un'applicazione o di un controllo di destinazione.
    -   Scegliere una destinazione dall'elenco a discesa precompilato. Questo elenco contiene tutti gli HWND di primo livello identificati all'avvio.
    -   Scegliere un oggetto HWND in base alla posizione del cursore del mouse. I controlli selezionabili sono evidenziati con un rettangolo rosso. Questa opzione consente di selezionare qualsiasi oggetto visibile con HWND.
    -   Immettere un oggetto HWND specifico.
-   **Elenco di controllo per le routine di verifica** Consente di selezionare la routine di verifica desiderata da eseguire su un'applicazione o un controllo. Per altre informazioni, vedere Routine di verifica.
-   **Selettore di file di eliminazione di errori e avvisi** I file di eliminazione vengono generati dalla scheda **Risultati verifica.** Facendo clic con il pulsante destro  del mouse su un messaggio di errore o di avviso e scegliendo Elimina dal menu di scelta rapida, viene impostato un flag per il messaggio. Se la **casella di controllo** Eliminazioni è selezionata, le voci soppresse vengono visualizzate nell'elenco. Una voce soppressa può essere riattivata usando lo stesso menu di scelta rapida usato per sopprimerla.

    Un file di eliminazione viene salvato in formato XML scegliendo **Salva** eliminazione dal menu **File.** Questo file viene utilizzato nelle successive esecuzioni di verifica in cui i messaggi verranno nascosti. Per rimuovere il file di eliminazione, fare clic su **Cancella.** Per informazioni su messaggi specifici, vedere Messaggi del log di verifica. Usare **Salva log** dal menu **File** per salvare l'intero elenco come file di log in XML o come file di testo formattato.

    ![Scheda dei risultati di accchecker con l'elemento di contesto suppress evidenziato](images/accchecker-results-tab-with-suppress.png)

    L'esempio seguente mostra il contenuto di un  file di eliminazione generato eseguendo le verifiche delle proprietà nell'applicazione Windows del pannello di controllo firewall. In questo esempio è stato scelto l'errore con ID "ElementHasNoName" per l'eliminazione.

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

    

-   **Visualizzare i risultati classificati in ordine di priorità** Offre le opzioni seguenti per filtrare i risultati della verifica in base alla priorità.
    -   **Tutti** Includere tutti i risultati indipendentemente dalla priorità.
    -   **Solo P1** Includere solo i risultati con priorità 0 e priorità 1.
    -   **Solo P1 P2** Includere i risultati con priorità 0 e priorità 2.
-   **Eseguire le verifiche selezionate** Fornisce il **pulsante Esegui verifiche per** avviare il processo di verifica. Durante l'esecuzione delle verifiche,  il pulsante cambia in Annulla verifiche e può essere usato per arrestare le verifiche dopo il completamento di quella corrente.

## <a name="results-tab"></a>Scheda Risultati

La **scheda Risultati** viene popolata dopo il completamento delle attività di verifica selezionate. È costituito dai componenti seguenti.

-   Elenco dei messaggi, in cui vengono visualizzati i messaggi di errore, di avviso e informativi generati dalle attività di verifica selezionate. I messaggi visualizzati possono essere filtrati in base al tipo usando le caselle di controllo sopra l'elenco dei messaggi.
-   I dettagli del messaggio e una schermata della destinazione di verifica. Se si seleziona un messaggio dall'elenco dei messaggi, vengono visualizzati altri dettagli ed è evidenziato l'elemento corrispondente nel riquadro di acquisizione schermo. Il **pulsante Visualize** (Visualizza) consente di passare da AccChecker alla **scheda MSAA Tree (Albero MSAA).** Se nella scheda Risultati  è evidenziato un errore, l'elemento corrispondente viene evidenziato nella **scheda Albero MSAA.**

Facendo clic con il pulsante destro del mouse su un messaggio viene visualizzato un menu di scelta rapida con gli elementi seguenti.

-   **Non visualizzare** Aggiunge il messaggio all'elenco di eliminazione.
-   **Copia negli Appunti** Copia i dettagli del messaggio negli Appunti.
-   **Visualizza** Consente di passare da AccChecker alla **scheda Albero MSAA.** L'elemento che corrisponde all'errore selezionato è evidenziato.
-   **Guida** Visualizza informazioni aggiuntive sul messaggio.

## <a name="msaa-and-uia-screen-reader-tabs"></a>Schede dell'utilità per la lettura dello schermo MSAA e UIA

Le schede Utilità per la lettura dello schermo MSAA e Utilità per la lettura dello schermo dell'interfaccia utente sono simili. Entrambi visualizzano una trascrizione degli elementi rilevati in un attraversamento simulato della destinazione di verifica da un'utilità per la lettura dello schermo, ad eccezione del fatto che uno mostra l'implementazione msaa e l'altro mostra l'implementazione dell'interfaccia utente.

Gli elementi vengono esplorati e registrati esattamente come un'utilità per la lettura dello schermo li leggerebbe. Le informazioni presentate in questa scheda sono essenziali per confermare che vengono annunciate solo informazioni utili e pertinenti. Ad esempio, un nome di controllo normale, ad esempio "MenuItem Edit" o "PushButton Close", è accettabile. tuttavia, un nome di controllo che non ha senso, ad esempio "CPNavPanel22" o "DefaultValue1", non è accettabile. Il **pulsante Visualizza** fa sì che AccChecker svolga il passaggio alla scheda MsAA Tree (Albero **MSAA)** **o UIA Tree (Albero UIA).** Se un elemento è evidenziato nella scheda **Utilità per** la lettura dello schermo, l'elemento corrispondente viene evidenziato nella scheda Albero **MSAA** o Albero **UIA.**

È necessario selezionare  la routine di verifica  **ScreenReader** in Coerenza nella scheda Verifiche per visualizzare la scheda Utilità per la lettura dello schermo **MSAA.** Analogamente, è necessario selezionare la routine **di verifica UiaScreenReader** per visualizzare **la** scheda Utilità per la lettura dello schermo dell'interfaccia utente.

Lo screenshot seguente mostra la scheda Utilità per la lettura dello schermo con un esempio di verifica Blocco note.

![Scheda dell'utilità per la lettura dello schermo accchecker che visualizza i risultati della verifica di esempio](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a>Schede dell'albero MSAA e UIA

Se si esegue una routine di verifica, AccChecker compila tutti gli elementi visibili nella destinazione di verifica e li visualizza gerarchicamente nella scheda MsAA Tree (Albero **MSAA)** e **UIA Tree (Albero UIA).** Lo screenshot seguente mostra la scheda Albero MSAA con la gerarchia di elementi per Blocco note.

![Scheda dell'albero accchecker msaa](images/accchecker-tree-tab.png)

## <a name="file-menu"></a>Menu File




| Menu | Comando | Descrizione | 
|------|---------|-------------|
| <strong>File</strong>${REMOVE}$<br /> | <strong>Apri</strong> | Fornisce le opzioni seguenti.<br /><ul><li><strong>DLL verifiche</strong> Apre una DLL di verifica. Le verifiche Native AccChecker sono incapsulate in una DLL autonoma (VerificationRoutines.dll). Questa progettazione consente ai team di test di creare un proprio set di verifiche in base alla piattaforma dell'interfaccia utente testata.</li><li><strong>File di log</strong> Consente di scegliere un file di log di verifica da aprire.</li></ul> | 
| <strong>Caricare automaticamente le verifiche disponibili</strong> | Carica automaticamente tutte le verifiche AccChecker disponibili. | 
| <strong>Salva log</strong> | Salvare il log di verifica come XML o come testo normale. Il testo normale è più leggibile. | 
| <strong>Salva eliminazione</strong> | Salvare il log di eliminazione come XML. Questo file specifica i messaggi di verifica da ignorare nei test di regressione. | 
| <strong>Esci</strong> | Chiude lo strumento AccChecker. | 
| <strong>Verifiche</strong>${REMOVE}$<br /> | <strong>Esegui ora</strong> | Eseguire le routine di verifica come specificato per la destinazione di verifica scelta. | 
| <strong>Abilita tutto</strong> | Selezionare tutte le caselle di controllo della routine di verifica. | 
| <strong>Disabilita tutto</strong> | Deselezionare tutte le caselle di controllo della routine di verifica. | 
| <strong>Opzioni</strong> | <strong>Always On superiore</strong> | Impostare AccChecker come finestra in primo piano nell'ordine Z. | 
| <strong>Guida</strong>${REMOVE}$<br /> | <strong>?</strong> | Visualizzare le informazioni della Guida. | 
| <strong>Informazioni</strong> | Visualizzare la versione di AccChecker e un indirizzo di posta elettronica per contattare Microsoft su AccChecker. | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
</dt> </dl>

 

 





