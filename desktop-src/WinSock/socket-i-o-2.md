---
description: Uso di operazioni di I/O di blocco, I/O non di blocco con notifica asincrona di eventi di rete e I/O sovrapposto con indicazione di completamento in Windows Sockets 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: Socket I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162491d2cd840ed15e30f4d0aa9add7040807b148d16950fcb279e0984a26b54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993401"
---
# <a name="socket-io"></a>Socket I/O

Esistono tre modi principali per eseguire l'I/O in Windows Sockets 2:

-   Blocco dell'I/O.
-   I/O non di blocco insieme alla notifica asincrona degli eventi di rete.
-   I/O sovrapposto con indicazione di completamento.

Ogni metodo viene descritto nelle sezioni seguenti. L'I/O di blocco è il comportamento predefinito, la modalità non di blocco può essere usata in qualsiasi socket inserito in modalità non di blocco e l'I/O sovrapposto può verificarsi solo nei socket creati con l'attributo sovrapposto. È anche interessante notare che le due chiamate per l'invio: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) e le due chiamate per la ricezione: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) implementano ognuno tutti e tre i metodi di I/O. I provider di servizi determinano come eseguire l'operazione di I/O in base alle modalità socket, agli attributi e ai valori dei parametri di input.

 

 
