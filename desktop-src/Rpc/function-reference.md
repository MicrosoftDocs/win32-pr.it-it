---
title: Riferimento di funzione
description: In questa sezione vengono documentate le funzioni di runtime RPC (Remote Procedure Call) supportate in Microsoft RPC.
ms.assetid: 135bef8d-1794-420e-a111-604d02dbcc06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163c68f56a483d3eb7f62596c4a3d78ba2b5774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471318"
---
# <a name="function-reference"></a><span data-ttu-id="ecd81-103">Riferimento di funzione</span><span class="sxs-lookup"><span data-stu-id="ecd81-103">Function Reference</span></span>

<span data-ttu-id="ecd81-104">In questa sezione vengono documentate le funzioni di runtime RPC (Remote Procedure Call) supportate in Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="ecd81-104">This section documents the Remote Procedure Call (RPC) run-time functions supported in Microsoft RPC.</span></span> <span data-ttu-id="ecd81-105">Questa sezione descrive lo scopo, la sintassi, i parametri di input e i valori restituiti di ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="ecd81-105">This section describes each function's purpose, syntax, input parameters, and return values.</span></span> <span data-ttu-id="ecd81-106">Vengono inoltre fornite informazioni aggiuntive per l'utilizzo di funzioni RPC in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ecd81-106">It also provides additional information to help you use RPC functions in an application.</span></span>

<span data-ttu-id="ecd81-107">Tutti i puntatori passati alle funzioni RPC devono includere l'attributo **\_ \_ RPC \_ Lung** .</span><span class="sxs-lookup"><span data-stu-id="ecd81-107">All pointers passed to RPC functions must include the **\_ \_RPC\_FAR** attribute.</span></span> <span data-ttu-id="ecd81-108">Ad esempio, l' **\_ \_ handle \* di binding RPC** del puntatore diventa un handle di binding RPC **\_ \_ \_ \_ \_ \*** **\* \***  **\_ \_ \_ \* \_ Lung e char \_ \_ ptr diventa un oggetto RPC Lung Lung lung. \***</span><span class="sxs-lookup"><span data-stu-id="ecd81-108">For example, the pointer **RPC\_BINDING\_HANDLE \*** becomes **RPC\_BINDING\_HANDLE \_ \_RPC\_FAR \*** and **char \* \*** *Ptr* becomes **char \_ \_RPC\_FAR \* \_ \_RPC\_FAR \*** *Ptr*.</span></span>

<span data-ttu-id="ecd81-109">In questa sezione vengono illustrati i riferimenti alle funzioni nei gruppi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecd81-109">This section presents the function references in the following groups:</span></span>

-   [<span data-ttu-id="ecd81-110">Funzioni RPC</span><span class="sxs-lookup"><span data-stu-id="ecd81-110">RPC Functions</span></span>](rpc-functions.md)
-   [<span data-ttu-id="ecd81-111">Callback RPC e funzioni di notifica</span><span class="sxs-lookup"><span data-stu-id="ecd81-111">RPC Callback and Notification Functions</span></span>](rpc-callback-and-notification-functions.md)

 

 




