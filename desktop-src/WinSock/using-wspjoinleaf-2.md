---
description: Come indicato in precedenza, WSPJoinLeaf viene usato per aggiungere un nodo foglia a una sessione multipoint.
ms.assetid: 03325f5e-4d4a-405b-b644-3d8c03435e17
title: Uso di WSPJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4426c0d22657b26dcc2217d856865d9ebe98db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226077"
---
# <a name="using-wspjoinleaf"></a>Uso di WSPJoinLeaf

Come indicato in precedenza, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) viene usato per aggiungere un nodo foglia a una sessione multipoint. **WSPJoinLeaf** presenta gli stessi parametri e la stessa semantica di [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , ad eccezione del fatto che restituisce un descrittore di socket (come in [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)) ed è dotato di un parametro *dwFlags* aggiuntivo. Il parametro *dwFlags* viene utilizzato per indicare se il socket fungerà solo da mittente, solo come ricevitore o entrambi. Solo i socket multipoint possono essere utilizzati per *i* parametri di input in questa funzione. Se il socket multipoint è in modalità non di blocco, il descrittore di socket restituito non sarà utilizzabile fino a quando non viene ricevuta un'indicazione di connessione FD corrispondente \_ . Un'applicazione radice in una sessione MultiPoint può chiamare **WSPJoinLeaf** una o più volte per aggiungere un numero di nodi foglia, ma al massimo una richiesta di connessione multipoint potrebbe essere in attesa alla volta.

Il descrittore di socket restituito da [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) è diverso a seconda che il descrittore di socket di input, *s*, sia una \_ radice c o una \_ foglia c. Quando viene usato con un \_ socket radice c, il parametro *Name* designa un particolare nodo foglia da aggiungere e il descrittore di socket restituito è un \_ socket foglia c corrispondente al nodo foglia appena aggiunto. Non è destinato a essere utilizzato per lo scambio di dati MultiPoint, ma viene invece utilizzato per ricevere le indicazioni relative agli eventi di rete (ad esempio, FD \_ Close) per la connessione esistente alla foglia c particolare \_ . Alcune implementazioni multipoint possono anche consentire l'uso di questo socket per le chat laterali tra la radice e un singolo nodo foglia. \_È necessario assegnare un'indicazione di chiusura FD per questo socket se il nodo foglia corrispondente chiama [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) per eliminare la sessione multipoint. In modo simmetrico, richiamando **WSPCloseSocket** sul \_ socket foglia c restituito da [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) , il socket nel nodo foglia corrispondente otterrà la notifica di \_ chiusura FD.

Quando [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) viene richiamato con un \_ socket foglia c, il parametro *Name* contiene l'indirizzo dell'applicazione radice (per uno schema di controllo radice) o una sessione multipoint esistente (schema di controllo non radice) e il descrittore di socket restituito è uguale al descrittore di socket di input. In uno schema di controllo con radice, il client radice inserisce il relativo \_ socket radice c in modalità di ascolto chiamando [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)). La notifica di \_ accettazione FD standard verrà recapitata quando il nodo foglia richiede di aggiungersi alla sessione multipoint. Il client radice usa la consueta funzione [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) per ammettere il nuovo nodo foglia. Il valore restituito da **WSPAccept** è anche un \_ descrittore di socket foglia c analogo a quello restituito da **WSPJoinLeaf**. Per supportare gli schemi multipoint che consentono sia i join avviati dalla radice che quelli avviati da foglia, è accettabile che un \_ socket radice c sia già in modalità di ascolto da usare come input per **WSPJoinLeaf**.

Un client radice multipoint è in genere responsabile della rimozione ordinata di una sessione multipoint. Un'applicazione di questo tipo può usare [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) o [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) in un socket radice c per fare in modo che \_ tutti i \_ socket foglia c associati, inclusi quelli restituiti da [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) e i socket foglia c corrispondenti \_ nei nodi foglia remoti, per ottenere la \_ notifica di chiusura FD.

 

 
