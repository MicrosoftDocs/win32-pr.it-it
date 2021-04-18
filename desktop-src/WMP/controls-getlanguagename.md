---
title: Controls. getLanguageName, metodo
description: Il metodo getLanguageName Recupera il nome della lingua audio con l'identificatore delle impostazioni locali (LCID) specificato.
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- Metodo getLanguageName Windows Media Player
- Metodo getLanguageName Windows Media Player, classe Controls
- Classe Controls Media Player Windows, metodo getLanguageName
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331247"
---
# <a name="controlsgetlanguagename-method"></a><span data-ttu-id="0d698-106">Controls. getLanguageName, metodo</span><span class="sxs-lookup"><span data-stu-id="0d698-106">Controls.getLanguageName method</span></span>

<span data-ttu-id="0d698-107">Il metodo **getLanguageName** Recupera il nome della lingua audio con l'identificatore delle impostazioni locali (LCID) specificato.</span><span class="sxs-lookup"><span data-stu-id="0d698-107">The **getLanguageName** method retrieves the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d698-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d698-108">Syntax</span></span>


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a><span data-ttu-id="0d698-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d698-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d698-110">*LCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d698-110">*LCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d698-111">**Numero** (**Long**) che specifica l'identificatore LCID.</span><span class="sxs-lookup"><span data-stu-id="0d698-111">**Number** (**long**) specifying the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d698-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d698-112">Return value</span></span>

<span data-ttu-id="0d698-113">Questo metodo restituisce una **stringa**.</span><span class="sxs-lookup"><span data-stu-id="0d698-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d698-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d698-114">Remarks</span></span>

<span data-ttu-id="0d698-115">Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="0d698-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="0d698-116">Per il contenuto basato su Windows Media, le proprietà e i metodi relativi alla selezione della lingua supportano solo un singolo output.</span><span class="sxs-lookup"><span data-stu-id="0d698-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d698-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d698-117">Requirements</span></span>



| <span data-ttu-id="0d698-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d698-118">Requirement</span></span> | <span data-ttu-id="0d698-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0d698-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d698-120">Versione</span><span class="sxs-lookup"><span data-stu-id="0d698-120">Version</span></span><br/> | <span data-ttu-id="0d698-121">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0d698-121">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="0d698-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0d698-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d698-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d698-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d698-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d698-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d698-125">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="0d698-125">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="0d698-126">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="0d698-126">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="0d698-127">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="0d698-127">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="0d698-128">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="0d698-128">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="0d698-129">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="0d698-129">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="0d698-130">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="0d698-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





