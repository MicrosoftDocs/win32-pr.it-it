---
title: Evento Player. OpenPlaylistSwitch
description: L'evento OpenPlaylistSwitch si verifica quando viene avviata la riproduzione di un titolo su un DVD. | Evento Player. OpenPlaylistSwitch
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Media Player di Windows Event OpenPlaylistSwitch
- Windows Event OpenPlaylistSwitch Media Player, classe Player
- Classe Player Windows Media Player, evento OpenPlaylistSwitch
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326465"
---
# <a name="playeropenplaylistswitch-event"></a><span data-ttu-id="50226-107">Evento Player. OpenPlaylistSwitch</span><span class="sxs-lookup"><span data-stu-id="50226-107">Player.OpenPlaylistSwitch event</span></span>

<span data-ttu-id="50226-108">L'evento **OpenPlaylistSwitch** si verifica quando viene avviata la riproduzione di un titolo su un DVD.</span><span class="sxs-lookup"><span data-stu-id="50226-108">The **OpenPlaylistSwitch** event occurs when a title on a DVD begins playing.</span></span>

## <a name="syntax"></a><span data-ttu-id="50226-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50226-109">Syntax</span></span>


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a><span data-ttu-id="50226-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="50226-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50226-111">*pItem*</span><span class="sxs-lookup"><span data-stu-id="50226-111">*pItem*</span></span> 
</dt> <dd>

<span data-ttu-id="50226-112">Oggetto **playlist** che rappresenta il titolo.</span><span class="sxs-lookup"><span data-stu-id="50226-112">**Playlist** object representing the title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50226-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50226-113">Return value</span></span>

<span data-ttu-id="50226-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="50226-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50226-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="50226-115">Remarks</span></span>

<span data-ttu-id="50226-116">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="50226-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="50226-117">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="50226-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="50226-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50226-118">Requirements</span></span>



| <span data-ttu-id="50226-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="50226-119">Requirement</span></span> | <span data-ttu-id="50226-120">Valore</span><span class="sxs-lookup"><span data-stu-id="50226-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50226-121">Versione</span><span class="sxs-lookup"><span data-stu-id="50226-121">Version</span></span><br/> | <span data-ttu-id="50226-122">Windows Media Player per Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="50226-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="50226-123">DLL</span><span class="sxs-lookup"><span data-stu-id="50226-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="50226-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50226-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50226-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50226-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50226-126">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="50226-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





