---
description: Elenca le API (Application Programming Interface) di stampa introdotte in Windows Vista.
ms.assetid: 7a4eb5d7-b37d-4090-aea4-7274daa1e15c
title: Novità relative alla stampa in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8648d57f48623e6db0f6311bb07ae24ac15d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313999"
---
# <a name="whats-new-for-printing-in-windows-vista"></a>Novità relative alla stampa in Windows Vista

Elenca le API (Application Programming Interface) di stampa introdotte in Windows Vista.

Per gestire i ticket di stampa vengono utilizzate le funzioni e le enumerazioni seguenti.



| Funzione                                                               | Descrizione                                                                                                                                   | Intestazione    | Libreria     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------|-------------|
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) | Converte un ticket di stampa in una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .                                                                            | Prntvpt. h | Prntvpt. lib |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) | Converte un oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in un ticket di stampa.                                                                                      | Prntvpt. h | Prntvpt. lib |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)                             | Rilascia i buffer creati da alcune funzioni di gestione dei ticket di stampa.                                                                        | Prntvpt. h | Prntvpt. lib |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) | Convalida e unisce due ticket di stampa in un Print Ticket valido.                                                                            | Prntvpt. h | Prntvpt. lib |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)               | Ottiene un account delle funzionalità della stampante.                                                                                                | Prntvpt. h | Prntvpt. lib |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)                               | Apre un provider di ticket di stampa.                                                                                                                | Prntvpt. h | Prntvpt. lib |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)                           | Apre un provider di ticket di stampa, anche se non supporta la versione preferita dello [schema di stampa](./print-schema.md). | Prntvpt. h | Prntvpt. lib |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)                             | Chiude un provider di ticket di stampa.                                                                                                               | Prntvpt. h | Prntvpt. lib |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)     | Ottiene la versione più recente dello [schema di stampa](./print-schema.md) supportata da una stampante specificata.                        | Prntvpt. h | Prntvpt. lib |



 



| Enumerazione                                        | Descrizione                                                                                                                                                                               | Intestazione    |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) | Consente ai chiamanti di specificare quale [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) viene utilizzato come origine dei valori predefiniti quando un ticket di stampa non specifica tutte le impostazioni che potrebbero essere presenti in un oggetto **DEVMODE**. | Prntvpt. h |
| [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope)     | Specifica l'ambito di un ticket di stampa.                                                                                                                                                    | Prntvpt. h |



 

Per installare i driver della stampante vengono utilizzate le funzioni seguenti.



| Funzione                                                                   | Descrizione                                                                                                                                                                 | Intestazione     | Libreria      |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**CorePrinterDriverInstalled**](coreprinterdriverinstalled.md)           | Segnala se un driver della stampante principale con un GUID, una data e una versione specificati è installato.                                                                                | Winspool. h | Winspool. lib |
| [**DeletePrinterDriverPackage**](deleteprinterdriverpackage.md)           | Elimina un pacchetto di driver della stampante dall'archivio driver.                                                                                                                     | Winspool. h | Winspool. lib |
| [**GetCorePrinterDrivers**](getcoreprinterdrivers.md)                     | Ottiene il GUID, la versione e la data dei driver della stampante principale specificati e il percorso dei pacchetti.                                                                      | Winspool. h | Winspool. lib |
| [**GetPrinterDriverPackagePath**](getprinterdriverpackagepath.md)         | Ottiene il percorso del pacchetto di driver della stampante specificato in un server di stampa.                                                                                                    | Winspool. h | Winspool. lib |
| [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) | Installa un driver della stampante da un pacchetto driver nell'archivio driver del server di stampa.                                                                                         | Winspool. h | Winspool. lib |
| [**UploadPrinterDriverPackage**](uploadprinterdriverpackage.md)           | Carica un driver della stampante nell'archivio driver di un server di stampa, in modo che possa essere installato con [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md). | Winspool. h | Winspool. lib |



 

Le funzioni, le enumerazioni e le strutture seguenti vengono utilizzate per la stampa e la gestione delle stampanti e delle connessioni alle stampanti.



| Funzione                                               | Descrizione                                                                                                                                              | Intestazione     | Libreria      |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**AddPrinterConnection2**](addprinterconnection2.md) | Aggiunge una connessione alla stampante specificata per l'utente corrente.                                                                                         | Winspool. h | Winspool. lib |
| [**OpenPrinter2**](openprinter2.md)                   | Recupera un handle per la stampante o il server di stampa specificato o per altri tipi di handle nel sottosistema di stampa, durante l'impostazione di alcune opzioni della stampante. | Winspool. h | Winspool. lib |



 



| Enumerazione                                            | Descrizione                                                                                       | Intestazione     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------|------------|
| [**\_flag di opzione stampante \_**](printer-option-flags.md) | Specifica la memorizzazione nella cache di un handle per una stampante aperta con [**OpenPrinter2**](openprinter2.md). | Winspool. h |



 



| Struttura                                                         | Descrizione                                                                            | Intestazione     |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------|
| [**\_driver della stampante principale \_**](core-printer-driver.md)              | Rappresenta un driver della stampante da cui dipendono altri driver della stampante.              | Winspool. h |
| [**\_Informazioni driver \_ 8**](driver-info-8.md)                          | Rappresenta un driver della stampante.                                                           | Winspool. h |
| [**Informazioni sul modulo \_ \_ 2**](form-info-2.md)                              | Rappresenta le informazioni su un form di stampa localizzabile.                                 | Winspool. h |
| [**Informazioni sul processo \_ \_ 4**](job-info-4.md)                                | Rappresenta un set completo di valori associati a un processo e supporta i file di spooling a 64 bit. | Winspool. h |
| [**\_Informazioni di connessione stampante \_ \_ 1**](printer-connection-info-1.md) | Rappresenta le informazioni su una connessione a una stampante.                                | Winspool. h |
| [**\_Opzioni stampante**](printer-options.md)                       | Rappresenta le opzioni della stampante.                                                            | Winspool. h |
| [**PRINTPROCESSOR \_ Caps \_ 2**](printprocessor-caps-2.md)          | Rappresenta le informazioni sulla funzionalità della stampante.                                             | Winspool. h |



 

