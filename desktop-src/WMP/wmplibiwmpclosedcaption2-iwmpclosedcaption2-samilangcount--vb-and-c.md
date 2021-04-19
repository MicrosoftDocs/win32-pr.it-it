---
title: Proprietà SAMILangCount di IWMPClosedCaption2
description: La proprietà SAMILangCount ottiene il numero di lingue supportate dal file SAMI corrente.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Finestra delle proprietà di SAMILangCount Media Player
- Proprietà di SAMILangCount Media Player Windows, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player, proprietà SAMILangCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea01357de508dea319389cd14ab85ebafe0329e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332493"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a><span data-ttu-id="0d588-106">Proprietà IWMPClosedCaption2:: SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="0d588-106">IWMPClosedCaption2::SAMILangCount property</span></span>

<span data-ttu-id="0d588-107">La proprietà **SAMILangCount** ottiene il numero di lingue supportate dal file Sami corrente.</span><span class="sxs-lookup"><span data-stu-id="0d588-107">The **SAMILangCount** property gets the number of languages supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d588-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d588-108">Syntax</span></span>


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="0d588-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0d588-109">Property value</span></span>

<span data-ttu-id="0d588-110">**System. Int32** che rappresenta il numero di lingue supportate.</span><span class="sxs-lookup"><span data-stu-id="0d588-110">A **System.Int32** that is the number of languages supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d588-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d588-111">Remarks</span></span>

<span data-ttu-id="0d588-112">Questa proprietà restituisce 0, a meno che non sia aperto un file multimediale digitale (AxWindowsMediaPlayer. openState è uguale a 13).</span><span class="sxs-lookup"><span data-stu-id="0d588-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d588-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d588-113">Requirements</span></span>



| <span data-ttu-id="0d588-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d588-114">Requirement</span></span> | <span data-ttu-id="0d588-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0d588-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d588-116">Versione</span><span class="sxs-lookup"><span data-stu-id="0d588-116">Version</span></span><br/>   | <span data-ttu-id="0d588-117">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="0d588-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0d588-118">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d588-118">Namespace</span></span><br/> | <span data-ttu-id="0d588-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0d588-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0d588-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="0d588-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0d588-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0d588-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d588-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d588-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d588-123">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="0d588-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="0d588-124">**Interfaccia IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0d588-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d588-125">**IWMPClosedCaption. SAMILang (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0d588-125">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d588-126">**Interfaccia IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0d588-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d588-127">**IWMPClosedCaption2. getSAMILangName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0d588-127">**IWMPClosedCaption2.getSAMILangName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





