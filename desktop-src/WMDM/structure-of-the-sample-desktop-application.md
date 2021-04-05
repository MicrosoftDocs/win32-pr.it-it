---
title: Struttura dell'applicazione desktop di esempio
description: Struttura dell'applicazione desktop di esempio
ms.assetid: e042470d-dc78-488c-bcad-2e8d34714d5d
keywords:
- Windows Media Gestione dispositivi, esempi
- Gestione dispositivi, esempi
- applicazioni desktop, esempi
- Windows Media Gestione dispositivi, esempio di applicazione desktop
- Esempio di Gestione dispositivi, applicazione desktop
- esempi, applicazioni desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34fb377c1bb6ebf943721b55ec6175e65f70ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711119"
---
# <a name="structure-of-the-sample-desktop-application"></a>Struttura dell'applicazione desktop di esempio

L'applicazione desktop di esempio è costituita da due parti principali:

-   Il progetto wmdapp contiene la maggior parte delle classi che visualizzano l'interfaccia utente, gestiscono il trascinamento e rilascio ed eseguono tutte le funzionalità necessarie del programma.
-   Il progetto proghelp è un'applicazione helper che contiene classi non essenziali per gestire le notifiche di stato e i trasferimenti manuali di file dal desktop all'applicazione.

Il file eseguibile usa il progetto Helper solo quando l'utente seleziona **Usa interfaccia operazione** nel menu **Opzioni** per gestire il trasferimento manuale dei file al dispositivo e incrementa la barra di stato nel modulo stato download. Tutto il resto dell'applicazione viene gestito nel progetto wmdapp.



| Classe                | File                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| —                    | WMDMApp. cpp             | Classe che gestisce la finestra padre dell'interfaccia utente. Il codice in questo file gestisce anche alcuni input utente non gestiti da CDevFiles, ad esempio la creazione di una playlist o un album in un dispositivo, l'eliminazione di file e la registrazione delle scelte di menu.                                                                                                                                                    |
| CDevices             | Devices. cpp             | Classe che gestisce il riquadro sinistro della finestra principale dell'applicazione, in cui sono elencati i dispositivi disponibili. Questa classe gestisce il ciclo di messaggistica, che gestisce l'input dell'utente, ad esempio la selezione di un dispositivo e la notifica al riquadro CDevFiles di caricare i file appropriati quando la selezione del dispositivo è cambiata.                                                                              |
| CDevFiles            | Devfiles. cpp            | Classe che gestisce il riquadro destro della finestra principale dell'applicazione, in cui sono elencati i file nel dispositivo selezionato. Questa classe gestisce il ciclo di messaggistica e gestisce l'input dell'utente, ad esempio il trascinamento di file nel dispositivo e l'eliminazione di file dal dispositivo.                                                                                                                          |
| CStatus              | Stato. cpp              | Classe che gestisce la barra di stato inferiore nella finestra principale, in cui è elencato il numero di dispositivi e file, insieme alla quantità di memoria disponibile e usata sul dispositivo selezionato.                                                                                                                                                                                                         |
| CWMDM                | Wmdevmgr. cpp            | Interfaccia di primo livello per Windows Media Gestione dispositivi. Questa classe gestisce l'autenticazione, recupera l'interfaccia **IWMDeviceManager** di primo livello e si registra per le notifiche con l'interfaccia **IWMDMNotification** .                                                                                                                                                                  |
| CProgress            | Progress. cpp            | Classe nel progetto di applicazione principale che consente di creare e gestire la finestra di dialogo che mostra lo stato di avanzamento di un evento.                                                                                                                                                                                                                                                                             |
| CItemData            | ItemData. cpp            | Classe wrapper che include un puntatore a una risorsa di archiviazione (se rappresenta un file o una cartella nel dispositivo) o un dispositivo (se rappresenta un dispositivo), oltre a un'ampia gamma di informazioni sull'oggetto, tra cui dimensioni e attributi.                                                                                                                                                                  |
| CNotificationHandler | NotificationHandler. cpp | Gestisce le notifiche di arrivo e rimozione dei dispositivi inviando avvisi alla finestra CDevices.                                                                                                                                                                                                                                                                                                               |
| CProgressHelper      | ProgressHelper. cpp      | Creato da CDevFiles nelle funzioni locali per ricevere notifiche da Windows Media Gestione dispositivi implementando **IWMDMProgress**. Viene usato dalla classe CProgress per determinare la quantità di barre nell'indicatore di stato e al termine di un'azione. Questa classe è definita come un oggetto COM che espone l'interfaccia SDK **IWMDMProgress** e un'interfaccia personalizzata IWMDMProgressHelper. |
| COperationHelper     | Operationhelper. cpp     | Questa classe implementa **IWMDMOperation** per gestire il trasferimento manuale dei file. È multithread per consentirne l'esecuzione in modo asincrono e viene definito come un oggetto COM che espone un'interfaccia personalizzata, IWMDMOperationHelper, per creare un'istanza e inizializzare la classe. Questa classe viene utilizzata solo se l'utente seleziona "utilizza interfaccia operazione" nel menu **Opzioni** .                            |



 