Le funzioni, le enumerazioni e le interfacce seguenti vengono utilizzate per implementare un nuovo sistema di notifica di stampa asincrona.



| Funzione                                                                             | Descrizione                                                                                                                                                                                       | Intestazione     | Libreria      |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)               | Consente di creare un canale di comunicazione tra il componente di stampa ospitato da spooler, ad esempio un driver di stampa o un monitor di porta, e un'applicazione che deve ricevere notifiche dal componente. | Prnasnot. h | Winspool. lib |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)     | Registra un'applicazione per ricevere notifiche da componenti ospitati da spooler quali driver della stampante, processori di stampa e monitor delle porte.                                                    | Prnasnot. h | Winspool. lib |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications) | Consente a un'applicazione che ha effettuato la registrazione di ricevere notifiche dai componenti di stampa ospitati da spooler per terminare la sottoscrizione alle notifiche.                                         | Prnasnot. h | Winspool. lib |



 



| Enumerazione                                                                    | Descrizione                                                                                                                                                                                                          | Intestazione     |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| [**PrintAsyncNotifyConversationStyle**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle) | Specifica se la comunicazione tra le applicazioni e i componenti ospitati dallo spooler di stampa, ad esempio i driver della stampante, i processori di stampa e i monitoraggi delle porte, è bidirezionale o unidirezionale.                          | Prnasnot. h |
| [**PrintAsyncNotifyError**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)                         | Specifica un errore in una transazione di notifica asincrona.                                                                                                                                                      | Prnasnot. h |
| [**PrintAsyncNotifyUserFilter**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)               | Specifica se le notifiche passeranno solo alle applicazioni in ascolto associate allo stesso utente del mittente ospitato dallo spooler di stampa o se verranno inviate a un set più ampio di applicazioni in ascolto. | Prnasnot. h |



 



| Interfaccia e metodo                                                                                                      | Descrizione                                                                                                                                                   | Intestazione     | Libreria      |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**IPrintAsyncNotifyCallback::ChannelClosed**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-channelclosed)    | Utilizzato da un membro di un canale di comunicazione per consigliare all'altro membro che il canale viene chiuso.                                                    | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyCallback::OnEventNotify**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-oneventnotify)    | Chiamato dallo spooler di stampa per avvertire un listener che è disponibile una notifica su un canale specificato.                                                      | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyChannel::CloseChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel)         | Chiude un canale di comunicazione.                                                                                                                               | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyChannel:: SendNotification**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification) | Invia una notifica da un componente ospitato dallo spooler di stampa a una o più applicazioni in ascolto oppure invia una risposta da un'applicazione a un componente. | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyDataObject::AcquireData**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata)  | Punta le applicazioni in ascolto ai dati di notifica, nonché le dimensioni e il tipo dei dati.                                                                   | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyDataObject::ReleaseData**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata)  | Rilascia la memoria utilizzata dai dati incapsulati in [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject).                                  | Prnasnot. h | Winspool. lib |



 

Per richiamare Microsoft XPS Document Converter (MXDC) che scrive i documenti XPS (XML Paper Specification) in un dispositivo o in un file, vengono utilizzate le strutture e le enumerazioni seguenti.



| Enumerazione                                | Descrizione                                                            | Intestazione |
|--------------------------------------------|------------------------------------------------------------------------|--------|
| [**MxdcS0PageEnums**](mxdcs0pageenums.md) | Specifica i tipi di risorse, ad esempio tipi di carattere o immagini, in una pagina XPS. | MXDC. h |



 



| Struttura                                                          | Descrizione                                                                                                                                    | Intestazione |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| [**MxdcEscapeHeader**](mxdcescapeheader.md)                       | Rappresenta un'istruzione per MXDC.                                                                                                         | MXDC. h |
| [**MxdcGetFileNameData**](mxdcgetfilenamedata.md)                 | Rappresenta il percorso completo e il nome di un file di output MXDC.                                                                                     | MXDC. h |
| [**MxdcPrintTicketEscape**](mxdcprintticketescape.md)             | Rappresenta una combinazione di [**MxdcEscapeHeader**](mxdcescapeheader.md) e [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md). | MXDC. h |
| [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md)   | Rappresenta un ticket di stampa che verrà associato a un documento XPS.                                                                        | MXDC. h |
| [**MxdcS0PageData**](mxdcs0pagedata.md)                           | Rappresenta una pagina in formato XPS da passare al file di output MXDC senza elaborazione.                                                  | MXDC. h |
| [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) | Rappresenta una combinazione di [**MxdcEscapeHeader**](mxdcescapeheader.md) e [**MxdcS0PageData**](mxdcs0pagedata.md).                         | MXDC. h |
| [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md)       | Rappresenta una combinazione di [**MxdcEscapeHeader**](mxdcescapeheader.md) e [**MxdcS0PageResource**](mxdcs0pageresourceescape.md).           | MXDC. h |
| [**MxdcS0PageResource**](mxdcs0pageresourceescape.md)             | Rappresenta una risorsa, ad esempio un tipo di carattere o un'immagine, inclusa in una pagina XPS da MXDC.                                                   | MXDC. h |



 

 

 
