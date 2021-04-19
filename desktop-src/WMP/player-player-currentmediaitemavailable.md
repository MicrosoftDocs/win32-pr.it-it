---
title: Evento Player. CurrentMediaItemAvailable
description: L'evento CurrentMediaItemAvailable si verifica quando diventa disponibile un elemento di metadati grafici nell'elemento multimediale corrente. | Evento Player. CurrentMediaItemAvailable
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Media Player di Windows Event CurrentMediaItemAvailable
- Windows Event CurrentMediaItemAvailable Media Player, classe Player
- Classe Player Windows Media Player, evento CurrentMediaItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326722"
---
# <a name="playercurrentmediaitemavailable-event"></a><span data-ttu-id="f5c72-107">Evento Player. CurrentMediaItemAvailable</span><span class="sxs-lookup"><span data-stu-id="f5c72-107">Player.CurrentMediaItemAvailable event</span></span>

<span data-ttu-id="f5c72-108">L'evento **CurrentMediaItemAvailable** si verifica quando diventa disponibile un elemento di metadati grafici nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="f5c72-108">The **CurrentMediaItemAvailable** event occurs when a graphic metadata item in the current media item becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c72-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5c72-109">Syntax</span></span>


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="f5c72-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5c72-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c72-111">*bstrItemName*</span><span class="sxs-lookup"><span data-stu-id="f5c72-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c72-112">**Stringa** contenente il nome dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="f5c72-112">**String** containing the name of the current media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c72-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5c72-113">Return value</span></span>

<span data-ttu-id="f5c72-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f5c72-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5c72-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5c72-115">Remarks</span></span>

<span data-ttu-id="f5c72-116">Poiché la riproduzione può iniziare prima che un elemento multimediale venga scaricato completamente, eventuali elementi grafici dei metadati contenuti nell'elemento multimediale, ad esempio Album Cover Art, potrebbero non essere disponibili quando viene avviata la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="f5c72-116">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="f5c72-117">Questo evento avvisa l'utente al termine del download di un elemento grafico dei metadati.</span><span class="sxs-lookup"><span data-stu-id="f5c72-117">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="f5c72-118">È quindi possibile recuperare l'oggetto **multimediale** passando il valore di *bstrItemName* a *mediacollection*. metodo **GetByName** , dopo il quale è possibile accedere all'elemento grafico dei metadati usando i *supporti*. **getItemInfoByType** e specificando **WM/Picture** per il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="f5c72-118">You can then retrieve the **Media** object by passing the value of *bstrItemName* to the *MediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *Media*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

<span data-ttu-id="f5c72-119">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="f5c72-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="f5c72-120">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="f5c72-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="f5c72-121">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f5c72-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c72-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5c72-122">Requirements</span></span>



| <span data-ttu-id="f5c72-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5c72-123">Requirement</span></span> | <span data-ttu-id="f5c72-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f5c72-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c72-125">Versione</span><span class="sxs-lookup"><span data-stu-id="f5c72-125">Version</span></span><br/> | <span data-ttu-id="f5c72-126">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="f5c72-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f5c72-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f5c72-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="f5c72-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5c72-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5c72-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5c72-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c72-130">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="f5c72-130">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f5c72-131">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="f5c72-131">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="f5c72-132">**Mediacollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="f5c72-132">**MediaCollection.getByName**</span></span>](mediacollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="f5c72-133">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="f5c72-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





