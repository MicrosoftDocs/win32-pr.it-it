---
description: Come accennato in precedenza, WSPJoinLeaf viene usato per unire un nodo foglia a una sessione multipoint.
ms.assetid: 03325f5e-4d4a-405b-b644-3d8c03435e17
title: Uso di WSPJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 057be0e2c1f2c3ffec21d64f3e95f6ad0ee584698e66f57cf4489ff6be887dc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121011"
---
# <a name="using-wspjoinleaf"></a>Uso di WSPJoinLeaf

Come accennato in [**precedenza, WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) viene usato per unire un nodo foglia a una sessione multipoint. **WSPJoinLeaf** ha gli stessi parametri e la stessa semantica di [**WSPConnect,**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) ad eccezione del fatto che restituisce un descrittore di socket (come in [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)) e ha un parametro *dwFlags* aggiuntivo. Il *parametro dwFlags* viene usato per indicare se il socket fungerà solo da mittente, solo come ricevitore o da entrambi. In questa funzione è possibile usare solo socket multipoint per i *parametri di* input. Se il socket multipoint è in modalità non di blocco, il descrittore del socket restituito non sarà utilizzabile fino a quando non viene ricevuta un'indicazione FD \_ CONNECT corrispondente. Un'applicazione radice in una sessione multipoint può chiamare **WSPJoinLeaf** una o più volte per aggiungere un numero di nodi foglia, ma al massimo una richiesta di connessione multipoint può essere in sospeso alla volta.

Il descrittore del socket restituito da [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) è diverso a seconda che il descrittore del socket di input, *s*, sia una radice c o una \_ foglia \_ c. Se usato con un socket radice c, il parametro name definisce un nodo foglia specifico da aggiungere e il descrittore del socket restituito è un socket foglia c corrispondente al nodo foglia \_ appena  \_ aggiunto. Non è progettato per essere usato per lo scambio di dati multipoint, ma viene usato per ricevere indicazioni di eventi di rete (ad esempio FD CLOSE) per la connessione esistente alla foglia \_ c \_ specifica. Alcune implementazioni multipoint possono anche consentire l'uso di questo socket per le chat laterali tra la radice e un singolo nodo foglia. Per questo socket deve essere specificata un'indicazione CLOSE FD se il nodo foglia corrispondente \_ chiama [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) per uscire dalla sessione multipoint. In modo simmetrico, se si richiama **WSPCloseSocket** sul socket foglia C restituito da \_ [**WSPJoinLeaf,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) il socket nel nodo foglia corrispondente riceverà la notifica FD \_ CLOSE.

Quando [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) viene richiamato con un socket foglia c, il parametro name contiene l'indirizzo dell'applicazione radice (per uno schema di controllo rooted) o di una sessione multipoint esistente (schema di controllo non rooted) e il descrittore del socket restituito è lo stesso del descrittore \_ del socket di input.  In uno schema di controllo rooted il client radice inserirà il socket radice c in modalità di ascolto \_ chiamando [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)). La notifica FD \_ ACCEPT standard verrà recapitata quando il nodo foglia richiede di unirsi alla sessione multipoint. Il client radice usa la funzione [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) consueta per riconoscere il nuovo nodo foglia. Il valore restituito da **WSPAccept** è anche un descrittore di socket foglia c esattamente come quelli \_ restituiti da **WSPJoinLeaf.** Per supportare schemi multipoint che consentono sia i join avviati dalla radice che i join foglia, è accettabile che un socket radice c già in modalità di ascolto sia usato come input per \_ **WSPJoinLeaf**.

Un client radice multipunto è in genere responsabile dell'smantellamento ordinato di una sessione multipoint. Un'applicazione di questo tipo può usare [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) o [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) in un socket radice c per fare in modo che tutti i socket foglia c associati, inclusi quelli restituiti da \_ \_ [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) e i socket foglia C corrispondenti nei nodi foglia remoti, otterrà la notifica \_ FD \_ CLOSE.

 

 
