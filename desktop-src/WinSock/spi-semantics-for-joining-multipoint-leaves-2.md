---
description: Nell'esempio seguente un socket multipoint è spesso caratterizzato dalla descrizione del ruolo in uno dei due piani (controllo o dati).
ms.assetid: 35e4a8c9-d943-44b8-be61-605b60a6cf5d
title: Semantica SPI per l'Unione di foglie multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0e77203e5405f6cb820baba5d545de03e3a8ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313692"
---
# <a name="spi-semantics-for-joining-multipoint-leaves"></a>Semantica SPI per l'Unione di foglie multipoint

Nell'esempio seguente un socket multipoint è spesso caratterizzato dalla descrizione del ruolo in uno dei due piani (controllo o dati). Si noti che lo stesso socket ha un ruolo nell'altro piano, ma questo non è indicato per tenere i riferimenti brevi. Ad esempio, un riferimento a un \_ socket radice c può fare riferimento a una radice c \_ /d \_ o a un \_ socket foglia radice c/d \_ .

Negli schemi del piano di controllo rooted i nuovi nodi foglia vengono aggiunti a una sessione multipoint in uno o in due modi diversi. Nel primo metodo, la radice USA [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) per avviare una connessione con un nodo foglia e invitarla a diventare un partecipante. Sul nodo foglia, l'applicazione peer deve avere creato un \_ socket foglia c e usato [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) per impostarlo in modalità di ascolto. Il nodo foglia riceverà un' \_ indicazione di accettazione FD quando viene invitato per partecipare alla sessione e segnala la volontà di partecipare chiamando [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept). \_Quando l'operazione di join è stata completata, l'applicazione radice riceverà un'indicazione di connessione FD.

Nel secondo metodo, i ruoli sono essenzialmente invertiti. Il client radice crea un \_ socket radice c e lo imposta in modalità ascolto. Un nodo foglia che desidera partecipare alla sessione crea un \_ socket foglia c e USA [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) per avviare la connessione e richiedere l'ammissione. Il client radice riceve l' \_ accettazione FD quando arriva una richiesta di ammissione in ingresso e ammette il nodo foglia chiamando [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept). Il nodo foglia riceve la \_ connessione FD quando è stata accettata.

In un piano di controllo non radice, in cui tutti i nodi sono \_ foglia c, viene usata la funzione [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) per avviare l'inclusione di un nodo in una sessione multipoint esistente. \_Quando il join è stato completato e il descrittore di socket restituito è utilizzabile nella sessione MultiPoint, viene fornita un'indicazione di connessione FD. Nel caso del multicast IP, questo corrisponderebbe all'opzione del socket di aggiunta dell'indirizzo IP \_ \_ .

Esistono, quindi, tre istanze in cui un client usa [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf):

-   Fungere da radice multipoint e invitare una nuova foglia a partecipare alla sessione.
-   Fungendo da foglia che effettua una richiesta di ammissione a una sessione multipoint radice.
-   Fungendo da foglia che cerca l'ammissione a una sessione MultiPoint non radice (ad esempio, multicast IP).

 

 
