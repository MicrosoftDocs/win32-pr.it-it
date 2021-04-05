---
title: Esecuzione di una chiamata di procedura remota
description: Quando il programma client di applicazioni distribuite che utilizza handle di binding espliciti dispone di un handle di binding, può eseguire le procedure remote.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- RPC (Remote Procedure Call), attività, esecuzione di una chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97095d7eda8227f2369f5e3776faf8ce04c22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707183"
---
# <a name="making-a-remote-procedure-call"></a><span data-ttu-id="21077-104">Esecuzione di una chiamata di procedura remota</span><span class="sxs-lookup"><span data-stu-id="21077-104">Making a Remote Procedure Call</span></span>

<span data-ttu-id="21077-105">Quando il programma client di applicazioni distribuite che utilizza handle di binding espliciti dispone di un handle di binding, può eseguire le procedure remote.</span><span class="sxs-lookup"><span data-stu-id="21077-105">Once the client program of distributed applications that uses explicit binding handles has a binding handle, it can execute remote procedures.</span></span>

<span data-ttu-id="21077-106">Microsoft RPC offre anche handle di binding personalizzati, handle di binding impliciti e handle di binding automatici.</span><span class="sxs-lookup"><span data-stu-id="21077-106">Microsoft RPC also offers custom binding handles, implicit binding handles, and automatic binding handles.</span></span> <span data-ttu-id="21077-107">Questi handle di associazione offrono ai programmi client e server diversi livelli di controllo sul processo di esecuzione di procedure remote.</span><span class="sxs-lookup"><span data-stu-id="21077-107">These binding handles offer client and server programs different levels of control over the process of executing remote procedures.</span></span> <span data-ttu-id="21077-108">Per informazioni dettagliate sui diversi tipi di handle e sulla flessibilità offerta, vedere [Binding e handle](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="21077-108">For details on different handle types and the flexibility they offer, see [Binding and Handles](binding-and-handles.md).</span></span>

<span data-ttu-id="21077-109">Per eseguire la chiamata di procedura in modalità remota, chiamare la funzione Stub lato client nello stesso modo in cui viene chiamata la funzione C.</span><span class="sxs-lookup"><span data-stu-id="21077-109">To execute the procedure call remotely, call the client-side stub function in the same manner any C function is called.</span></span>

 

 




