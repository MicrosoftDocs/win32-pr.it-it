---
description: "Proprietà AVDecAudioDualMono: specifica se l'audio a 2 canali è codificato come stereo o doppio mono."
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Proprietà AVDecAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc84e19d41840b358e3e79576152dbc8527e2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096569"
---
# <a name="avdecaudiodualmono-property"></a><span data-ttu-id="4090b-103">AVDecAudioDualMono - proprietà</span><span class="sxs-lookup"><span data-stu-id="4090b-103">AVDecAudioDualMono property</span></span>

<span data-ttu-id="4090b-104">Specifica se l'audio a 2 canali è codificato come stereo o doppio mono.</span><span class="sxs-lookup"><span data-stu-id="4090b-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="4090b-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4090b-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="4090b-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4090b-106">Data type</span></span>

<span data-ttu-id="4090b-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="4090b-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4090b-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="4090b-108">Property GUID</span></span>

<span data-ttu-id="4090b-109">**CODECAPI \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="4090b-109">**CODECAPI\_AVDecAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="4090b-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4090b-110">Property value</span></span>

<span data-ttu-id="4090b-111">Il valore di questa proprietà è un membro [**dell'enumerazione eAVDecAudioDualMono.**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)</span><span class="sxs-lookup"><span data-stu-id="4090b-111">The value of this property is a member of the [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="4090b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4090b-112">Remarks</span></span>

<span data-ttu-id="4090b-113">Questa proprietà si applica solo quando il flusso di bit di input del decodificatore contiene audio a due canali.</span><span class="sxs-lookup"><span data-stu-id="4090b-113">This property applies only when the decoder's input bit stream contains two-channel audio.</span></span> <span data-ttu-id="4090b-114">Un flusso audio a due canali può essere codificato come stereo o come doppio mono.</span><span class="sxs-lookup"><span data-stu-id="4090b-114">A two-channel audio stream might be encoded as stereo or as dual mono.</span></span> <span data-ttu-id="4090b-115">Se l'audio è doppio mono, è possibile impostare la proprietà [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) per configurare il modo in cui il decodificatore riproduce l'audio.</span><span class="sxs-lookup"><span data-stu-id="4090b-115">If the audio is dual mono, you can set the [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) property to configure how the decoder reproduces the audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="4090b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4090b-116">Requirements</span></span>



| <span data-ttu-id="4090b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4090b-117">Requirement</span></span> | <span data-ttu-id="4090b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4090b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4090b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4090b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4090b-120">App \[ desktop UWP di Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="4090b-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4090b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4090b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4090b-122">App UWP per app desktop di Windows 2000 Server \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="4090b-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4090b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4090b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4090b-124"><dt>Codecapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="4090b-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4090b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4090b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4090b-126">Proprietà API codec</span><span class="sxs-lookup"><span data-stu-id="4090b-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="4090b-127">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="4090b-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




