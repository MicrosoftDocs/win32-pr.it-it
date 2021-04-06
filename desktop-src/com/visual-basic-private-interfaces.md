---
title: Interfacce private Visual Basic
description: Interfacce private Visual Basic
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045360"
---
# <a name="visual-basic-private-interfaces"></a><span data-ttu-id="841a6-103">Interfacce private Visual Basic</span><span class="sxs-lookup"><span data-stu-id="841a6-103">Visual Basic Private Interfaces</span></span>

<span data-ttu-id="841a6-104">In questa sezione vengono identificate due interfacce implementate da Visual Basic per le categorie di componenti.</span><span class="sxs-lookup"><span data-stu-id="841a6-104">Two interfaces that are implemented by Visual Basic are identified here for component categories.</span></span> <span data-ttu-id="841a6-105">Non è previsto che i controlli richiedano queste categorie perché è possibile che i controlli offrano funzionalità alternative quando questi non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="841a6-105">It is not expected that controls should require these categories because it is possible for controls to offer alternative functionality when these are not available.</span></span>

<span data-ttu-id="841a6-106">L'interfaccia [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) consente ai controlli di integrarsi meglio nell'ambiente Visual Basic durante la formattazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="841a6-106">The [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) interface allows controls to better integrate into the Visual Basic environment when formatting data.</span></span>

<span data-ttu-id="841a6-107">CATId-{02496840-3AC4-11cf-87B9-00AA006C8166} CATId \_ VBFormat</span><span class="sxs-lookup"><span data-stu-id="841a6-107">CATID - {02496840-3AC4-11cf-87B9-00AA006C8166} CATID\_VBFormat</span></span>

<span data-ttu-id="841a6-108">L'interfaccia [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) consente a un controllo di enumerare altri controlli nel form VB.</span><span class="sxs-lookup"><span data-stu-id="841a6-108">The [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) interface allows a control to enumerate other controls on the VB form.</span></span>

<span data-ttu-id="841a6-109">CATId-{02496841-3AC4-11cf-87B9-00AA006C8166} CATId \_ VBGetControl</span><span class="sxs-lookup"><span data-stu-id="841a6-109">CATID - {02496841-3AC4-11cf-87B9-00AA006C8166} CATID\_VBGetControl</span></span>

<span data-ttu-id="841a6-110">Di seguito sono descritte due interfacce private aggiuntive, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) e [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), anche se non definiscono le categorie di componenti.</span><span class="sxs-lookup"><span data-stu-id="841a6-110">Two additional private interfaces, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) and [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), are described here even though they do not define component categories.</span></span> <span data-ttu-id="841a6-111">Non è consigliabile usare queste quattro interfacce perché non sono supportate da contenitori diversi da Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="841a6-111">Use of these four interfaces is not recommended because they are not supported by containers other than Visual Basic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="841a6-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="841a6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="841a6-113">Categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="841a6-113">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




