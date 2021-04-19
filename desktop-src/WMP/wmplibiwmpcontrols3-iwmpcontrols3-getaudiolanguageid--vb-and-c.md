---
title: Metodo IWMPControls3 getAudioLanguageID
description: Il metodo getAudioLanguageID restituisce l'identificatore delle impostazioni locali (LCID) per un indice di lingua audio specificato.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- Metodo getAudioLanguageID Windows Media Player
- Metodo getAudioLanguageID Windows Media Player, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, metodo getAudioLanguageID
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332452"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a><span data-ttu-id="e0250-106">Metodo IWMPControls3:: getAudioLanguageID</span><span class="sxs-lookup"><span data-stu-id="e0250-106">IWMPControls3::getAudioLanguageID method</span></span>

<span data-ttu-id="e0250-107">Il metodo **getAudioLanguageID** restituisce l'identificatore delle impostazioni locali (LCID) per un indice di lingua audio specificato.</span><span class="sxs-lookup"><span data-stu-id="e0250-107">The **getAudioLanguageID** method returns the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0250-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0250-108">Syntax</span></span>


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a><span data-ttu-id="e0250-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0250-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0250-110">*lIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0250-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0250-111">**System. Int32** che rappresenta l'indice in base uno della lingua audio.</span><span class="sxs-lookup"><span data-stu-id="e0250-111">A **System.Int32** that is the one-based index of the audio language.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0250-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0250-112">Return value</span></span>

<span data-ttu-id="e0250-113">**System. Int32** che rappresenta l'identificatore LCID.</span><span class="sxs-lookup"><span data-stu-id="e0250-113">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0250-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0250-114">Remarks</span></span>

<span data-ttu-id="e0250-115">Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="e0250-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="e0250-116">Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.</span><span class="sxs-lookup"><span data-stu-id="e0250-116">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="e0250-117">Utilizzare la proprietà **audioLanguageCount** per ottenere il numero di lingue audio supportate e accedere a una lingua audio singolarmente utilizzando un indice in base uno.</span><span class="sxs-lookup"><span data-stu-id="e0250-117">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0250-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0250-118">Requirements</span></span>



| <span data-ttu-id="e0250-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0250-119">Requirement</span></span> | <span data-ttu-id="e0250-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e0250-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0250-121">Versione</span><span class="sxs-lookup"><span data-stu-id="e0250-121">Version</span></span><br/>   | <span data-ttu-id="e0250-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e0250-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e0250-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e0250-123">Namespace</span></span><br/> | <span data-ttu-id="e0250-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e0250-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e0250-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="e0250-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e0250-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e0250-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0250-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0250-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0250-128">**Interfaccia IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0250-128">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0250-129">**IWMPControls3. audioLanguageCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0250-129">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0250-130">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0250-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0250-131">**IWMPControls3. currentAudioLanguageIndex (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0250-131">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0250-132">**IWMPControls3. getAudioLanguageDescription (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0250-132">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e0250-133">**IWMPControls3. getLanguageName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e0250-133">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





