---
title: Proprietà audioLanguageCount di IWMPControls3
description: La proprietà audioLanguageCount ottiene il conteggio delle lingue audio supportate.
ms.assetid: 92e2093f-435b-4427-9f85-8c8ae76e0e2d
keywords:
- Finestra delle proprietà di audioLanguageCount Media Player
- Proprietà di audioLanguageCount Media Player Windows, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, proprietà audioLanguageCount
topic_type:
- apiref
api_name:
- IWMPControls3.audioLanguageCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd397dec80a5ccb5f2085e3231782555efde8e39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332467"
---
# <a name="iwmpcontrols3audiolanguagecount-property"></a><span data-ttu-id="5ef97-106">Proprietà IWMPControls3:: audioLanguageCount</span><span class="sxs-lookup"><span data-stu-id="5ef97-106">IWMPControls3::audioLanguageCount property</span></span>

<span data-ttu-id="5ef97-107">La proprietà **audioLanguageCount** ottiene il conteggio delle lingue audio supportate.</span><span class="sxs-lookup"><span data-stu-id="5ef97-107">The **audioLanguageCount** property gets the count of supported audio languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef97-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ef97-108">Syntax</span></span>


```CSharp
public System.Int32 audioLanguageCount {get; set;}
```


```VB

Public ReadOnly Property audioLanguageCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="5ef97-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5ef97-109">Property value</span></span>

<span data-ttu-id="5ef97-110">**System. Int32** che rappresenta il numero di lingue audio supportate.</span><span class="sxs-lookup"><span data-stu-id="5ef97-110">A **System.Int32** that is the count of supported audio languages.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ef97-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ef97-111">Remarks</span></span>

<span data-ttu-id="5ef97-112">Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.</span><span class="sxs-lookup"><span data-stu-id="5ef97-112">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef97-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ef97-113">Requirements</span></span>



| <span data-ttu-id="5ef97-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ef97-114">Requirement</span></span> | <span data-ttu-id="5ef97-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5ef97-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef97-116">Versione</span><span class="sxs-lookup"><span data-stu-id="5ef97-116">Version</span></span><br/>   | <span data-ttu-id="5ef97-117">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5ef97-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5ef97-118">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ef97-118">Namespace</span></span><br/> | <span data-ttu-id="5ef97-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5ef97-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5ef97-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="5ef97-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5ef97-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5ef97-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ef97-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ef97-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef97-123">**Interfaccia IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5ef97-123">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5ef97-124">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5ef97-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5ef97-125">**IWMPControls3. currentAudioLanguageIndex (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5ef97-125">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5ef97-126">**IWMPControls3. getAudioLanguageDescription (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5ef97-126">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5ef97-127">**IWMPControls3. getAudioLanguageID (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5ef97-127">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5ef97-128">**IWMPControls3. getLanguageName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5ef97-128">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





