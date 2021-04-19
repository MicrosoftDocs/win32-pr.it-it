---
title: Attributi di sincronizzazione
description: Gli attributi Sync01 tramite Sync16 sono rappresentazioni di stringa di valori a 32 bit utilizzati da Windows Media Player durante la sincronizzazione delle playlist con uno di un massimo di 16 dispositivi portatili.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Attributi di sincronizzazione Windows Media Player
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325580"
---
# <a name="sync-attributes"></a><span data-ttu-id="43aec-104">Attributi di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="43aec-104">Sync Attributes</span></span>

<span data-ttu-id="43aec-105">Gli attributi **Sync01** tramite **Sync16** sono rappresentazioni di stringa di valori a 32 bit utilizzati da Windows Media Player durante la sincronizzazione delle playlist con uno di un massimo di 16 dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="43aec-105">The **Sync01** through **Sync16** attributes are string representations of 32-bit values that Windows Media Player uses when it synchronizes playlists with one of up to 16 portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="43aec-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="43aec-106">Applies To</span></span>

-   [<span data-ttu-id="43aec-107">Playlist</span><span class="sxs-lookup"><span data-stu-id="43aec-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="43aec-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="43aec-108">Remarks</span></span>

<span data-ttu-id="43aec-109">Si tratta di attributi di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="43aec-109">These are read/write attributes.</span></span> <span data-ttu-id="43aec-110">Un valore pari a zero indica che Windows Media Player non deve sincronizzare la playlist con il dispositivo associato.</span><span class="sxs-lookup"><span data-stu-id="43aec-110">A value of zero indicates that Windows Media Player should not synchronize the playlist with the associated device.</span></span> <span data-ttu-id="43aec-111">Un valore maggiore di zero indica una priorità di sincronizzazione per la playlist specificata.</span><span class="sxs-lookup"><span data-stu-id="43aec-111">A value greater than zero indicates a synchronization priority for the given playlist.</span></span>

<span data-ttu-id="43aec-112">In base all'input dell'utente, Windows Media Player imposta questo attributo per ogni playlist nella libreria.</span><span class="sxs-lookup"><span data-stu-id="43aec-112">Based on user input, Windows Media Player sets this attribute for each of the playlists in the library.</span></span> <span data-ttu-id="43aec-113">Quando Windows Media Player tenta di sincronizzare una playlist con un dispositivo portatile, esamina ogni playlist per confrontare i valori per gli attributi di **Sync**_XX_ che rappresentano la partnership del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43aec-113">When Windows Media Player attempts to synchronize a playlist with a portable device, it examines each playlist to compare the values for the **Sync**_XX_ attributes that represent the device partnership.</span></span> <span data-ttu-id="43aec-114">Le playlist con valori _XX_ della **sincronizzazione** inferiore ricevono una priorità di sincronizzazione superiore.</span><span class="sxs-lookup"><span data-stu-id="43aec-114">Playlists that have lower **Sync**_XX_ values receive higher synchronization priority.</span></span>

<span data-ttu-id="43aec-115">Ad esempio, la libreria potrebbe contenere le quattro playlist seguenti e i rispettivi valori _XX_ della **sincronizzazione**:</span><span class="sxs-lookup"><span data-stu-id="43aec-115">For example, the library might contain the following four playlists and respective **Sync**_XX_ values:</span></span>



| <span data-ttu-id="43aec-116">Nome della playlist</span><span class="sxs-lookup"><span data-stu-id="43aec-116">Playlist Name</span></span> | <span data-ttu-id="43aec-117">Valore Sync01</span><span class="sxs-lookup"><span data-stu-id="43aec-117">Sync01 Value</span></span> |
|---------------|--------------|
| <span data-ttu-id="43aec-118">GymMusic. WPL</span><span class="sxs-lookup"><span data-stu-id="43aec-118">GymMusic.WPL</span></span>  | <span data-ttu-id="43aec-119">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="43aec-119">0x0000000D</span></span>   |
| <span data-ttu-id="43aec-120">Relax. WPL</span><span class="sxs-lookup"><span data-stu-id="43aec-120">Relax.WPL</span></span>     | <span data-ttu-id="43aec-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="43aec-121">0x00000020</span></span>   |
| <span data-ttu-id="43aec-122">DriveHome. WPL</span><span class="sxs-lookup"><span data-stu-id="43aec-122">DriveHome.WPL</span></span> | <span data-ttu-id="43aec-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="43aec-123">0x00000001</span></span>   |
| <span data-ttu-id="43aec-124">NoGo. WPL</span><span class="sxs-lookup"><span data-stu-id="43aec-124">NoGo.WPL</span></span>      | <span data-ttu-id="43aec-125">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43aec-125">0x00000000</span></span>   |



 

<span data-ttu-id="43aec-126">Quando Windows Media Player sincronizza il dispositivo associato all'attributo, sincronizza le playlist nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="43aec-126">When Windows Media Player synchronizes the device associated with the attribute, it will synchronize the playlists in the following order:</span></span>

1.  <span data-ttu-id="43aec-127">DriveHome. WPL</span><span class="sxs-lookup"><span data-stu-id="43aec-127">DriveHome.WPL</span></span>
2.  <span data-ttu-id="43aec-128">GymMusic. WPL</span><span class="sxs-lookup"><span data-stu-id="43aec-128">GymMusic.WPL</span></span>
3.  <span data-ttu-id="43aec-129">Relax. WPL</span><span class="sxs-lookup"><span data-stu-id="43aec-129">Relax.WPL</span></span>

<span data-ttu-id="43aec-130">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="43aec-130">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="43aec-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43aec-131">Requirements</span></span>



| <span data-ttu-id="43aec-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="43aec-132">Requirement</span></span> | <span data-ttu-id="43aec-133">Valore</span><span class="sxs-lookup"><span data-stu-id="43aec-133">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="43aec-134">Versione</span><span class="sxs-lookup"><span data-stu-id="43aec-134">Version</span></span><br/> | <span data-ttu-id="43aec-135">Windows Media Player 10 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="43aec-135">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43aec-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43aec-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43aec-137">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="43aec-137">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="43aec-138">**Enumerazione delle playlist di sincronizzazione**</span><span class="sxs-lookup"><span data-stu-id="43aec-138">**Enumerating Synchronization Playlists**</span></span>](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





