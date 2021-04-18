---
title: Evento Player. AudioLanguageChange
description: L'evento AudioLanguageChange si verifica quando cambia la lingua audio corrente. | Evento Player. AudioLanguageChange
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Media Player di Windows Event AudioLanguageChange
- Windows Event AudioLanguageChange Media Player, classe Player
- Classe Player Windows Media Player, evento AudioLanguageChange
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327068"
---
# <a name="playeraudiolanguagechange-event"></a><span data-ttu-id="96c7d-107">Evento Player. AudioLanguageChange</span><span class="sxs-lookup"><span data-stu-id="96c7d-107">Player.AudioLanguageChange event</span></span>

<span data-ttu-id="96c7d-108">L'evento **AudioLanguageChange** si verifica quando cambia la lingua audio corrente.</span><span class="sxs-lookup"><span data-stu-id="96c7d-108">The **AudioLanguageChange** event occurs when the current audio language changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c7d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96c7d-109">Syntax</span></span>


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a><span data-ttu-id="96c7d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="96c7d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c7d-111">*LangID*</span><span class="sxs-lookup"><span data-stu-id="96c7d-111">*LangID*</span></span> 
</dt> <dd>

<span data-ttu-id="96c7d-112">**Numero** (**Long**) che specifica il nuovo identificatore delle impostazioni locali (LCID).</span><span class="sxs-lookup"><span data-stu-id="96c7d-112">**Number** (**long**) specifying the new locale identifier (LCID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96c7d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96c7d-113">Return value</span></span>

<span data-ttu-id="96c7d-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="96c7d-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96c7d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="96c7d-115">Remarks</span></span>

<span data-ttu-id="96c7d-116">Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="96c7d-116">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="96c7d-117">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file Microsoft JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="96c7d-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported Microsoft JScript file by using the parameter name given.</span></span> <span data-ttu-id="96c7d-118">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="96c7d-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="96c7d-119">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="96c7d-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="96c7d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96c7d-120">Requirements</span></span>



| <span data-ttu-id="96c7d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c7d-121">Requirement</span></span> | <span data-ttu-id="96c7d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="96c7d-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96c7d-123">Versione</span><span class="sxs-lookup"><span data-stu-id="96c7d-123">Version</span></span><br/> | <span data-ttu-id="96c7d-124">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="96c7d-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="96c7d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="96c7d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="96c7d-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96c7d-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c7d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96c7d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c7d-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="96c7d-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="96c7d-129">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="96c7d-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





