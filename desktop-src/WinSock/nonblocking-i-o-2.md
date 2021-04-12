---
description: Se un socket si trova in modalità non di blocco, tutte le operazioni di I/O devono essere completate immediatamente o restituire il codice di errore WSAEWOULDBLOCK che indica che l'operazione non può essere completata immediatamente.
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: Input/output non di blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526130"
---
# <a name="nonblocking-inputoutput"></a><span data-ttu-id="039ac-103">Input/output non di blocco</span><span class="sxs-lookup"><span data-stu-id="039ac-103">Nonblocking Input/Output</span></span>

<span data-ttu-id="039ac-104">Se un socket si trova in modalità non di blocco, tutte le operazioni di I/O devono essere completate immediatamente o restituire il codice di errore WSAEWOULDBLOCK che indica che l'operazione non può essere completata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="039ac-104">If a socket is in nonblocking mode, any I/O operation must either complete immediately or return the error code WSAEWOULDBLOCK indicating that the operation cannot be finished right away.</span></span> <span data-ttu-id="039ac-105">Nel secondo caso, è necessario un meccanismo per individuare quando è opportuno riprovare a eseguire l'operazione con la previsione che l'operazione avrà esito positivo.</span><span class="sxs-lookup"><span data-stu-id="039ac-105">In the latter case, a mechanism is needed to discover when it is appropriate to try the operation again with the expectation that the operation will succeed.</span></span> <span data-ttu-id="039ac-106">A questo scopo è stato definito un set di eventi di rete.</span><span class="sxs-lookup"><span data-stu-id="039ac-106">A set of network events has been defined for this purpose.</span></span> <span data-ttu-id="039ac-107">È possibile eseguire il polling o l'attesa di questi eventi tramite [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))oppure è possibile registrarli per il recapito asincrono chiamando [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) o [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="039ac-107">These events can be polled or waited on by using [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), or they can be registered for asynchronous delivery by calling [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) or [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="039ac-108">Per ulteriori informazioni, vedere [notifica degli eventi di rete](notification-of-network-events-2.md) .</span><span class="sxs-lookup"><span data-stu-id="039ac-108">See [Notification of Network Events](notification-of-network-events-2.md) for more information.</span></span>

 

 
