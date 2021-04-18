---
title: Attributo SyncState
description: L'attributo SyncState è una rappresentazione di stringa di un valore a 32 bit utilizzato da Windows Media Player durante la sincronizzazione delle playlist con i dispositivi portatili.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- Attributo SyncState Windows Media Player
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325576"
---
# <a name="syncstate-attribute"></a><span data-ttu-id="706bb-104">Attributo SyncState</span><span class="sxs-lookup"><span data-stu-id="706bb-104">SyncState Attribute</span></span>

<span data-ttu-id="706bb-105">L'attributo **SyncState** è una rappresentazione di stringa di un valore a 32 bit utilizzato da Windows Media Player durante la sincronizzazione delle playlist con i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="706bb-105">The **SyncState** attribute is a string representation of a 32-bit value that Windows Media Player uses when it synchronizes playlists with portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="706bb-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="706bb-106">Applies To</span></span>

-   [<span data-ttu-id="706bb-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="706bb-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="706bb-108">Altri elementi</span><span class="sxs-lookup"><span data-stu-id="706bb-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="706bb-109">Elementi foto</span><span class="sxs-lookup"><span data-stu-id="706bb-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="706bb-110">Elementi video</span><span class="sxs-lookup"><span data-stu-id="706bb-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="706bb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="706bb-111">Remarks</span></span>

<span data-ttu-id="706bb-112">Questo attributo è costituito da valori a 16 2 bit, ciascuno dei quali specifica lo stato di sincronizzazione di un dispositivo portatile.</span><span class="sxs-lookup"><span data-stu-id="706bb-112">This attribute consists of sixteen 2-bit values, each of which specifies the synchronization state of a portable device.</span></span> <span data-ttu-id="706bb-113">Il bit più significativo (MSB) di questo valore a 32 bit corrisponde al dispositivo 16.</span><span class="sxs-lookup"><span data-stu-id="706bb-113">The most significant bit (MSB) of this 32-bit value corresponds to device 16.</span></span> <span data-ttu-id="706bb-114">Il bit meno significativo (LSB) corrisponde al dispositivo 1.</span><span class="sxs-lookup"><span data-stu-id="706bb-114">The least significant bit (LSB) corresponds to device 1.</span></span>

<span data-ttu-id="706bb-115">Il MSB di ogni valore a 2 bit indica se Windows Media Player sincronizzato il contenuto con il dispositivo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="706bb-115">The MSB of each 2-bit value indicates whether Windows Media Player synchronized the content with the corresponding device.</span></span> <span data-ttu-id="706bb-116">Il valore 1 indica che è stato fatto.</span><span class="sxs-lookup"><span data-stu-id="706bb-116">A value of 1 indicates that it did.</span></span> <span data-ttu-id="706bb-117">Il valore 0 indica che non è stato fatto.</span><span class="sxs-lookup"><span data-stu-id="706bb-117">A value of 0 indicates that it did not.</span></span>

<span data-ttu-id="706bb-118">Se MSB è 0, LSB specifica il motivo per cui la sincronizzazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="706bb-118">If the MSB is 0, the LSB specifies why the synchronization failed.</span></span> <span data-ttu-id="706bb-119">Il valore 1 nell'LSB indica che lo spazio disponibile per il contenuto non è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="706bb-119">A value of 1 in the LSB indicates that there was not enough free space for the content.</span></span> <span data-ttu-id="706bb-120">Il valore 0 in LSB indica un altro motivo per cui è stata impedita la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="706bb-120">A value of 0 in the LSB indicates some other reason prevented synchronization.</span></span>

<span data-ttu-id="706bb-121">Per recuperare lo stato di sincronizzazione di un dispositivo specifico, è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="706bb-121">To retrieve the synchronization state of a given device, you should do the following:</span></span>

1.  <span data-ttu-id="706bb-122">Richiamare **\_ lo stato IWMPSyncDevice:: Get** per determinare se un determinato dispositivo è sincronizzato.</span><span class="sxs-lookup"><span data-stu-id="706bb-122">Invoke **IWMPSyncDevice::get\_status** to determine whether a given device is synchronized.</span></span>
2.  <span data-ttu-id="706bb-123">Se è sincronizzato, richiamare **IWMPSyncDevice:: Get \_ partnershipIndex** per recuperare l'indice della coppia di bit del dispositivo nell'attributo **SyncState** .</span><span class="sxs-lookup"><span data-stu-id="706bb-123">If it is synchronized, invoke **IWMPSyncDevice::get\_partnershipIndex** to retrieve the index of the device's bit pair in the **SyncState** attribute.</span></span>
3.  <span data-ttu-id="706bb-124">Usando questo indice, mascherare la coppia di bit corrispondente dell'attributo **SyncState** ed esaminare il risultato per determinare lo stato di sincronizzazione della playlist con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="706bb-124">Using this index, mask the corresponding bit pair of the **SyncState** attribute and examine the result to determine the synchronization state of the playlist with the device.</span></span>

<span data-ttu-id="706bb-125">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="706bb-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="706bb-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="706bb-126">Requirements</span></span>



| <span data-ttu-id="706bb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="706bb-127">Requirement</span></span> | <span data-ttu-id="706bb-128">Valore</span><span class="sxs-lookup"><span data-stu-id="706bb-128">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="706bb-129">Versione</span><span class="sxs-lookup"><span data-stu-id="706bb-129">Version</span></span><br/> | <span data-ttu-id="706bb-130">Windows Media Player 10 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="706bb-130">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="706bb-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="706bb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="706bb-132">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="706bb-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="706bb-133">**Determinazione dello stato di sincronizzazione della playlist**</span><span class="sxs-lookup"><span data-stu-id="706bb-133">**Determining Playlist Synchronization State**</span></span>](determining-playlist-synchronization-state.md)
</dt> <dt>

[<span data-ttu-id="706bb-134">**IWMPSyncDevice:: Get \_ partnershipIndex**</span><span class="sxs-lookup"><span data-stu-id="706bb-134">**IWMPSyncDevice::get\_partnershipIndex**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[<span data-ttu-id="706bb-135">**Stato IWMPSyncDevice:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="706bb-135">**IWMPSyncDevice::get\_status**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





