---
title: Proprietà burnProgress di IWMPCdromBurn
description: La proprietà burnProgress ottiene lo stato di avanzamento del CD come percentuale di completamento.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- Finestra delle proprietà di burnProgress Media Player
- Proprietà di burnProgress Media Player Windows, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, proprietà burnProgress
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329669"
---
# <a name="iwmpcdromburnburnprogress-property"></a><span data-ttu-id="abb4b-106">Proprietà IWMPCdromBurn:: burnProgress</span><span class="sxs-lookup"><span data-stu-id="abb4b-106">IWMPCdromBurn::burnProgress property</span></span>

<span data-ttu-id="abb4b-107">La proprietà **burnProgress** ottiene lo stato di avanzamento del CD come percentuale di completamento.</span><span class="sxs-lookup"><span data-stu-id="abb4b-107">The **burnProgress** property gets the CD burning progress as percent complete.</span></span>

<span data-ttu-id="abb4b-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="abb4b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb4b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abb4b-109">Syntax</span></span>


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="abb4b-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="abb4b-110">Property value</span></span>

<span data-ttu-id="abb4b-111">**System. Int32** che rappresenta il valore di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="abb4b-111">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="abb4b-112">I valori di avanzamento sono compresi tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="abb4b-112">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="abb4b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="abb4b-113">Remarks</span></span>

<span data-ttu-id="abb4b-114">Il valore di avanzamento rappresenta la percentuale completa dell'intero processo di masterizzazione, incluse le operazioni di gestione temporanea.</span><span class="sxs-lookup"><span data-stu-id="abb4b-114">The progress value represents the completed percentage of the entire burning process, including any staging operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="abb4b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abb4b-115">Requirements</span></span>



| <span data-ttu-id="abb4b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="abb4b-116">Requirement</span></span> | <span data-ttu-id="abb4b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="abb4b-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb4b-118">Versione</span><span class="sxs-lookup"><span data-stu-id="abb4b-118">Version</span></span><br/>   | <span data-ttu-id="abb4b-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="abb4b-119">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="abb4b-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="abb4b-120">Namespace</span></span><br/> | <span data-ttu-id="abb4b-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="abb4b-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="abb4b-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="abb4b-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="abb4b-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="abb4b-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abb4b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abb4b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb4b-125">**Interfaccia IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="abb4b-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





