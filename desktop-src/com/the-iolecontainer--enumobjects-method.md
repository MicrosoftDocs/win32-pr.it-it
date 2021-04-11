---
title: Metodo EnumObjects di IOleContainer
description: Metodo EnumObjects di IOleContainer
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221016"
---
# <a name="the-iolecontainerenumobjects-method"></a><span data-ttu-id="a3f16-103">Il metodo IOleContainer:: EnumObjects</span><span class="sxs-lookup"><span data-stu-id="a3f16-103">The IOleContainer::EnumObjects Method</span></span>

<span data-ttu-id="a3f16-104">Questo metodo viene utilizzato per enumerare tutti gli oggetti OLE contenuti in un documento o un form, restituendo un puntatore a interfaccia per ogni oggetto OLE.</span><span class="sxs-lookup"><span data-stu-id="a3f16-104">This method is used to enumerate over all the OLE objects contained in a document or form, returning an interface pointer for each OLE object.</span></span> <span data-ttu-id="a3f16-105">Il contenitore deve restituire puntatori a ogni oggetto OLE che condivide lo stesso contenitore.</span><span class="sxs-lookup"><span data-stu-id="a3f16-105">The container must return pointers to each OLE object that shares the same container.</span></span> <span data-ttu-id="a3f16-106">È necessario enumerare anche i form nidificati o i controlli annidati.</span><span class="sxs-lookup"><span data-stu-id="a3f16-106">Nested forms or nested controls must also be enumerated.</span></span>

<span data-ttu-id="a3f16-107">Alcuni contenitori implementano i controlli Extender, che consentono di eseguire il wrapping dei controlli non ActiveX, quindi restituiscono i puntatori a questi controlli Extender come un form enumerato.</span><span class="sxs-lookup"><span data-stu-id="a3f16-107">Some containers implement extender controls, which wrap non-ActiveX controls, and then return pointers to these extender controls as a form is enumerated.</span></span> <span data-ttu-id="a3f16-108">Questo comportamento consente ai controlli ActiveX e ai contenitori di controlli ActiveX di integrarsi correttamente con i controlli non ActiveX ed è quindi consigliabile, ma non obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a3f16-108">This behavior enables ActiveX controls and ActiveX control containers to integrate well with non-ActiveX controls, and is thus recommended, but not required.</span></span>

 

 




