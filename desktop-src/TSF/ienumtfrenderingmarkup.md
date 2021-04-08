---
title: Interfaccia IEnumTfRenderingMarkup
description: L'interfaccia IEnumTfRenderingMarkup viene implementata da TSF Manager e utilizzata dalle applicazioni. Questa interfaccia può essere recuperata da ITfContextRenderingMarkup GetRenderingMarkup ed enumera le informazioni di markup per il rendering.
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- Framework servizi di testo interfaccia IEnumTfRenderingMarkup
- Framework dei servizi di testo dell'interfaccia IEnumTfRenderingMarkup, descritto
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047155"
---
# <a name="ienumtfrenderingmarkup-interface"></a><span data-ttu-id="271a4-106">Interfaccia IEnumTfRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="271a4-106">IEnumTfRenderingMarkup interface</span></span>

<span data-ttu-id="271a4-107">L'interfaccia **IEnumTfRenderingMarkup** viene implementata da TSF Manager e utilizzata dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="271a4-107">The **IEnumTfRenderingMarkup** interface is implemented by TSF Manager and used by applications.</span></span> <span data-ttu-id="271a4-108">Questa interfaccia può essere recuperata da [ITfContextRenderingMarkup:: GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) ed enumera le informazioni di markup per il rendering.</span><span class="sxs-lookup"><span data-stu-id="271a4-108">This interface can be retrieved by [ITfContextRenderingMarkup::GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) and enumerates the rendering markup information.</span></span>



| <span data-ttu-id="271a4-109">Metodi IEnumTfRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="271a4-109">IEnumTfRenderingMarkup methods</span></span>            | <span data-ttu-id="271a4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="271a4-110">Description</span></span>                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="271a4-111">Clone</span><span class="sxs-lookup"><span data-stu-id="271a4-111">Clone</span></span>](ienumtfrenderingmarkup-clone.md) | <span data-ttu-id="271a4-112">Il metodo **IEnumTfRenderingMarkup:: Clone** crea una copia dell'oggetto enumeratore.</span><span class="sxs-lookup"><span data-stu-id="271a4-112">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>                                                                  |
| [<span data-ttu-id="271a4-113">Avanti</span><span class="sxs-lookup"><span data-stu-id="271a4-113">Next</span></span>](ienumtfrenderingmarkup-next.md)   | <span data-ttu-id="271a4-114">Il metodo **IEnumTfRenderingMarkup:: Next** ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="271a4-114">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |
| [<span data-ttu-id="271a4-115">Reimpostazione</span><span class="sxs-lookup"><span data-stu-id="271a4-115">Reset</span></span>](ienumtfrenderingmarkup-reset.md) | <span data-ttu-id="271a4-116">Il metodo **IEnumTfRenderingMarkup:: Reset** Reimposta l'oggetto enumeratore spostando la posizione corrente all'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="271a4-116">The **IEnumTfRenderingMarkup::Reset** method resets the enumerator object by moving the current position to the beginning of the enumeration sequence.</span></span> |
| [<span data-ttu-id="271a4-117">Skip</span><span class="sxs-lookup"><span data-stu-id="271a4-117">Skip</span></span>](ienumtfrenderingmarkup-skip.md)   | <span data-ttu-id="271a4-118">Il metodo **IEnumTfRenderingMarkup:: Skip** ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="271a4-118">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |



 

## <a name="members"></a><span data-ttu-id="271a4-119">Membri</span><span class="sxs-lookup"><span data-stu-id="271a4-119">Members</span></span>

<span data-ttu-id="271a4-120">L'interfaccia **IEnumTfRenderingMarkup** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="271a4-120">The **IEnumTfRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="271a4-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="271a4-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="271a4-122">Questa interfaccia non è attualmente presente nei file di intestazione pubblici.</span><span class="sxs-lookup"><span data-stu-id="271a4-122">This interface is not currently in the public header files.</span></span> <span data-ttu-id="271a4-123">Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="271a4-123">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 