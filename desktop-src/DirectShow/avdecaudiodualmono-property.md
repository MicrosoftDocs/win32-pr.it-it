---
description: Specifica se l'audio a 2 canali è codificato come stereo o doppia mono.
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Proprietà AVDecAudioDualMono (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 107adb00eb68cbb9ec19331b0c0f3f9db916a306
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876854"
---
# <a name="avdecaudiodualmono-property"></a><span data-ttu-id="65699-103">Proprietà AVDecAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="65699-103">AVDecAudioDualMono property</span></span>

<span data-ttu-id="65699-104">Specifica se l'audio a 2 canali è codificato come stereo o doppia mono.</span><span class="sxs-lookup"><span data-stu-id="65699-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="65699-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="65699-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="65699-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="65699-106">Data type</span></span>

<span data-ttu-id="65699-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="65699-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="65699-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="65699-108">Property GUID</span></span>

<span data-ttu-id="65699-109">**Codecapis \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="65699-109">**CODECAPI\_AVDecAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="65699-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="65699-110">Property value</span></span>

<span data-ttu-id="65699-111">Il valore di questa proprietà è un membro dell'enumerazione [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) .</span><span class="sxs-lookup"><span data-stu-id="65699-111">The value of this property is a member of the [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="65699-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="65699-112">Remarks</span></span>

<span data-ttu-id="65699-113">Questa proprietà si applica solo quando il flusso di bit di input del decodificatore contiene audio a due canali.</span><span class="sxs-lookup"><span data-stu-id="65699-113">This property applies only when the decoder's input bit stream contains two-channel audio.</span></span> <span data-ttu-id="65699-114">Un flusso audio a due canali può essere codificato come stereo o come doppio mono.</span><span class="sxs-lookup"><span data-stu-id="65699-114">A two-channel audio stream might be encoded as stereo or as dual mono.</span></span> <span data-ttu-id="65699-115">Se l'audio è dual mono, è possibile impostare la proprietà [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) per configurare la modalità di riproduzione dell'audio da parte del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="65699-115">If the audio is dual mono, you can set the [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) property to configure how the decoder reproduces the audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="65699-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65699-116">Requirements</span></span>



| <span data-ttu-id="65699-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="65699-117">Requirement</span></span> | <span data-ttu-id="65699-118">Valore</span><span class="sxs-lookup"><span data-stu-id="65699-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65699-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65699-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65699-120">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="65699-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="65699-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65699-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65699-122">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="65699-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="65699-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65699-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="65699-124"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="65699-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65699-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65699-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65699-126">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="65699-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="65699-127">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="65699-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




