---
title: D1104 Possibile perdita
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: La factory è stata rilasciata ma l'interfaccia creata da essa è ancora attiva. Anche se è valido rilasciare le risorse dopo il rilascio della factory, questa condizione potrebbe essere indicativa di una perdita di memoria.
keywords:
- D1104 Possibile perdita Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b6629a0da2b89e13feebc33fe5742e3459fc082b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548676"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="fd1fe-105">D1104: possibile perdita</span><span class="sxs-lookup"><span data-stu-id="fd1fe-105">D1104: Possible Leak</span></span>

<span data-ttu-id="fd1fe-106">La factory \[ *factory è* \] stata rilasciata, ma l'interfaccia creata da essa è ancora \[  \] attiva.</span><span class="sxs-lookup"><span data-stu-id="fd1fe-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="fd1fe-107">Anche se è valido rilasciare le risorse dopo il rilascio della factory, questa condizione potrebbe essere indicativa di una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="fd1fe-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="fd1fe-108">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="fd1fe-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="fd1fe-109"><span id="factory"></span><span id="FACTORY"></span>*Fabbrica*</span><span class="sxs-lookup"><span data-stu-id="fd1fe-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="fd1fe-110">Indirizzo della factory rilasciata.</span><span class="sxs-lookup"><span data-stu-id="fd1fe-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="fd1fe-111"><span id="interface"></span><span id="INTERFACE"></span>*Interfaccia*</span><span class="sxs-lookup"><span data-stu-id="fd1fe-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="fd1fe-112">Indirizzo dell'interfaccia creata nella *factory*.</span><span class="sxs-lookup"><span data-stu-id="fd1fe-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| <span data-ttu-id="fd1fe-113">Livello di errore</span><span class="sxs-lookup"><span data-stu-id="fd1fe-113">Error Level</span></span> | <span data-ttu-id="fd1fe-114">Informazioni</span><span class="sxs-lookup"><span data-stu-id="fd1fe-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="fd1fe-115">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="fd1fe-115">Possible Causes</span></span>

<span data-ttu-id="fd1fe-116">La factory è stata rilasciata ma l'interfaccia creata da essa è ancora attiva.</span><span class="sxs-lookup"><span data-stu-id="fd1fe-116">The factory was released but the interface created from it is still alive.</span></span>

 

 




