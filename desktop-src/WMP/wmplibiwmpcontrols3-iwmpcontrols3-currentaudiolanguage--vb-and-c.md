---
title: Proprietà currentAudioLanguage di IWMPControls3
description: La proprietà currentAudioLanguage Ottiene o imposta l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- Finestra delle proprietà di currentAudioLanguage Media Player
- Proprietà di currentAudioLanguage Media Player Windows, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, proprietà currentAudioLanguage
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4621b5eace56cb883a6c8b14c3b1f082b12d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332466"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a><span data-ttu-id="2ffce-106">Proprietà IWMPControls3:: currentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="2ffce-106">IWMPControls3::currentAudioLanguage property</span></span>

<span data-ttu-id="2ffce-107">La proprietà **currentAudioLanguage** Ottiene o imposta l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="2ffce-107">The **currentAudioLanguage** property gets or sets the locale identifier (LCID) of the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ffce-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ffce-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="2ffce-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2ffce-109">Property value</span></span>

<span data-ttu-id="2ffce-110">**System. Int32** che rappresenta l'identificatore LCID della lingua audio.</span><span class="sxs-lookup"><span data-stu-id="2ffce-110">A **System.Int32** that is the LCID of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ffce-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ffce-111">Remarks</span></span>

<span data-ttu-id="2ffce-112">Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="2ffce-112">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="2ffce-113">Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.</span><span class="sxs-lookup"><span data-stu-id="2ffce-113">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="2ffce-114">Quando si usa il contenuto DVD, se si specifica un LCID, verrà selezionata la prima traccia audio disponibile con l'ID lingua specificato.</span><span class="sxs-lookup"><span data-stu-id="2ffce-114">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ffce-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ffce-115">Requirements</span></span>



| <span data-ttu-id="2ffce-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ffce-116">Requirement</span></span> | <span data-ttu-id="2ffce-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2ffce-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ffce-118">Versione</span><span class="sxs-lookup"><span data-stu-id="2ffce-118">Version</span></span><br/>   | <span data-ttu-id="2ffce-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2ffce-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2ffce-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2ffce-120">Namespace</span></span><br/> | <span data-ttu-id="2ffce-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2ffce-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2ffce-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="2ffce-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2ffce-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2ffce-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ffce-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ffce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ffce-125">**Interfaccia IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2ffce-125">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ffce-126">**IWMPControls3. audioLanguageCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2ffce-126">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ffce-127">**IWMPControls3. currentAudioLanguageIndex (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2ffce-127">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ffce-128">**IWMPControls3. getAudioLanguageDescription (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2ffce-128">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ffce-129">**IWMPControls3. getAudioLanguageID (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2ffce-129">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ffce-130">**IWMPControls3. getLanguageName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2ffce-130">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





