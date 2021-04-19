---
title: Controls. currentAudioLanguageIndex
description: La proprietà currentAudioLanguageIndex specifica o recupera l'indice in base uno che corrisponde alla lingua audio per la riproduzione.
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- Media Player di Windows Controls. currentAudioLanguageIndex
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1eb87873170c486782368f431f4fa8e3597b20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330124"
---
# <a name="controlscurrentaudiolanguageindex"></a><span data-ttu-id="0b8cb-104">Controls. currentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="0b8cb-104">Controls.currentAudioLanguageIndex</span></span>

<span data-ttu-id="0b8cb-105">La proprietà **currentAudioLanguageIndex** specifica o recupera l'indice in base uno che corrisponde alla lingua audio per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-105">The **currentAudioLanguageIndex** property specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a><span data-ttu-id="0b8cb-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="0b8cb-106">Possible Values</span></span>

<span data-ttu-id="0b8cb-107">Questa proprietà è un **numero** di lettura/scrittura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="0b8cb-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b8cb-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b8cb-108">Remarks</span></span>

<span data-ttu-id="0b8cb-109">Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-109">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="0b8cb-110">Usare la proprietà **audioLanguageCount** per ottenere il numero di lingue audio supportate.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-110">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

<span data-ttu-id="0b8cb-111">**Windows Media Player 10 Mobile:** Questa proprietà accetta o restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-111">**Windows Media Player 10 Mobile:** This property only accepts or returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b8cb-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b8cb-112">Requirements</span></span>



| <span data-ttu-id="0b8cb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b8cb-113">Requirement</span></span> | <span data-ttu-id="0b8cb-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0b8cb-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8cb-115">Versione</span><span class="sxs-lookup"><span data-stu-id="0b8cb-115">Version</span></span><br/> | <span data-ttu-id="0b8cb-116">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-116">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="0b8cb-117">DLL</span><span class="sxs-lookup"><span data-stu-id="0b8cb-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="0b8cb-118"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b8cb-118"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b8cb-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b8cb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b8cb-120">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="0b8cb-120">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="0b8cb-121">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="0b8cb-121">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="0b8cb-122">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="0b8cb-122">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="0b8cb-123">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="0b8cb-123">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="0b8cb-124">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="0b8cb-124">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="0b8cb-125">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="0b8cb-125">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





