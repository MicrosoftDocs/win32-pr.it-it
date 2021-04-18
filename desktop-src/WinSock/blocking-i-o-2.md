---
description: La forma più semplice di I/O in Windows Sockets 2 è il blocco di I/O.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Blocco di input/output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307040"
---
# <a name="blocking-inputoutput"></a><span data-ttu-id="3e968-103">Blocco di input/output</span><span class="sxs-lookup"><span data-stu-id="3e968-103">Blocking Input/Output</span></span>

<span data-ttu-id="3e968-104">La forma più semplice di I/O in Windows Sockets 2 è il blocco di I/O.</span><span class="sxs-lookup"><span data-stu-id="3e968-104">The simplest form of I/O in Windows Sockets 2 is blocking I/O.</span></span> <span data-ttu-id="3e968-105">Come indicato nelle [modalità e nei flag dell'attributo socket](socket-attribute-flags-and-modes-2.md), per impostazione predefinita i socket vengono creati in modalità di blocco.</span><span class="sxs-lookup"><span data-stu-id="3e968-105">As mentioned in [Socket Attribute Flags and Modes](socket-attribute-flags-and-modes-2.md), sockets are created in blocking mode by default.</span></span> <span data-ttu-id="3e968-106">Qualsiasi operazione di I/O con un socket di blocco non verrà restituita finché l'operazione non è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="3e968-106">Any I/O operation with a blocking socket will not return until the operation has been fully completed.</span></span> <span data-ttu-id="3e968-107">Pertanto, qualsiasi thread può eseguire solo un'operazione di I/O alla volta.</span><span class="sxs-lookup"><span data-stu-id="3e968-107">Thus, any thread can only execute one I/O operation at a time.</span></span> <span data-ttu-id="3e968-108">Se, ad esempio, un thread esegue un'operazione di ricezione e nessun dato è attualmente disponibile, il thread si bloccherà fino a quando i dati non diventano disponibili e vengono inseriti nel buffer del thread.</span><span class="sxs-lookup"><span data-stu-id="3e968-108">For example, if a thread issues a receive operation and no data is currently available, the thread will block until data becomes available and is placed into the thread's buffer.</span></span> <span data-ttu-id="3e968-109">Sebbene questo sia semplice, non è necessariamente il modo più efficiente per eseguire operazioni di I/O (vedere [pseudo-blocco e vero blocco](pseudo-vs--true-blocking-2.md) per altre informazioni).</span><span class="sxs-lookup"><span data-stu-id="3e968-109">Although this is simple, it is not necessarily the most efficient way to do I/O (see [Pseudo Blocking and True Blocking](pseudo-vs--true-blocking-2.md) for more information).</span></span>

 

 



