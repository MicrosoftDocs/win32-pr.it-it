---
title: Metodo IWMPControls3 getAudioLanguageDescription
description: Il metodo getAudioLanguageDescription restituisce la descrizione della lingua audio corrispondente all'indice in base uno specificato.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- Metodo getAudioLanguageDescription Windows Media Player
- Metodo getAudioLanguageDescription Windows Media Player, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, metodo getAudioLanguageDescription
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb45ceb166ca9c948823e516029569e457f35e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332454"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a><span data-ttu-id="473d6-106">Metodo IWMPControls3:: getAudioLanguageDescription</span><span class="sxs-lookup"><span data-stu-id="473d6-106">IWMPControls3::getAudioLanguageDescription method</span></span>

<span data-ttu-id="473d6-107">Il metodo **getAudioLanguageDescription** restituisce la descrizione della lingua audio corrispondente all'indice in base uno specificato.</span><span class="sxs-lookup"><span data-stu-id="473d6-107">The **getAudioLanguageDescription** method returns the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="473d6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="473d6-108">Syntax</span></span>


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a><span data-ttu-id="473d6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="473d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="473d6-110">*lIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="473d6-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="473d6-111">**System. Int32** che è l'indice del linguaggio audio basato su uno.</span><span class="sxs-lookup"><span data-stu-id="473d6-111">A **System.Int32** that is the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="473d6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="473d6-112">Return value</span></span>

<span data-ttu-id="473d6-113">**System. String** che rappresenta la descrizione della lingua audio.</span><span class="sxs-lookup"><span data-stu-id="473d6-113">A **System.String** that is the description of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="473d6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="473d6-114">Remarks</span></span>

<span data-ttu-id="473d6-115">Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.</span><span class="sxs-lookup"><span data-stu-id="473d6-115">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="473d6-116">Utilizzare la proprietà **audioLanguageCount** per ottenere il numero di lingue audio supportate e accedere a una lingua audio singolarmente utilizzando un indice in base uno.</span><span class="sxs-lookup"><span data-stu-id="473d6-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="473d6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="473d6-117">Requirements</span></span>



| <span data-ttu-id="473d6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="473d6-118">Requirement</span></span> | <span data-ttu-id="473d6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="473d6-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="473d6-120">Versione</span><span class="sxs-lookup"><span data-stu-id="473d6-120">Version</span></span><br/>   | <span data-ttu-id="473d6-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="473d6-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="473d6-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="473d6-122">Namespace</span></span><br/> | <span data-ttu-id="473d6-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="473d6-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="473d6-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="473d6-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="473d6-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="473d6-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="473d6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="473d6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="473d6-127">**Interfaccia IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="473d6-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="473d6-128">**IWMPControls3. audioLanguageCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="473d6-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="473d6-129">**IWMPControls3. currentAudioLanguageIndex (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="473d6-129">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="473d6-130">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="473d6-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="473d6-131">**IWMPControls3. getAudioLanguageID (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="473d6-131">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="473d6-132">**IWMPControls3. getLanguageName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="473d6-132">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





