---
description: Pseudoblocking operazioni pseudo-blocco in Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo-blocco e vero blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309943"
---
# <a name="pseudo-blocking-and-true-blocking"></a>Pseudo-blocco e vero blocco

In 16 ambienti Windows il blocco effettivo non è supportato dal sistema operativo. Pertanto, un'operazione di blocco che non può essere completata immediatamente viene gestita come segue:

-   Il provider di servizi avvia l'operazione e quindi immette un ciclo durante il quale invia tutti i messaggi di Windows (cedendo il processore a un altro thread, se necessario)
-   Viene quindi verificato il completamento della funzione Windows Sockets.
-   Se la funzione è stata completata o se [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) è stato richiamato, il ciclo viene terminato e la funzione di blocco viene completata con un risultato appropriato.

Questo è ciò che si intende con il termine pseudo-blocco e il ciclo a cui si fa riferimento è noto come hook di blocco predefinito.

 

 
