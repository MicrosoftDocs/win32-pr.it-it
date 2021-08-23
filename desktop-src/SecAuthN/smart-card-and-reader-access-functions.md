---
description: Connessione e comunicare con una specifica smart card.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Funzioni di accesso smart card e lettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b571764ae2d31865082e823996e8cc1ecde9d9d3e2dd618f28e528fd465a567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917956"
---
# <a name="smart-card-and-reader-access-functions"></a>Funzioni di accesso smart card e lettore

Le funzioni seguenti si connettono a e comunicano con [*un*](../secgloss/s-gly.md)smart card . Le operazioni di I/O sulla scheda usano un buffer per l'invio o la ricezione di dati e una struttura che contiene informazioni sul controllo del protocollo. La struttura delle informazioni di controllo del protocollo inizia sempre con [**una struttura \_ SCARD IO \_ REQUEST.**](scard-io-request.md)



| Argomento                                                  | Descrizione                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | Connessione a una scheda.                                                                                                                                                                                                                         |
| [**SCardReconnect**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | Ristabilire una connessione.                                                                                                                                                                                                                  |
| [**SCardDisconnect**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | Terminare una connessione.                                                                                                                                                                                                                    |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | Avviare una [*transazione*](../secgloss/t-gly.md), bloccando l'accesso di altre applicazioni a una scheda.                                                                                            |
| [**Scardendtransaction**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | Terminare una transazione, consentendo ad altre applicazioni di accedere a una scheda.                                                                                                                                                                           |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | Specificare lo stato corrente del lettore.                                                                                                                                                                                                  |
| [**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | Richiede il servizio e riceve i dati da una scheda usando [*T=0,*](../secgloss/t-gly.md) [*T=1*](../secgloss/t-gly.md)e protocolli non elaborati. |



 

 

 
