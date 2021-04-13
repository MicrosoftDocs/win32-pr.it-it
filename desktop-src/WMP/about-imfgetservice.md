---
title: Informazioni su IMFGetService
description: Informazioni su IMFGetService
ms.assetid: c71b1362-a596-42e5-b894-f8a3c0e70140
keywords:
- Plug-in di Windows Media Player, interfacce
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- Plug-in DSP, interfacce
- interfacce, plug-in DSP
- Plug-in di Windows Media Player, interfaccia IMFGetService
- plug-in, interfaccia IMFGetService
- plug-in per l'elaborazione di segnali digitali, interfaccia IMFGetService
- Plug-in DSP, interfaccia IMFGetService
- Interfaccia IMFGetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235b616afe48db9ae772da1f1d74c4f7de1a74a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328668"
---
# <a name="about-imfgetservice"></a><span data-ttu-id="117f3-113">Informazioni su IMFGetService</span><span class="sxs-lookup"><span data-stu-id="117f3-113">About IMFGetService</span></span>

<span data-ttu-id="117f3-114">L'interfaccia **IMFGetService** è una delle interfacce che devono essere implementate da un plug-in DSP a doppia modalità.</span><span class="sxs-lookup"><span data-stu-id="117f3-114">The **IMFGetService** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="117f3-115">Dispone di un solo metodo, **GetService**.</span><span class="sxs-lookup"><span data-stu-id="117f3-115">It has only one method, **GetService**.</span></span> <span data-ttu-id="117f3-116">Un plug-in DSP implementa il metodo **GetService** in modo che i client possano ottenere i puntatori alle interfacce supportate dal plug-in quando il plug-in viene eseguito in modalità nativa nella pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="117f3-116">A DSP plug-in implements the **GetService** method so that clients can obtain pointers to the interfaces supported by the plug-in when the plug-in is running natively in the Media Foundation pipeline.</span></span>

 

 




