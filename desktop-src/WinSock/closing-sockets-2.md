---
description: WSPCloseSocket rilascia il descrittore del socket in modo che qualsiasi operazione in sospeso in qualsiasi thread dello stesso processo verrà interrotta e qualsiasi altro riferimento a esso avrà esito negativo.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Chiusura di socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc35b7ba401e43494d49815e17eca19bd25b0080a385c40813209037c858a456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051689"
---
# <a name="closing-sockets"></a>Chiusura di socket

[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) rilascia il descrittore del socket in modo che qualsiasi operazione in sospeso in qualsiasi thread dello stesso processo verrà interrotta e qualsiasi altro riferimento a esso avrà esito negativo. Si noti che è necessario utilizzare un conteggio dei riferimenti per i socket condivisi e solo se si tratta dell'ultimo riferimento a un socket sottostante, se le informazioni associate a questo socket devono essere rimosse, a condizione che la chiusura normalmente non sia richiesta (ovvero, DONTLINGER non è \_ impostato). Nel caso dell'impostazione di SO DONTLINGER, tutti i dati accodati per la trasmissione verranno inviati, se possibile, prima che vengano rilasciate le informazioni associate \_ al socket. Per **altre informazioni, vedere WSPCloseSocket.**

Per i provider di servizi nonIFS, È necessario richiamare [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) per rilasciare l'handle socket alla DLL Windows Sockets 2.

 

 