Negli elenchi seguenti vengono illustrati i passaggi di base che si verificano per diverse azioni utente:

**All'avvio**

I passaggi principali seguenti si verificano quando viene avviata l'applicazione di esempio.

1.  Viene creata un'istanza e viene eseguita l'autenticazione della variabile CWMDM globale e viene eseguita la registrazione per ricevere le notifiche
2.  Viene creata un'istanza di CDevices globale e viene chiamato CDevices:: create per creare e riempire il riquadro dei dispositivi.
3.  Viene creata un'istanza di CDevFiles globale e viene chiamato CDevFiles:: create per creare il riquadro dei file, che non viene compilato fino a quando l'utente non seleziona un dispositivo.
4.  Viene creata un'istanza di CStatus globale e viene chiamato CStatus:: create per creare un'istanza della barra di stato.
5.  \_OnViewRefresh enumera tutti i dispositivi e Inizializza e aggiunge tutti i dispositivi (CItemData) a CDevices e aggiorna la barra di stato in modo da visualizzare il numero di dispositivi.
6.  CDevices:: AddItem aggiunge l'elemento al controllo TreeView che rappresenta i dispositivi, con un puntatore a se stesso come TVITEM. lParam. Tutti gli oggetti CDevice (Devices) e CDevFiles (file) vengono archiviati in questo membro del nodo TreeView nella finestra appropriata.

**Quando si seleziona un dispositivo**

I passaggi principali seguenti si verificano quando l'utente seleziona un dispositivo nel riquadro a sinistra della finestra dell'applicazione.

1.  La finestra CDevices intrappola un clic e invia un messaggio WM \_ DRM \_ UPDATEDEVICE a se stesso.
2.  CDevices riceve il proprio messaggio e chiama UpdateSelection, che indica all'oggetto CDevFiles globale di cancellare tutti gli elementi, enumerare tutti gli elementi di primo livello nel dispositivo e chiama CDevFiles:: AddItem per aggiungere ognuno al riquadro file.
3.  Infine, CDevices chiama CDevFiles:: UpdateStatusBar per aggiornare la barra di stato con le informazioni corrette sul dispositivo e sul file.

**Creazione di una playlist**

Dopo aver fatto clic su "Crea playlist" nel menu **contenitori** , l'applicazione chiama la funzione locale \_ OnCreatePlaylist, che esegue le azioni seguenti:

1.  Ottiene il numero di elementi selezionati dalla variabile globale CDevFiles.
2.  Chiamare la funzione locale DlgNamePlaylist per aprire una finestra di dialogo per ottenere un nome per la playlist.
3.  Chiamare il metodo CProgress:: create per creare una finestra di dialogo che mostra lo stato di avanzamento dell'azione e impostare i parametri sulla classe CProgress, ad esempio il testo del titolo, l'intervallo, il valore corrente e così via.
4.  Scorrere tutti gli elementi selezionati nell'oggetto visualizzazione albero CDevFiles e richiedere l'oggetto CItemData associato a ogni file selezionato nella visualizzazione albero, incrementando la barra della finestra di dialogo di stato con ogni file. I file vengono aggiunti a una matrice di interfacce [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) .
5.  Ottenere un handle per l'elemento attualmente selezionato ed eseguirvi una query per un'interfaccia [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) , che verrà usata in un secondo momento per creare la nuova playlist nel dispositivo.
6.  Eseguire una query sull'oggetto selezionato per [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)e chiamare [**CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject) per creare una nuova interfaccia [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata).
7.  Aggiungere il \_ codice del formato WMDM FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST alla nuova interfaccia **IWMDMMetadata** e creare una playlist sul dispositivo chiamando [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3), passando l'interfaccia dei metadati. Il metodo recupera un puntatore al nuovo **IWMDMStorage** sul dispositivo.
8.  Compilare la playlist eseguendo una query sulla nuova risorsa di archiviazione per [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)e chiamando [**IWMDMStorage4:: sereferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences), passando la matrice di puntatori **IWMDMStorage** raccolti nel passaggio 4.
9.  Infine, creare un nuovo oggetto CItemData per memorizzare la nuova playlist nel dispositivo, inizializzarla con la nuova risorsa di archiviazione e chiamare CDevFiles:: AddItem per aggiungerla al riquadro CDevFiles.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Applicazione desktop di esempio**](sample-desktop-application.md)
</dt> </dl>

 

 




