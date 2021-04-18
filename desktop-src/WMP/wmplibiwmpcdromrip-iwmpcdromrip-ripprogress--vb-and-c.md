---
title: Proprietà ripProgress di IWMPCdromRip
description: La proprietà ripProgress ottiene lo stato di ripping del CD come percentuale di completamento.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- Finestra delle proprietà di ripProgress Media Player
- Proprietà di ripProgress Media Player Windows, interfaccia IWMPCdromRip
- Interfaccia IWMPCdromRip Windows Media Player, proprietà ripProgress
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329288"
---
# <a name="iwmpcdromripripprogress-property"></a><span data-ttu-id="34ffd-106">Proprietà IWMPCdromRip:: ripProgress</span><span class="sxs-lookup"><span data-stu-id="34ffd-106">IWMPCdromRip::ripProgress property</span></span>

<span data-ttu-id="34ffd-107">La proprietà **ripProgress** ottiene lo stato di ripping del CD come percentuale di completamento.</span><span class="sxs-lookup"><span data-stu-id="34ffd-107">The **ripProgress** property gets the CD ripping progress as percent complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="34ffd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34ffd-108">Syntax</span></span>


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="34ffd-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="34ffd-109">Property value</span></span>

<span data-ttu-id="34ffd-110">**System. Int32** che rappresenta il valore di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="34ffd-110">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="34ffd-111">I valori di avanzamento sono compresi tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="34ffd-111">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="34ffd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="34ffd-112">Remarks</span></span>

<span data-ttu-id="34ffd-113">Il valore di avanzamento rappresenta la percentuale completa dell'intero processo di estrazione.</span><span class="sxs-lookup"><span data-stu-id="34ffd-113">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="34ffd-114">Per determinare lo stato di avanzamento di una traccia specifica, usare [IWMPMedia. GetItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) con **RipProgress** come nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="34ffd-114">To determine the progress of a specific track, use [IWMPMedia.getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) with **RipProgress** as the attribute name.</span></span> <span data-ttu-id="34ffd-115">Per ottenere l'indice della traccia attualmente in fase di ripping, chiamare IWMPPlaylist. getItemInfo con "CurrentRipTrackIndex" come nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="34ffd-115">To get the index of the track currently being ripped, call IWMPPlaylist.getItemInfo with "CurrentRipTrackIndex" as the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="34ffd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34ffd-116">Requirements</span></span>



| <span data-ttu-id="34ffd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="34ffd-117">Requirement</span></span> | <span data-ttu-id="34ffd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="34ffd-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34ffd-119">Versione</span><span class="sxs-lookup"><span data-stu-id="34ffd-119">Version</span></span><br/>   | <span data-ttu-id="34ffd-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="34ffd-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="34ffd-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="34ffd-121">Namespace</span></span><br/> | <span data-ttu-id="34ffd-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="34ffd-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="34ffd-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="34ffd-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="34ffd-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="34ffd-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34ffd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34ffd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34ffd-126">**Interfaccia IWMPCdromRip (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="34ffd-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="34ffd-127">**Copia di un CD**</span><span class="sxs-lookup"><span data-stu-id="34ffd-127">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





