---
title: Proprietà SAMIStyleCount di IWMPClosedCaption2
description: La proprietà SAMIStyleCount ottiene il numero di stili supportati dal file SAMI corrente.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Finestra delle proprietà di SAMIStyleCount Media Player
- Proprietà di SAMIStyleCount Media Player Windows, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player, proprietà SAMIStyleCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff361b4c6d34f63e86e3d8458bff4d3308cae29f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332491"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a><span data-ttu-id="e0097-106">Proprietà IWMPClosedCaption2:: SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="e0097-106">IWMPClosedCaption2::SAMIStyleCount property</span></span>

<span data-ttu-id="e0097-107">La proprietà **SAMIStyleCount** ottiene il numero di stili supportati dal file Sami corrente.</span><span class="sxs-lookup"><span data-stu-id="e0097-107">The **SAMIStyleCount** property gets the number of styles supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0097-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0097-108">Syntax</span></span>


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e0097-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e0097-109">Property value</span></span>

<span data-ttu-id="e0097-110">**System. Int32** che rappresenta il numero di stili.</span><span class="sxs-lookup"><span data-stu-id="e0097-110">A **System.Int32** that is the number of styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0097-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0097-111">Remarks</span></span>

<span data-ttu-id="e0097-112">Questa proprietà restituisce 0, a meno che non sia aperto un file multimediale digitale (AxWindowsMediaPlayer. openState è uguale a 13).</span><span class="sxs-lookup"><span data-stu-id="e0097-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0097-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0097-113">Requirements</span></span>



| <span data-ttu-id="e0097-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0097-114">Requirement</span></span> | <span data-ttu-id="e0097-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e0097-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0097-116">Versione</span><span class="sxs-lookup"><span data-stu-id="e0097-116">Version</span></span><br/>   | <span data-ttu-id="e0097-117">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e0097-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e0097-118">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e0097-118">Namespace</span></span><br/> | <span data-ttu-id="e0097-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e0097-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e0097-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="e0097-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e0097-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e0097-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0097-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0097-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0097-123">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="e0097-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="e0097-124">**Interfaccia IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0097-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0097-125">**IWMPClosedCaption. SAMIStyle (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0097-125">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0097-126">**Interfaccia IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0097-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0097-127">**IWMPClosedCaption2. getSAMIStyleName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0097-127">**IWMPClosedCaption2.getSAMIStyleName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





