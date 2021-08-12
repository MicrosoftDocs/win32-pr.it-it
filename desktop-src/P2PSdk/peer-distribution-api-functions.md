---
description: Il servizio Distribuzione peer Microsoft supporta funzioni per scenari con ruolo consumer e ruolo editore.
ms.assetid: 3f5af891-4f5d-4523-8fe6-47fc6ff13b35
title: Funzioni dell'API di distribuzione peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a594313300c6bf39a2ea4f08efba89d1ed757ba4b8a50eda074466b94433e1e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612322"
---
# <a name="peer-distribution-api-functions"></a>Funzioni dell'API di distribuzione peer

Il servizio Distribuzione peer Microsoft supporta funzioni per scenari con ruolo consumer e ruolo editore.

## <a name="the-following-functions-are-common-in-both-client-and-server-scenarios"></a>Le funzioni seguenti sono comuni negli scenari "client" e "server".



| Funzioni comuni                                                                                       | Descrizione                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                                                             | Crea una nuova **istanza DI \_ PEERDIST INSTANCE \_ HANDLE** che deve essere passata a tutte le altre API di distribuzione peer. |
| [**PeerDistShutdown**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistshutdown)                                                           | Rilascia le risorse allocate dalla chiamata a [**PeerDistStartup.**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                         |
| [**PeerDistGetStatus**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatus)                                                         | Restituisce lo stato corrente del servizio di distribuzione peer.                                                        |
| [**PeerDistGetStatusEx**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatusex)                                                     | Restituisce lo stato corrente e le funzionalità del servizio di distribuzione peer.                                   |
| [**PeerDistGetOverlappedResult**](/windows/desktop/api/peerdist/nf-peerdist-peerdistgetoverlappedresult)                                     | Recupera i risultati delle operazioni asincrone.                                                               |
| [**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)     | Richiede che il servizio di distribuzione peer invii una notifica al chiamante quando si verifica una modifica dello stato.                      |
| [**PeerDistRegisterForStatusChangeNotificationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotificationex) | Richiede che il servizio di distribuzione peer invii una notifica al chiamante quando si verifica una modifica dello stato.                      |
| [**PeerDistUnregisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistunregisterforstatuschangenotification) | Annulla la registrazione della notifica di modifica dello stato per la sessione associata all'handle fornito.                 |



 

## <a name="the-following-functions-are-only-supported-in-client-scenarios"></a>Le funzioni seguenti sono supportate solo negli scenari "client".



| Funzioni client                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                               | Apre e restituisce un **HANDLE DI CONTENUTO PEERDIST \_ \_ per** fare riferimento a tale contenuto.                                                                                                                                                                                                                                                                     |
| [**PeerDistClientCloseContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientclosecontent)                             | Chiude **l'HANDLE DI \_ CONTENUTO \_ PEERDIST.**                                                                                                                                                                                                                                                                                                        |
| [**PeerDistClientGetInformationByHandle**](/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle)         | Recupera informazioni aggiuntive dal servizio di distribuzione peer per un handle di contenuto specifico.                                                                                                                                                                                                                                               |
| [**PeerDistClientAddContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientaddcontentinformation)           | Aggiunge informazioni sul contenuto che vengono quindi associate **all'HANDLE DI CONTENUTO \_ PEERDIST. \_** Un **HANDLE DI \_ CONTENUTO \_ PEERDIST** può essere associato a qualsiasi informazione sul contenuto.                                                                                                                                                                        |
| [**PeerDistClientCompleteContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcompletecontentinformation) | Indica la fine delle informazioni sul contenuto.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientAddData**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientadddata)                                       | Utilizzato per fornire contenuto alla cache locale. Questa operazione viene in genere eseguita quando non è possibile trovare i dati nella rete locale, come indicato quando [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread) o [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread) viene completato con **ERROR \_ TIMEOUT** o **PEERDIST \_ ERROR MISSING \_ \_ DATA**. |
| [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread)                                   | Fornisce l'accesso casuale al flusso di contenuto.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread)                                 | Fornisce l'accesso sequenziale al flusso di contenuto.                                                                                                                                                                                                                                                                                                |
| [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)                             | Rimuove il contenuto aggiunto in precedenza al sistema di distribuzione peer locale.                                                                                                                                                                                                                                                            |
| [**PeerDistClientCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcancelasyncoperation)             | Annulla l'operazione asincrona associata a una struttura [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) e all'handle di contenuto restituito da [**PeerDistClientOpenContent.**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                                                                                                                     |



 

## <a name="the-following-functions-are-only-supported-in-server-scenarios"></a>Le funzioni seguenti sono supportate solo negli scenari "server".



| Funzioni server                                                                             | Descrizione                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)                           | Crea **\_ \_ l'HANDLE DI FLUSSO PEERDIST** che può essere usato con [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream) per creare informazioni sul contenuto per il flusso di contenuto. |
| [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)                 | Aggiunge dati al flusso a cui fa riferimento l'handle del flusso PeerDist.                                                                                                                                  |
| [**PeerDistServerPublishCompleteStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishcompletestream)           | Chiamato per indicare che tutti i dati sono stati aggiunti al flusso.                                                                                                                                     |
| [**PeerDistServerCloseStreamHandle**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosestreamhandle)                   | Chiude l'handle del flusso.                                                                                                                                                                          |
| [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish)                                   | Annulla la pubblicazione del contenuto pubblicato in precedenza nel servizio di distribuzione peer.                                                                                                                         |
| [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)         | Apre un **HANDLE PEERDIST \_ CONTENTINFO \_ per** il contenuto pubblicato.                                                                                                                                   |
| [**PeerDistServerOpenContentInformationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex)     | Apre un **HANDLE PEERDIST \_ CONTENTINFO \_ per** il contenuto pubblicato.                                                                                                                                   |
| [**PeerDistServerRetrieveContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverretrievecontentinformation) | Recupera le informazioni sul contenuto associate al contenuto pubblicato.                                                                                                                               |
| [**PeerDistServerCloseContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosecontentinformation)       | **PEERDIST \_ HANDLE \_ CONTENTINFO** aperto da [**PeerDistServerOpenContentInformation.**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)                                                                  |
| [**PeerDistServerCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistservercancelasyncoperation)             | Annulla l'operazione asincrona associata all'identificatore di contenuto e [alla struttura OVERLAPPED.](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)                                             |



 

 

 
