---
title: Funzioni client del trasporto WDS
description: Questo modulo definisce le strutture e le funzioni che compongono l'interfaccia tra il ricevitore del contenuto e il client di trasporto.
ms.assetid: 20c3116b-3a0d-4048-b6f2-81c03e0a80ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8449f620eb04045d37e56499be998477d361871c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298741"
---
# <a name="wds-transport-client-functions"></a>Funzioni client del trasporto WDS

Questo modulo definisce le strutture e le funzioni che compongono l'interfaccia tra il ricevitore del contenuto e il client di trasporto.



| Funzione                                                                              | Descrizione                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*\_WDSTRANSPORTCLIENTRECEIVECONTENTS PFN*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivecontents) | Indica che un blocco di dati è pronto per essere utilizzato.                                                                                                                         |
| [*\_WDSTRANSPORTCLIENTRECEIVEMETADATA PFN*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivemetadata) | Riceve informazioni sui metadati di un file.                                                                                                                                 |
| [*\_WDSTRANSPORTCLIENTSESSIONCOMPLETE PFN*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessioncomplete) | Indica che la sessione è stata completata correttamente o si è verificato un errore.                                                                                                  |
| [*\_WDSTRANSPORTCLIENTSESSIONSTART PFN*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstart)       | Indica le dimensioni del file e altre informazioni sul lato server del file al consumer.                                                                                   |
| [*\_WDSTRANSPORTCLIENTSESSIONSTARTEX PFN*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex)   | Indica le dimensioni del file e altre informazioni sul lato server del file al consumer.                                                                                   |
| [**WdsTransportClientAddRefBuffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientaddrefbuffer)              | Incrementa il conteggio dei riferimenti in un buffer di proprietà del client multicast.                                                                                                   |
| [**WdsTransportClientCancelSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcancelsession)            | Rilascia le risorse associate a una sessione nel client.                                                                                                             |
| [**WdsTransportClientCloseSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientclosesession)              | Rilascia le risorse associate a una sessione nel client.                                                                                                             |
| [**WdsTransportClientCompleteReceive**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcompletereceive)        | Indica che tutte le operazioni di elaborazione in un blocco di dati sono state completate e che il client multicast può rimuovere questo blocco di dati dalla relativa cache per fare spazio a ulteriori ricezioni. |
| [**WdsTransportClientInitialize**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitialize)                  | Inizializza il client multicast.                                                                                                                                           |
| [**WdsTransportClientInitializeSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitializesession)    | Avvia un trasferimento di file multicast.                                                                                                                                        |
| [**WdsTransportClientQueryStatus**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientquerystatus)                | Recupera lo stato corrente di una trasmissione multicast in corso o completa dal client multicast.                                                                    |
| [**WdsTransportClientRegisterCallback**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientregistercallback)      | Registra un callback con il client multicast.                                                                                                                             |
| [**WdsTransportClientReleaseBuffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientreleasebuffer)            | Decrementa il conteggio dei riferimenti in un buffer di proprietà del client multicast.                                                                                                   |
| [**WdsTransportClientShutdown**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientshutdown)                      | Arresta il client multicast.                                                                                                                                            |
| [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession)              | Avvia un trasferimento di file multicast.                                                                                                                                        |
| [**WdsTransportClientWaitForCompletion**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientwaitforcompletion)    | Si blocca fino al completamento della sessione multicast o al raggiungimento del timeout specificato.                                                                                  |



 

 

 




