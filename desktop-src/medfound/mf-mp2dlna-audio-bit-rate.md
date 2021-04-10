---
description: Specifica la velocità in bit audio massima per il sink del supporto Digital Living Network Alliance (DLNA).
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: Attributo MF_MP2DLNA_AUDIO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c61554f592aefbb863057339d807e23fc96567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967042"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a><span data-ttu-id="6b03d-103">\_ \_ \_ Attributo velocità in bit \_ audio MF MP2DLNA</span><span class="sxs-lookup"><span data-stu-id="6b03d-103">MF\_MP2DLNA\_AUDIO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="6b03d-104">Specifica la velocità in bit audio massima per il sink del supporto Digital Living Network Alliance (DLNA).</span><span class="sxs-lookup"><span data-stu-id="6b03d-104">Specifies the maximum audio bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="6b03d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6b03d-105">Data type</span></span>

<span data-ttu-id="6b03d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6b03d-106">**UINT32**</span></span>

<span data-ttu-id="6b03d-107">Il valore è la velocità in bit massima di destinazione per il flusso audio codificato, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="6b03d-107">The value is the target maximum bit rate for the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="6b03d-108">Il valore deve essere una delle velocità in bit consentite per l'audio MPEG-2 Layer 2 per DLNA.</span><span class="sxs-lookup"><span data-stu-id="6b03d-108">The value must be one of the bit rates allowed for MPEG-2 layer 2 audio for DLNA.</span></span> <span data-ttu-id="6b03d-109">Il valore predefinito è 192000 (192 Kbps).</span><span class="sxs-lookup"><span data-stu-id="6b03d-109">The default value is 192000 (192 Kbps).</span></span>

## <a name="getset"></a><span data-ttu-id="6b03d-110">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="6b03d-110">Get/set</span></span>

<span data-ttu-id="6b03d-111">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6b03d-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6b03d-112">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="6b03d-112">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b03d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b03d-113">Remarks</span></span>

<span data-ttu-id="6b03d-114">Per impostare questo attributo sul sink multimediale DLNA, eseguire una query sul sink multimediale per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="6b03d-114">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="6b03d-115">Impostare l'attributo prima dell'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="6b03d-115">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b03d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b03d-116">Requirements</span></span>



| <span data-ttu-id="6b03d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b03d-117">Requirement</span></span> | <span data-ttu-id="6b03d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6b03d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b03d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b03d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6b03d-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6b03d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6b03d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b03d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6b03d-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b03d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6b03d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b03d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b03d-124"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b03d-124"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b03d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b03d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b03d-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b03d-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




