---
title: Controls. getAudioLanguageDescription, metodo
description: Il metodo getAudioLanguageDescription recupera la descrizione della lingua audio corrispondente all'indice in base uno specificato.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- Metodo getAudioLanguageDescription Windows Media Player
- Metodo getAudioLanguageDescription Windows Media Player, classe Controls
- Classe Controls Media Player Windows, metodo getAudioLanguageDescription
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326476"
---
# <a name="controlsgetaudiolanguagedescription-method"></a><span data-ttu-id="e5c51-106">Controls. getAudioLanguageDescription, metodo</span><span class="sxs-lookup"><span data-stu-id="e5c51-106">Controls.getAudioLanguageDescription method</span></span>

<span data-ttu-id="e5c51-107">Il metodo **getAudioLanguageDescription** recupera la descrizione della lingua audio corrispondente all'indice in base uno specificato.</span><span class="sxs-lookup"><span data-stu-id="e5c51-107">The **getAudioLanguageDescription** method retrieves the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c51-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5c51-108">Syntax</span></span>


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="e5c51-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5c51-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5c51-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e5c51-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5c51-111">**Numero** (**Long**) che specifica l'indice della lingua audio in base uno.</span><span class="sxs-lookup"><span data-stu-id="e5c51-111">**Number** (**long**) specifying the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5c51-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5c51-112">Return value</span></span>

<span data-ttu-id="e5c51-113">Questo metodo restituisce un valore **stringa** .</span><span class="sxs-lookup"><span data-stu-id="e5c51-113">This method returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5c51-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5c51-114">Remarks</span></span>

<span data-ttu-id="e5c51-115">Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.</span><span class="sxs-lookup"><span data-stu-id="e5c51-115">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="e5c51-116">Utilizzare la proprietà **audioLanguageCount** per ottenere il numero di lingue audio supportate e accedere a una lingua audio singolarmente utilizzando un indice in base uno.</span><span class="sxs-lookup"><span data-stu-id="e5c51-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

<span data-ttu-id="e5c51-117">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e5c51-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5c51-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5c51-118">Requirements</span></span>



| <span data-ttu-id="e5c51-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5c51-119">Requirement</span></span> | <span data-ttu-id="e5c51-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e5c51-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c51-121">Versione</span><span class="sxs-lookup"><span data-stu-id="e5c51-121">Version</span></span><br/> | <span data-ttu-id="e5c51-122">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e5c51-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e5c51-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e5c51-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e5c51-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5c51-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c51-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5c51-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c51-126">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="e5c51-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="e5c51-127">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="e5c51-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="e5c51-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="e5c51-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="e5c51-129">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="e5c51-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="e5c51-130">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="e5c51-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="e5c51-131">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="e5c51-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





