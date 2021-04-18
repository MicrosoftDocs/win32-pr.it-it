---
title: Attributo SyncOnly
description: L'attributo SyncOnly è una rappresentazione di stringa di un valore booleano usato da Windows Media Player per determinare se una playlist è disponibile solo per la sincronizzazione.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Attributo SyncOnly Windows Media Player
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325579"
---
# <a name="synconly-attribute"></a><span data-ttu-id="113db-104">Attributo SyncOnly</span><span class="sxs-lookup"><span data-stu-id="113db-104">SyncOnly Attribute</span></span>

<span data-ttu-id="113db-105">L'attributo **SyncOnly** è una rappresentazione di stringa di un valore **booleano** usato da Windows Media Player per determinare se una playlist è disponibile solo per la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="113db-105">The **SyncOnly** attribute is a string representation of a **Boolean** value that Windows Media Player uses to determine whether a playlist is available only for synchronization.</span></span>

## <a name="applies-to"></a><span data-ttu-id="113db-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="113db-106">Applies To</span></span>

-   [<span data-ttu-id="113db-107">Playlist</span><span class="sxs-lookup"><span data-stu-id="113db-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="113db-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="113db-108">Remarks</span></span>

<span data-ttu-id="113db-109">Il valore 1 indica che la playlist è disponibile solo per la sincronizzazione e non può essere visualizzata nel nodo **playlist automatico** .</span><span class="sxs-lookup"><span data-stu-id="113db-109">A value of 1 indicates that the playlist is available only for synchronization and cannot appear in the **Auto Playlist** node.</span></span> <span data-ttu-id="113db-110">Un valore pari a zero indica che la playlist può essere visualizzata nel nodo **playlist automatico** .</span><span class="sxs-lookup"><span data-stu-id="113db-110">A value of zero indicates that the playlist can appear in the **Auto Playlist** node.</span></span>

<span data-ttu-id="113db-111">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="113db-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="113db-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="113db-112">Requirements</span></span>



| <span data-ttu-id="113db-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="113db-113">Requirement</span></span> | <span data-ttu-id="113db-114">Valore</span><span class="sxs-lookup"><span data-stu-id="113db-114">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="113db-115">Versione</span><span class="sxs-lookup"><span data-stu-id="113db-115">Version</span></span><br/> | <span data-ttu-id="113db-116">Windows Media Player 10 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="113db-116">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="113db-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="113db-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113db-118">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="113db-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





