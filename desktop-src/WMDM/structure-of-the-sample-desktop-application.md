---
title: Struttura dell'applicazione desktop di esempio
description: Struttura dell'applicazione desktop di esempio
ms.assetid: e042470d-dc78-488c-bcad-2e8d34714d5d
keywords:
- Windows Gestione dispositivi multimediali, esempi
- Gestione dispositivi, esempi
- applicazioni desktop, esempi
- Windows Esempio di applicazione desktop di Gestione dispositivi multimediali
- Esempio di applicazione desktop di Gestione dispositivi
- esempi, applicazioni desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dde8250a5efc8bc0f0b9582739bd8770d95ee586ea571a43bcbb9be69e8774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957161"
---
# <a name="structure-of-the-sample-desktop-application"></a>Struttura dell'applicazione desktop di esempio

L'applicazione desktop di esempio è costituita da due parti principali:

-   Il progetto wmdapp contiene la maggior parte delle classi che visualizzano l'interfaccia utente, gestiscono il trascinamento della selezione ed eseguono tutte le funzionalità necessarie del programma.
-   Il progetto proghelp è un'applicazione helper che contiene classi nonessential per gestire le notifiche di stato e i trasferimenti manuali di file dal desktop all'applicazione.

Il file eseguibile usa il progetto  helper solo quando l'utente seleziona Usa interfaccia operazione dal **menu** Opzioni per gestire il trasferimento manuale di file al dispositivo e per incrementare la barra di stato nel modulo di stato del download. Tutto il resto dell'applicazione viene gestito nel progetto wmdapp.



| Classe                | File                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| —                    | wmdmapp.cpp             | Classe che gestisce la finestra padre dell'interfaccia utente. Il codice in questo file gestisce anche alcuni input utente non gestiti da CDevFiles, ad esempio la creazione di una playlist o di un album in un dispositivo, l'eliminazione di file e la registrazione delle scelte di menu.                                                                                                                                                    |
| CDevices             | Devices.cpp             | Classe che gestisce il riquadro sinistro della finestra principale dell'applicazione, in cui sono elencati i dispositivi disponibili. Questa classe gestisce il ciclo di messaggistica, che gestisce l'input dell'utente, ad esempio la selezione di un dispositivo e la notifica al riquadro CDevFiles di caricare i file appropriati quando la selezione del dispositivo è stata modificata.                                                                              |
| CDevFiles            | Devfiles.cpp            | Classe che gestisce il riquadro di destra della finestra principale dell'applicazione, in cui sono elencati i file nel dispositivo selezionato. Questa classe gestisce il ciclo di messaggistica e gestisce l'input dell'utente, ad esempio il trascinamento di file nel dispositivo e l'eliminazione di file dal dispositivo.                                                                                                                          |
| CStatus              | Status.cpp              | Classe che gestisce la barra di stato inferiore nella finestra principale, in cui è elencato il numero di dispositivi e file, insieme alla quantità di memoria disponibile e usata nel dispositivo selezionato.                                                                                                                                                                                                         |
| CWMDM                | Wmdevmgr.cpp            | L'interfaccia di primo livello per Windows Gestione dispositivi multimediali. Questa classe gestisce l'autenticazione, recupera l'interfaccia **IWMDeviceManager** di primo livello e si registra per le notifiche con **l'interfaccia IWMDMNotification.**                                                                                                                                                                  |
| CProgress            | Progress.cpp            | Classe nel progetto di applicazione principale che crea e gestisce la finestra di dialogo che mostra lo stato di un evento.                                                                                                                                                                                                                                                                             |
| CItemData            | ItemData.cpp            | Classe wrapper che contiene un puntatore a un archivio (se rappresenta un file o una cartella nel dispositivo) o a un dispositivo (se rappresenta un dispositivo), nonché un'ampia gamma di informazioni sull'oggetto, incluse le dimensioni e gli attributi.                                                                                                                                                                  |
| CNotificationHandler | Notificationhandler.cpp | Gestisce le notifiche di arrivo e rimozione del dispositivo inviando un avviso alla finestra CDevices.                                                                                                                                                                                                                                                                                                               |
| CProgressHelper      | ProgressHelper.cpp      | Creato da CDevFiles nelle funzioni locali per ricevere notifiche Windows Gestione dispositivi multimediali implementando **IWMDMProgress**. Viene usato dalla classe CProgress per determinare la quantità di barre nell'indicatore di stato e al termine di un'azione. Questa classe è definita come oggetto COM che espone l'interfaccia SDK **IWMDMProgress** e un'interfaccia personalizzata IWMDMProgressHelper. |
| COperationHelper     | Operationhelper.cpp     | Questa classe implementa **IWMDMOperation per** gestire il trasferimento manuale dei file. È multi-thread per consentire che si verifichi in modo asincrono ed è definito come oggetto COM che espone un'interfaccia personalizzata, IWMDMOperationHelper, per creare un'istanza e inizializzare la classe. Questa classe viene usata solo se l'utente seleziona "Usa interfaccia operazione" **nel** menu Opzioni.                            |



 

