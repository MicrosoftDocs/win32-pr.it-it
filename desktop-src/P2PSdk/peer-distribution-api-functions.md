---
description: Il servizio di distribuzione peer Microsoft supporta le funzioni sia per gli scenari del ruolo utente che del ruolo di server di pubblicazione.
ms.assetid: 3f5af891-4f5d-4523-8fe6-47fc6ff13b35
title: Funzioni API per la distribuzione di peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2532ad8bf5cbb14e18bd16a14bb1be2d79c1791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312251"
---
# <a name="peer-distribution-api-functions"></a>Funzioni API per la distribuzione di peer

Il servizio di distribuzione peer Microsoft supporta le funzioni sia per gli scenari del ruolo utente che del ruolo di server di pubblicazione.

## <a name="the-following-functions-are-common-in-both-client-and-server-scenarios"></a>Le funzioni seguenti sono comuni negli scenari "client" e "Server".



| Funzioni comuni                                                                                       | Descrizione                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                                                             | Crea una nuova istanza dell' **\_ \_ handle di istanza PEERDIST** che deve essere passata a tutte le altre API di distribuzione peer. |
| [**PeerDistShutdown**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistshutdown)                                                           | Rilascia le risorse allocate dalla chiamata a [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup).                         |
| [**PeerDistGetStatus**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatus)                                                         | Restituisce lo stato corrente del servizio di distribuzione peer.                                                        |
| [**PeerDistGetStatusEx**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatusex)                                                     | Restituisce lo stato corrente e le funzionalità del servizio di distribuzione peer.                                   |
| [**PeerDistGetOverlappedResult**](/windows/desktop/api/peerdist/nf-peerdist-peerdistgetoverlappedresult)                                     | Recupera i risultati delle operazioni asincrone.                                                               |
| [**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)     | Richiede che il servizio di distribuzione peer invii una notifica al chiamante quando si verifica una modifica dello stato.                      |
| [**PeerDistRegisterForStatusChangeNotificationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotificationex) | Richiede che il servizio di distribuzione peer invii una notifica al chiamante quando si verifica una modifica dello stato.                      |
| [**PeerDistUnregisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistunregisterforstatuschangenotification) | Annulla la registrazione della notifica di modifica dello stato per la sessione associata all'handle fornito.                 |



 

## <a name="the-following-functions-are-only-supported-in-client-scenarios"></a>Le funzioni seguenti sono supportate solo negli scenari "client".



| Funzioni client                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                               | Apre e restituisce un **\_ \_ handle di contenuto PEERDIST** per fare riferimento a tale contenuto.                                                                                                                                                                                                                                                                     |
| [**PeerDistClientCloseContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientclosecontent)                             | Chiude l' **\_ \_ handle di contenuto PEERDIST**.                                                                                                                                                                                                                                                                                                        |
| [**PeerDistClientGetInformationByHandle**](/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle)         | Recupera informazioni aggiuntive dal servizio di distribuzione peer per un handle di contenuto specifico.                                                                                                                                                                                                                                               |
| [**PeerDistClientAddContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientaddcontentinformation)           | Aggiunge le informazioni sul contenuto che vengono quindi associate **all' \_ \_ handle di contenuto PEERDIST**. Un **\_ \_ handle di contenuto PEERDIST** può essere associato a qualsiasi informazione sul contenuto.                                                                                                                                                                        |
| [**PeerDistClientCompleteContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcompletecontentinformation) | Indica la fine delle informazioni sul contenuto.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientAddData**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientadddata)                                       | Utilizzato per fornire contenuto alla cache locale. Questa operazione viene in genere eseguita quando non è possibile trovare i dati nella rete locale come indicato quando [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread) o [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread) è stato completato con il **\_ timeout di errore** o **PEERDIST \_ \_ mancano \_ i dati**. |
| [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread)                                   | Consente l'accesso casuale al flusso di contenuto.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread)                                 | Fornisce l'accesso sequenziale al flusso di contenuto.                                                                                                                                                                                                                                                                                                |
| [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)                             | Rimuove il contenuto aggiunto in precedenza al sistema di distribuzione dei peer locali.                                                                                                                                                                                                                                                            |
| [**PeerDistClientCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcancelasyncoperation)             | Annulla l'operazione asincrona associata a una struttura [sovrapposta](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) e l'handle di contenuto restituito da [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).                                                                                                                     |



 

## <a name="the-following-functions-are-only-supported-in-server-scenarios"></a>Le funzioni seguenti sono supportate solo negli scenari "Server".



| Funzioni server                                                                             | Descrizione                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)                           | Crea l' **\_ \_ handle del flusso PEERDIST** che può essere usato con [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream) per creare informazioni sul contenuto per il flusso di contenuto. |
| [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)                 | Aggiunge dati al flusso a cui fa riferimento l'handle del flusso PeerDist.                                                                                                                                  |
| [**PeerDistServerPublishCompleteStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishcompletestream)           | Chiamato per indicare che tutti i dati sono stati aggiunti al flusso.                                                                                                                                     |
| [**PeerDistServerCloseStreamHandle**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosestreamhandle)                   | Chiude l'handle del flusso.                                                                                                                                                                          |
| [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish)                                   | Annulla la pubblicazione del contenuto pubblicato in precedenza nel servizio di distribuzione peer.                                                                                                                         |
| [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)         | Apre un **\_ \_ handle CONTENTINFO PEERDIST** per il contenuto pubblicato.                                                                                                                                   |
| [**PeerDistServerOpenContentInformationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex)     | Apre un **\_ \_ handle CONTENTINFO PEERDIST** per il contenuto pubblicato.                                                                                                                                   |
| [**PeerDistServerRetrieveContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverretrievecontentinformation) | Recupera le informazioni sul contenuto associate al contenuto pubblicato.                                                                                                                               |
| [**PeerDistServerCloseContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosecontentinformation)       | **PEERDIST \_ \_Handle CONTENTINFO** aperto da [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation).                                                                  |
| [**PeerDistServerCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistservercancelasyncoperation)             | Annulla l'operazione asincrona associata all'identificatore del contenuto e alla struttura [sovrapposta](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .                                             |



 

 

 
