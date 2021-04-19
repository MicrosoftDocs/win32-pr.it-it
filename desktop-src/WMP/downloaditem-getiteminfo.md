---
title: DownloadItem. getItemInfo, metodo
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo getItemInfo Recupera il valore di un attributo per l'elemento di download.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, classe DownloadItem
- Classe DownloadItem Windows Media Player, metodo getItemInfo
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326345"
---
# <a name="downloaditemgetiteminfo-method"></a><span data-ttu-id="39cd8-108">DownloadItem. getItemInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="39cd8-108">DownloadItem.getItemInfo method</span></span>

> [!Note]  
> <span data-ttu-id="39cd8-109">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="39cd8-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="39cd8-110">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="39cd8-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="39cd8-111">Il metodo **GetItemInfo** Recupera il valore di un attributo per l'elemento di download.</span><span class="sxs-lookup"><span data-stu-id="39cd8-111">The **getItemInfo** method retrieves the value of an attribute for the download item.</span></span>

## <a name="syntax"></a><span data-ttu-id="39cd8-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39cd8-112">Syntax</span></span>


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a><span data-ttu-id="39cd8-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="39cd8-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39cd8-114">*ItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39cd8-114">*itemname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39cd8-115">**Stringa** contenente il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="39cd8-115">**String** containing the attribute name.</span></span> <span data-ttu-id="39cd8-116">I valori supportati sono AlbumArtist, album, Duration, WM/provider, title, UserRating e WM/numero.</span><span class="sxs-lookup"><span data-stu-id="39cd8-116">Supported values are AlbumArtist, Album, Duration, WM/Provider, Title, UserRating, and WM/TrackNumber.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39cd8-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39cd8-117">Return value</span></span>

<span data-ttu-id="39cd8-118">Questo metodo restituisce una **stringa** contenente il valore dell'attributo specificato da *ItemName*.</span><span class="sxs-lookup"><span data-stu-id="39cd8-118">This method returns a **String** containing the value of the attribute specified by *itemname*.</span></span>

## <a name="remarks"></a><span data-ttu-id="39cd8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="39cd8-119">Remarks</span></span>

<span data-ttu-id="39cd8-120">Questo metodo recupera gli attributi specificati usando la stringa di descrizione BITS.</span><span class="sxs-lookup"><span data-stu-id="39cd8-120">This method retrieves attributes specified using the BITS description string.</span></span> <span data-ttu-id="39cd8-121">Vedere la [convenzione di processo di Windows Media Player bits](windows-media-player-bits-job-convention.md).</span><span class="sxs-lookup"><span data-stu-id="39cd8-121">See [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md).</span></span>

<span data-ttu-id="39cd8-122">Questo metodo è supportato per il download in background.</span><span class="sxs-lookup"><span data-stu-id="39cd8-122">This method is supported for background downloading.</span></span> <span data-ttu-id="39cd8-123">Il codice non deve chiamare questo metodo quando si usa il download in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="39cd8-123">Your code should not call this method when using real-time downloading.</span></span>

<span data-ttu-id="39cd8-124">Questo metodo consente di recuperare informazioni per i processi BITS aggiunti solo durante la sessione corrente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="39cd8-124">This method can retrieve information for BITS jobs added during the current Windows Media Player session only.</span></span>

## <a name="requirements"></a><span data-ttu-id="39cd8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39cd8-125">Requirements</span></span>



| <span data-ttu-id="39cd8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="39cd8-126">Requirement</span></span> | <span data-ttu-id="39cd8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="39cd8-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39cd8-128">Versione</span><span class="sxs-lookup"><span data-stu-id="39cd8-128">Version</span></span><br/> | <span data-ttu-id="39cd8-129">Windows Media Player 10 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="39cd8-129">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="39cd8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="39cd8-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="39cd8-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39cd8-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39cd8-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39cd8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39cd8-133">**DownloadItem. Type**</span><span class="sxs-lookup"><span data-stu-id="39cd8-133">**DownloadItem.type**</span></span>](downloaditem-type.md)
</dt> <dt>

[<span data-ttu-id="39cd8-134">**Oggetto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="39cd8-134">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





