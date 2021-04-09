---
description: Utilizzo di I/o di blocco, I/o non di blocco con notifica asincrona degli eventi di rete e I/O sovrapposti con indicazione di completamento in Windows Sockets 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: I/O socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efcd325a0a379671dd39709f37e2c6d2133ca27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129118"
---
# <a name="socket-io"></a>I/O socket

Esistono tre modi principali per eseguire operazioni di I/O in Windows Sockets 2:

-   Blocco di I/O.
-   I/O non di blocco insieme alla notifica asincrona degli eventi di rete.
-   I/O sovrapposto con indicazione di completamento.

Ogni metodo viene descritto nelle sezioni seguenti. L'I/O di blocco è il comportamento predefinito. è possibile utilizzare la modalità non di blocco in qualsiasi socket inserito in modalità non di blocco e I/O sovrapposti possono essere eseguiti solo su socket creati con l'attributo Overlapped. È anche interessante notare che le due chiamate per l'invio di: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) e le due chiamate per la ricezione di: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) implementano ogni tre metodi di i/O. I provider di servizi stabiliscono come eseguire l'operazione di I/O in base alle modalità socket, agli attributi e ai valori dei parametri di input.

 

 
