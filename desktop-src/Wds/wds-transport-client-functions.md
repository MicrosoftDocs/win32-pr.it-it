---
title: Funzioni client di trasporto WDS
description: Questo modulo definisce le strutture e le funzioni che compongono l'interfaccia tra il ricevitore di contenuto e il client di trasporto.
ms.assetid: 20c3116b-3a0d-4048-b6f2-81c03e0a80ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f228370aa0973e124b1877dcf8a458d1356170fbb872a05a1867ac0489c00a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680401"
---
# <a name="wds-transport-client-functions"></a>Funzioni client di trasporto WDS

Questo modulo definisce le strutture e le funzioni che compongono l'interfaccia tra il ricevitore di contenuto e il client di trasporto.



| Funzione                                                                              | Descrizione                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ WdsTransportClientReceiveContents*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivecontents) | Indica che un blocco di dati è pronto per l'uso.                                                                                                                         |
| [*PFN \_ WdsTransportClientReceiveMetadata*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivemetadata) | Riceve informazioni sui metadati su un file.                                                                                                                                 |
| [*PFN \_ WdsTransportClientSessionComplete*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessioncomplete) | Indica che la sessione è stata completata correttamente o si è verificato un errore.                                                                                                  |
| [*PFN \_ WdsTransportClientSessionStart*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstart)       | Indica le dimensioni del file e altre informazioni sul lato server relative al file al consumer.                                                                                   |
| [*PFN \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex)   | Indica le dimensioni del file e altre informazioni sul lato server relative al file al consumer.                                                                                   |
| [**WdsTransportClientAddRefBuffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientaddrefbuffer)              | Incrementa il conteggio dei riferimenti su un buffer di proprietà del client multicast.                                                                                                   |
| [**WdsTransportClientCancelSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcancelsession)            | Rilascia le risorse associate a una sessione nel client.                                                                                                             |
| [**WdsTransportClientCloseSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientclosesession)              | Rilascia le risorse associate a una sessione nel client.                                                                                                             |
| [**WdsTransportClientCompleteReceive**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcompletereceive)        | Indica che tutte le elaborazioni su un blocco di dati sono completate e che il client multicast può rimuovere questo blocco di dati dalla cache per fare spazio a ulteriori ricevimenti. |
| [**WdsTransportClientInitialize**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitialize)                  | Inizializza il client multicast.                                                                                                                                           |
| [**WdsTransportClientInitializeSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitializesession)    | Avvia un trasferimento di file multicast.                                                                                                                                        |
| [**WdsTransportClientQueryStatus**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientquerystatus)                | Recupera lo stato corrente di una trasmissione multicast in corso o completa dal client multicast.                                                                    |
| [**WdsTransportClientRegisterCallback**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientregistercallback)      | Registra un callback con il client multicast.                                                                                                                             |
| [**WdsTransportClientReleaseBuffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientreleasebuffer)            | Decrementa il conteggio dei riferimenti su un buffer di proprietà del client multicast.                                                                                                   |
| [**WdsTransportClientShutdown**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientshutdown)                      | Arresta il client multicast.                                                                                                                                            |
| [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession)              | Avvia un trasferimento di file multicast.                                                                                                                                        |
| [**WdsTransportClientWaitForCompletion**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientwaitforcompletion)    | Si blocca fino al completamento della sessione multicast o fino a quando non viene raggiunto il timeout specificato.                                                                                  |



 

 

 




