---
title: Metodo getLanguageName IWMPControls3
description: Il metodo getLanguageName restituisce il nome della lingua audio con l'identificatore delle impostazioni locali (LCID) specificato.
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- Metodo getLanguageName Windows Media Player
- Metodo getLanguageName Windows Media Player, interfaccia IWMPControls3
- Interfaccia IWMPControls3 Windows Media Player, metodo getLanguageName
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93bf97c7b5213e3d196897de1c3ebcfa6e6d2c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332451"
---
# <a name="iwmpcontrols3getlanguagename-method"></a><span data-ttu-id="04432-106">Metodo IWMPControls3:: getLanguageName</span><span class="sxs-lookup"><span data-stu-id="04432-106">IWMPControls3::getLanguageName method</span></span>

<span data-ttu-id="04432-107">Il metodo **getLanguageName** restituisce il nome della lingua audio con l'identificatore delle impostazioni locali (LCID) specificato.</span><span class="sxs-lookup"><span data-stu-id="04432-107">The **getLanguageName** method returns the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="04432-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04432-108">Syntax</span></span>


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a><span data-ttu-id="04432-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="04432-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04432-110">*lLangID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04432-110">*lLangID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04432-111">**System. Int32** che rappresenta l'identificatore LCID.</span><span class="sxs-lookup"><span data-stu-id="04432-111">A **System.Int32** that is the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04432-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04432-112">Return value</span></span>

<span data-ttu-id="04432-113">**System. String** che rappresenta il nome della lingua audio.</span><span class="sxs-lookup"><span data-stu-id="04432-113">A **System.String** that is the name of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="04432-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="04432-114">Remarks</span></span>

<span data-ttu-id="04432-115">Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="04432-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="04432-116">Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.</span><span class="sxs-lookup"><span data-stu-id="04432-116">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="04432-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04432-117">Requirements</span></span>



| <span data-ttu-id="04432-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="04432-118">Requirement</span></span> | <span data-ttu-id="04432-119">Valore</span><span class="sxs-lookup"><span data-stu-id="04432-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04432-120">Versione</span><span class="sxs-lookup"><span data-stu-id="04432-120">Version</span></span><br/>   | <span data-ttu-id="04432-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="04432-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="04432-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="04432-122">Namespace</span></span><br/> | <span data-ttu-id="04432-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="04432-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="04432-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="04432-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="04432-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="04432-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04432-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04432-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04432-127">**Interfaccia IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="04432-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="04432-128">**IWMPControls3. audioLanguageCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="04432-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="04432-129">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="04432-129">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="04432-130">**IWMPControls3. currentAudioLanguageIndex (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="04432-130">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="04432-131">**IWMPControls3. getAudioLanguageDescription (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="04432-131">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="04432-132">**IWMPControls3. getAudioLanguageID (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="04432-132">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





