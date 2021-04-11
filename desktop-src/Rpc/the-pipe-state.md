---
title: Stato della pipe
description: Sul server, il compilatore MIDL crea una variabile di stato che coordina le procedure push, pull e allocazione.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118055"
---
# <a name="the-pipe-state"></a><span data-ttu-id="b42f7-103">Stato della pipe</span><span class="sxs-lookup"><span data-stu-id="b42f7-103">The Pipe State</span></span>

<span data-ttu-id="b42f7-104">Sul server, il compilatore MIDL crea una variabile di *stato* che coordina le procedure push, pull e allocazione.</span><span class="sxs-lookup"><span data-stu-id="b42f7-104">On the server, the MIDL compiler creates a *state* variable that coordinates push, pull, and alloc procedures.</span></span> <span data-ttu-id="b42f7-105">Sul lato client, lo sviluppatore deve creare la variabile di *stato* .</span><span class="sxs-lookup"><span data-stu-id="b42f7-105">On the client side, the developer must create the *state* variable.</span></span> <span data-ttu-id="b42f7-106">La variabile di *stato* è quindi locale a entrambi i lati, ovvero il client e il server mantengono il proprio stato di pipe.</span><span class="sxs-lookup"><span data-stu-id="b42f7-106">Therefore, the *state* variable is local to both sides—that is, the client and server each maintain their own pipe state.</span></span> <span data-ttu-id="b42f7-107">Il codice stub del server mantiene la variabile di stato nel server.</span><span class="sxs-lookup"><span data-stu-id="b42f7-107">The server stub code maintains the state variable on the server.</span></span> <span data-ttu-id="b42f7-108">Non tentare di modificare direttamente il contenuto.</span><span class="sxs-lookup"><span data-stu-id="b42f7-108">You should not attempt to modify its contents directly.</span></span> <span data-ttu-id="b42f7-109">Il client deve inizializzare i campi nella struttura del controllo pipe e mantenerne la variabile di *stato* .</span><span class="sxs-lookup"><span data-stu-id="b42f7-109">The client must initialize the fields in the pipe control structure and maintain its *state* variable.</span></span> <span data-ttu-id="b42f7-110">Usa la variabile di *stato* per identificare dove individuare o inserire i dati.</span><span class="sxs-lookup"><span data-stu-id="b42f7-110">It uses the *state* variable to identify where to locate or place data.</span></span>

<span data-ttu-id="b42f7-111">La variabile di *stato* del client può essere semplice come un handle di file, se si trasferiscono dati da un file a un altro.</span><span class="sxs-lookup"><span data-stu-id="b42f7-111">The client *state* variable can be as simple as a file handle, if you are transferring data from one file to another.</span></span> <span data-ttu-id="b42f7-112">Può anche essere un numero intero che punta a un elemento in una matrice.</span><span class="sxs-lookup"><span data-stu-id="b42f7-112">It can also be an integer that points to an element in an array.</span></span> <span data-ttu-id="b42f7-113">In alternativa, è possibile definire una struttura di stato piuttosto complessa per eseguire attività aggiuntive, ad esempio il coordinamento delle routine push e pull \[ [in un](/windows/desktop/Midl/in)parametro [out](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="b42f7-113">Or you can define a fairly complex state structure to perform additional tasks, such as coordinating the push and pull routines on an \[ [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl)\] parameter.</span></span>

 

 