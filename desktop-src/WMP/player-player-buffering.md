---
title: Evento Player. buffering
description: L'evento di buffering si verifica quando il controllo Media Player Windows inizia o termina il buffering o il download. | Evento Player. buffering
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Media Player buffering di Windows Event
- Evento di buffering Media Player di Windows, classe Player
- Classe Player Windows Media Player, evento di buffering
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327065"
---
# <a name="playerbuffering-event"></a><span data-ttu-id="d9779-107">Evento Player. buffering</span><span class="sxs-lookup"><span data-stu-id="d9779-107">Player.Buffering event</span></span>

<span data-ttu-id="d9779-108">L'evento di **buffering** si verifica quando il controllo Media Player Windows inizia o termina il buffering o il download.</span><span class="sxs-lookup"><span data-stu-id="d9779-108">The **Buffering** event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9779-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9779-109">Syntax</span></span>


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a><span data-ttu-id="d9779-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9779-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9779-111">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="d9779-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="d9779-112">**Valore booleano** contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d9779-112">**Boolean** containing one of the following values.</span></span>



| <span data-ttu-id="d9779-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d9779-113">Value</span></span> | <span data-ttu-id="d9779-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9779-114">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="d9779-115">true</span><span class="sxs-lookup"><span data-stu-id="d9779-115">true</span></span>  | <span data-ttu-id="d9779-116">Il buffering è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="d9779-116">Buffering has started.</span></span> |
| <span data-ttu-id="d9779-117">false</span><span class="sxs-lookup"><span data-stu-id="d9779-117">false</span></span> | <span data-ttu-id="d9779-118">Il buffering è terminato.</span><span class="sxs-lookup"><span data-stu-id="d9779-118">Buffering has ended.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9779-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9779-119">Return value</span></span>

<span data-ttu-id="d9779-120">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d9779-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9779-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9779-121">Remarks</span></span>

<span data-ttu-id="d9779-122">Utilizzare questo evento per determinare quando viene avviata o arrestata la memorizzazione nel buffer o il download.</span><span class="sxs-lookup"><span data-stu-id="d9779-122">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="d9779-123">È possibile utilizzare lo stesso blocco di eventi sia per i case che per la *rete* di test. **bufferingProgress** e *rete*. **downloadProgress** per determinare se Windows Media Player sta attualmente memorizzando nel buffer o scaricando il contenuto.</span><span class="sxs-lookup"><span data-stu-id="d9779-123">You can use the same event block for both cases and test *Network*.**bufferingProgress** and *Network*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

<span data-ttu-id="d9779-124">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="d9779-124">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file by using the parameter name given.</span></span> <span data-ttu-id="d9779-125">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="d9779-125">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9779-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9779-126">Requirements</span></span>



| <span data-ttu-id="d9779-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9779-127">Requirement</span></span> | <span data-ttu-id="d9779-128">Valore</span><span class="sxs-lookup"><span data-stu-id="d9779-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9779-129">Versione</span><span class="sxs-lookup"><span data-stu-id="d9779-129">Version</span></span><br/> | <span data-ttu-id="d9779-130">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="d9779-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d9779-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d9779-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="d9779-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9779-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9779-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9779-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9779-134">**Rete. bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="d9779-134">**Network.bufferingProgress**</span></span>](network-bufferingprogress.md)
</dt> <dt>

[<span data-ttu-id="d9779-135">**Rete. downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="d9779-135">**Network.downloadProgress**</span></span>](network-downloadprogress.md)
</dt> <dt>

[<span data-ttu-id="d9779-136">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="d9779-136">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





