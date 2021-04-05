---
title: D1104 possibile perdita
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: La Factory è stata rilasciata, ma l'interfaccia creata è ancora attiva. Sebbene sia possibile rilasciare le risorse dopo aver rilasciato la Factory, questa condizione potrebbe essere indicativa di una perdita di memoria.
keywords:
- D1104 possibile perdita di Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 71ccbee152d60a73fbea5ebac2a1074534b69c3a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333556"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="8cc17-105">D1104: possibile perdita</span><span class="sxs-lookup"><span data-stu-id="8cc17-105">D1104: Possible Leak</span></span>

<span data-ttu-id="8cc17-106">Factory factory \[ *è* \] stata rilasciata, ma l' \[ *interfaccia* \] di interfaccia creata da essa è ancora attiva.</span><span class="sxs-lookup"><span data-stu-id="8cc17-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="8cc17-107">Sebbene sia possibile rilasciare le risorse dopo aver rilasciato la Factory, questa condizione potrebbe essere indicativa di una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="8cc17-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="8cc17-108">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="8cc17-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="8cc17-109"><span id="factory"></span><span id="FACTORY"></span>*fabbrica*</span><span class="sxs-lookup"><span data-stu-id="8cc17-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="8cc17-110">Indirizzo della Factory rilasciata.</span><span class="sxs-lookup"><span data-stu-id="8cc17-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="8cc17-111"><span id="interface"></span><span id="INTERFACE"></span>*interfaccia*</span><span class="sxs-lookup"><span data-stu-id="8cc17-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="8cc17-112">Indirizzo dell'interfaccia creata nella *Factory*.</span><span class="sxs-lookup"><span data-stu-id="8cc17-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

|             |             |
|-------------|-------------|
| <span data-ttu-id="8cc17-113">Livello di errore</span><span class="sxs-lookup"><span data-stu-id="8cc17-113">Error Level</span></span> | <span data-ttu-id="8cc17-114">Informazioni</span><span class="sxs-lookup"><span data-stu-id="8cc17-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="8cc17-115">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="8cc17-115">Possible Causes</span></span>

<span data-ttu-id="8cc17-116">La Factory è stata rilasciata, ma l'interfaccia creata è ancora attiva.</span><span class="sxs-lookup"><span data-stu-id="8cc17-116">The factory was released but the interface created from it is still alive.</span></span>

 

 




