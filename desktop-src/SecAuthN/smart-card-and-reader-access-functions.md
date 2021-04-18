---
description: Connettersi e comunicare con una smart card specifica.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Funzioni di accesso con smart card e lettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316232"
---
# <a name="smart-card-and-reader-access-functions"></a>Funzioni di accesso con smart card e lettore

Le funzioni seguenti si connettono e comunicano con una [*Smart Card*](../secgloss/s-gly.md)specifica. Le operazioni di i/O nella scheda utilizzano un buffer per l'invio o la ricezione di dati e una struttura contenente informazioni sul controllo del protocollo. La struttura delle informazioni di controllo del protocollo inizia sempre con una struttura di [**\_ \_ richiesta**](scard-io-request.md) di i/o spaventata.



| Argomento                                                  | Descrizione                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | Connettersi a una scheda.                                                                                                                                                                                                                         |
| [**SCardReconnect**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | Ristabilire una connessione.                                                                                                                                                                                                                  |
| [**SCardDisconnect**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | Terminare una connessione.                                                                                                                                                                                                                    |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | Avviare una [*transazione*](../secgloss/t-gly.md), impedendo ad altre applicazioni di accedere a una scheda.                                                                                            |
| [**SCardEndTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | Terminare una transazione, consentendo ad altre applicazioni di accedere a una scheda.                                                                                                                                                                           |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | Consente di specificare lo stato corrente del lettore.                                                                                                                                                                                                  |
| [**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | Richiede il servizio e riceve i dati da una scheda usando [*T = 0*](../secgloss/t-gly.md), [*T = 1*](../secgloss/t-gly.md)e i protocolli non elaborati. |



 

 

 
