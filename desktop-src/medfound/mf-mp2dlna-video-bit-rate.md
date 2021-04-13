---
description: Specifica la velocità in bit massima del video per il sink multimediale Digital Living Network Alliance (DLNA).
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: Attributo MF_MP2DLNA_VIDEO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226642"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a><span data-ttu-id="008d0-103">\_ \_ \_ Attributo velocità in bit del video MF MP2DLNA \_</span><span class="sxs-lookup"><span data-stu-id="008d0-103">MF\_MP2DLNA\_VIDEO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="008d0-104">Specifica la velocità in bit massima del video per il sink multimediale Digital Living Network Alliance (DLNA).</span><span class="sxs-lookup"><span data-stu-id="008d0-104">Specifies the maximum video bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="008d0-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="008d0-105">Data type</span></span>

<span data-ttu-id="008d0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="008d0-106">**UINT32**</span></span>

<span data-ttu-id="008d0-107">Il valore è la velocità in bit massima di destinazione per il flusso video codificato, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="008d0-107">The value is the target maximum bit rate for the encoded video stream, in bits per second.</span></span> <span data-ttu-id="008d0-108">Il valore massimo è 9,8 milioni (9,8 Mbps), che è anche il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="008d0-108">The maximum value is 9800000 (9.8 Mbps), which is also the default value.</span></span>

## <a name="getset"></a><span data-ttu-id="008d0-109">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="008d0-109">Get/set</span></span>

<span data-ttu-id="008d0-110">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="008d0-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="008d0-111">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="008d0-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="008d0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="008d0-112">Remarks</span></span>

<span data-ttu-id="008d0-113">Per impostare questo attributo sul sink multimediale DLNA, eseguire una query sul sink multimediale per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="008d0-113">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="008d0-114">Impostare l'attributo prima dell'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="008d0-114">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="008d0-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="008d0-115">Requirements</span></span>



| <span data-ttu-id="008d0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="008d0-116">Requirement</span></span> | <span data-ttu-id="008d0-117">Valore</span><span class="sxs-lookup"><span data-stu-id="008d0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="008d0-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="008d0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="008d0-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="008d0-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="008d0-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="008d0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="008d0-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="008d0-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="008d0-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="008d0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="008d0-123"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="008d0-123"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="008d0-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="008d0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="008d0-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="008d0-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




