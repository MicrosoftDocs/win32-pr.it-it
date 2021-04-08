---
description: Ottiene la configurazione dell'altoparlante per i canali audio nel flusso di bit audio.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Proprietà AVAudioChannelConfig (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ee1bc7897d92f7efa1b6d351d2f73c32867529
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048944"
---
# <a name="avaudiochannelconfig-property"></a><span data-ttu-id="aab04-103">Proprietà AVAudioChannelConfig</span><span class="sxs-lookup"><span data-stu-id="aab04-103">AVAudioChannelConfig property</span></span>

<span data-ttu-id="aab04-104">Ottiene la configurazione dell'altoparlante per i canali audio nel flusso di bit audio.</span><span class="sxs-lookup"><span data-stu-id="aab04-104">Gets the speaker configuration for the audio channels in the audio bit stream.</span></span>

<span data-ttu-id="aab04-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="aab04-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="aab04-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="aab04-106">Data type</span></span>

<span data-ttu-id="aab04-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="aab04-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="aab04-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="aab04-108">Property GUID</span></span>

<span data-ttu-id="aab04-109">**Codecapis \_ AVAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="aab04-109">**CODECAPI\_AVAudioChannelConfig**</span></span>

## <a name="property-value"></a><span data-ttu-id="aab04-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aab04-110">Property value</span></span>

<span data-ttu-id="aab04-111">Il valore di questa proprietà è un operatore OR bit per bit dei membri dell'enumerazione [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) .</span><span class="sxs-lookup"><span data-stu-id="aab04-111">The value of this property is a bitwise OR of members of the [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="aab04-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="aab04-112">Remarks</span></span>

<span data-ttu-id="aab04-113">Il numero di canali include il canale LFE (Low Frequency Effect), se presente.</span><span class="sxs-lookup"><span data-stu-id="aab04-113">The number of channels includes the low frequency effect (LFE) channel, if present.</span></span>

## <a name="requirements"></a><span data-ttu-id="aab04-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aab04-114">Requirements</span></span>



| <span data-ttu-id="aab04-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="aab04-115">Requirement</span></span> | <span data-ttu-id="aab04-116">Valore</span><span class="sxs-lookup"><span data-stu-id="aab04-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aab04-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aab04-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aab04-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="aab04-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="aab04-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aab04-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aab04-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aab04-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="aab04-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aab04-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="aab04-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="aab04-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aab04-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aab04-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab04-124">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="aab04-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="aab04-125">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="aab04-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




