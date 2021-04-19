---
title: Proprietà currentAudioLanguageIndex di IWMPControls3
description: La proprietà currentAudioLanguageIndex Ottiene o imposta l'indice in base uno che corrisponde alla lingua audio per la riproduzione.
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- Finestra delle proprietà di currentAudioLanguageIndex Media Player
- Proprietà di currentAudioLanguageIndex Media Player Windows, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, proprietà currentAudioLanguageIndex
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fb36eea4038322cacd7f233892151ab77e5eea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332464"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a><span data-ttu-id="9cdbb-106">Proprietà IWMPControls3:: currentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="9cdbb-106">IWMPControls3::currentAudioLanguageIndex property</span></span>

<span data-ttu-id="9cdbb-107">La proprietà **currentAudioLanguageIndex** Ottiene o imposta l'indice in base uno che corrisponde alla lingua audio per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="9cdbb-107">The **currentAudioLanguageIndex** property gets or sets the one-based index that corresponds to the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cdbb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cdbb-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="9cdbb-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9cdbb-109">Property value</span></span>

<span data-ttu-id="9cdbb-110">**System. Int32** che rappresenta l'indice in base uno della lingua.</span><span class="sxs-lookup"><span data-stu-id="9cdbb-110">A **System.Int32** that is the one-based index of the language.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cdbb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cdbb-111">Remarks</span></span>

<span data-ttu-id="9cdbb-112">Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.</span><span class="sxs-lookup"><span data-stu-id="9cdbb-112">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="9cdbb-113">Usare la proprietà **audioLanguageCount** per ottenere il numero di lingue audio supportate.</span><span class="sxs-lookup"><span data-stu-id="9cdbb-113">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cdbb-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cdbb-114">Requirements</span></span>



| <span data-ttu-id="9cdbb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cdbb-115">Requirement</span></span> | <span data-ttu-id="9cdbb-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9cdbb-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cdbb-117">Versione</span><span class="sxs-lookup"><span data-stu-id="9cdbb-117">Version</span></span><br/>   | <span data-ttu-id="9cdbb-118">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9cdbb-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9cdbb-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9cdbb-119">Namespace</span></span><br/> | <span data-ttu-id="9cdbb-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9cdbb-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9cdbb-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="9cdbb-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9cdbb-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbb-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cdbb-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cdbb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cdbb-124">**Interfaccia IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9cdbb-124">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9cdbb-125">**IWMPControls3. audioLanguageCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9cdbb-125">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9cdbb-126">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9cdbb-126">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9cdbb-127">**IWMPControls3. getAudioLanguageDescription (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9cdbb-127">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9cdbb-128">**IWMPControls3. getAudioLanguageID (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9cdbb-128">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9cdbb-129">**IWMPControls3. getLanguageName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9cdbb-129">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