Di seguito sono elencati i passaggi di base che si verificano per le varie azioni dell'utente:

**All'avvio**

I passaggi principali seguenti si verificano all'avvio dell'applicazione di esempio.

1.  Viene creata e autenticata la variabile CWMDM globale e viene registrato per ricevere notifiche
2.  Viene creata un'istanza di CDevices globale e viene chiamato CDevices::Create per creare e riempire il riquadro dei dispositivi.
3.  Viene creata un'istanza di CDevFiles globale e viene chiamato CDevFiles::Create per creare il riquadro dei file , che non viene riempito fino a quando l'utente non seleziona un dispositivo.
4.  Viene creata un'istanza di CStatus globale e viene chiamato CStatus::Create per creare un'istanza della barra di stato.
5.  \_OnViewRefresh enumera tutti i dispositivi e inizializza e aggiunge tutti i dispositivi (CItemData) a CDevices e aggiorna la barra di stato per visualizzare il numero di dispositivi.
6.  CDevices::AddItem aggiunge l'elemento alla visualizzazione albero che rappresenta i dispositivi, con un puntatore a se stesso come TVITEM.lparam. Tutti gli oggetti CDevice (dispositivi) e CDevFiles (file) vengono archiviati in questo membro del nodo treeview nella finestra appropriata.

**Quando si seleziona un dispositivo**

I passaggi principali seguenti si verificano quando l'utente seleziona un dispositivo nel riquadro sinistro della finestra dell'applicazione.

1.  La finestra CDevices intercetta un clic e invia un messaggio WM \_ DRM \_ UPDATEDEVICE a se stesso.
2.  CDevices riceve il proprio messaggio e chiama UpdateSelection, che indica all'oggetto CDevFiles globale di cancellare tutti gli elementi, enumerare tutti gli elementi di primo livello nel dispositivo e chiama CDevFiles::AddItem per aggiungere ognuno al riquadro dei file.
3.  Infine, CDevices chiama CDevFiles::UpdateStatusBar per aggiornare la barra di stato con le informazioni corrette sul dispositivo e sul file.

**Alla creazione di una playlist**

Dopo aver fatto clic su "Crea playlist" nel **menu** Contenitori, l'applicazione chiama la funzione locale \_ OnCreatePlaylist, che esegue le azioni seguenti:

1.  Ottiene il numero di elementi selezionati dalla variabile CDevFiles globale.
2.  Chiamare la funzione locale DlgNamePlaylist per aprire una finestra di dialogo per ottenere un nome per la playlist.
3.  Chiamare CProgress::Create per creare una finestra di dialogo che mostra lo stato dell'azione e impostare i parametri nella classe CProgress, ad esempio il testo del titolo, l'intervallo, il valore corrente e così via.
4.  Scorrere tutti gli elementi selezionati nell'oggetto visualizzazione albero CDevFiles e richiedere l'oggetto CItemData associato a ogni file selezionato nella visualizzazione albero, incrementando la barra della finestra di dialogo di stato con ogni file. I file vengono aggiunti a una matrice di [**interfacce IWMDMStorage.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)
5.  Ottenere un handle per l'elemento attualmente selezionato ed eseguire una query per [**un'interfaccia IWMDMStorageControl3,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) che verrà usata in un secondo momento per creare la nuova playlist nel dispositivo.
6.  Eseguire una query sull'oggetto selezionato [**per IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)e chiamare [**CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject) per creare una nuova [**interfaccia IWMDMMetaData.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)
7.  Aggiungere il codice di formato WMDM FORMATCODE ABSTRACTAUDIOVIDEOPLAYLIST alla nuova interfaccia IWMDMMetadata e creare una playlist nel dispositivo chiamando \_ \_ [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3),  passando l'interfaccia dei metadati. Il metodo recupera un puntatore al nuovo **IWMDMStorage** nel dispositivo.
8.  Compilare la playlist effettuando una query sulla nuova archiviazione [**per IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)e chiamando [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences), passando la matrice di puntatori **IWMDMStorage** raccolti nel passaggio 4.
9.  Creare infine un nuovo oggetto CItemData per contenere la nuova playlist nel dispositivo, inizializzarla con la nuova archiviazione e chiamare CDevFiles::AddItem per aggiungerla al riquadro CDevFiles.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Applicazione desktop di esempio**](sample-desktop-application.md)
</dt> </dl>

 

 




