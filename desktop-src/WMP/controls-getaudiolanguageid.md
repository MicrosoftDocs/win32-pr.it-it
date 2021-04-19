---
title: Controls. getAudioLanguageID, metodo
description: Il metodo getAudioLanguageID recupera l'identificatore delle impostazioni locali (LCID) per un indice di lingua audio specificato.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- Metodo getAudioLanguageID Windows Media Player
- Metodo getAudioLanguageID Windows Media Player, classe Controls
- Classe Controls Media Player Windows, metodo getAudioLanguageID
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab27e95edfc74fa7a9f57d2010bf86299c55dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326473"
---
# <a name="controlsgetaudiolanguageid-method"></a><span data-ttu-id="16f50-106">Controls. getAudioLanguageID, metodo</span><span class="sxs-lookup"><span data-stu-id="16f50-106">Controls.getAudioLanguageID method</span></span>

<span data-ttu-id="16f50-107">Il metodo **getAudioLanguageID** recupera l'identificatore delle impostazioni locali (LCID) per un indice di lingua audio specificato.</span><span class="sxs-lookup"><span data-stu-id="16f50-107">The **getAudioLanguageID** method retrieves the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f50-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16f50-108">Syntax</span></span>


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="16f50-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="16f50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16f50-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="16f50-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16f50-111">**Numero** (**Long**) che specifica l'indice della lingua audio.</span><span class="sxs-lookup"><span data-stu-id="16f50-111">**Number** (**long**) specifying the audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16f50-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16f50-112">Return value</span></span>

<span data-ttu-id="16f50-113">Questo metodo restituisce un **numero** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="16f50-113">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="16f50-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="16f50-114">Remarks</span></span>

<span data-ttu-id="16f50-115">Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="16f50-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="16f50-116">Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.</span><span class="sxs-lookup"><span data-stu-id="16f50-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="16f50-117">**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre l'LCID indipendente dalla lingua (0).</span><span class="sxs-lookup"><span data-stu-id="16f50-117">**Windows Media Player 10 Mobile:** This property always returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="16f50-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16f50-118">Requirements</span></span>



| <span data-ttu-id="16f50-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="16f50-119">Requirement</span></span> | <span data-ttu-id="16f50-120">Valore</span><span class="sxs-lookup"><span data-stu-id="16f50-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16f50-121">Versione</span><span class="sxs-lookup"><span data-stu-id="16f50-121">Version</span></span><br/> | <span data-ttu-id="16f50-122">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="16f50-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="16f50-123">DLL</span><span class="sxs-lookup"><span data-stu-id="16f50-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="16f50-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16f50-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16f50-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16f50-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f50-126">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="16f50-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="16f50-127">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="16f50-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="16f50-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="16f50-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="16f50-129">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="16f50-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="16f50-130">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="16f50-130">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="16f50-131">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="16f50-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





