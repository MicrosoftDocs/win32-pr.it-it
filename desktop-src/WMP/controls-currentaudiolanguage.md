---
title: Controls. currentAudioLanguage
description: La proprietà currentAudioLanguage specifica o recupera l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Media Player di Windows Controls. currentAudioLanguage
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bc84c7d4c14bb742a6db37feca59fb9d0db0e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330125"
---
# <a name="controlscurrentaudiolanguage"></a><span data-ttu-id="e26f1-104">Controls. currentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="e26f1-104">Controls.currentAudioLanguage</span></span>

<span data-ttu-id="e26f1-105">La proprietà **currentAudioLanguage** specifica o recupera l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="e26f1-105">The **currentAudioLanguage** property specifies or retrieves the locale identifier (LCID) of the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a><span data-ttu-id="e26f1-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="e26f1-106">Possible Values</span></span>

<span data-ttu-id="e26f1-107">Questa proprietà è un **numero** di lettura/scrittura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="e26f1-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e26f1-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e26f1-108">Remarks</span></span>

<span data-ttu-id="e26f1-109">Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="e26f1-109">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="e26f1-110">Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.</span><span class="sxs-lookup"><span data-stu-id="e26f1-110">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="e26f1-111">Quando si usa il contenuto DVD, se si specifica un LCID, verrà selezionata la prima traccia audio disponibile con l'ID lingua specificato.</span><span class="sxs-lookup"><span data-stu-id="e26f1-111">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

<span data-ttu-id="e26f1-112">**Windows Media Player 10 Mobile:** Questa proprietà accetta o restituisce solo l'LCID indipendente dalla lingua (0).</span><span class="sxs-lookup"><span data-stu-id="e26f1-112">**Windows Media Player 10 Mobile:** This property only accepts or returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="e26f1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e26f1-113">Requirements</span></span>



| <span data-ttu-id="e26f1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e26f1-114">Requirement</span></span> | <span data-ttu-id="e26f1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e26f1-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e26f1-116">Versione</span><span class="sxs-lookup"><span data-stu-id="e26f1-116">Version</span></span><br/> | <span data-ttu-id="e26f1-117">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e26f1-117">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e26f1-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e26f1-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="e26f1-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e26f1-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e26f1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e26f1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e26f1-121">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="e26f1-121">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="e26f1-122">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="e26f1-122">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="e26f1-123">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="e26f1-123">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="e26f1-124">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="e26f1-124">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="e26f1-125">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="e26f1-125">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="e26f1-126">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="e26f1-126">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





