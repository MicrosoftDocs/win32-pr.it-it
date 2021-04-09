---
description: Specifica la qualità di codifica per il sink multimediale Digital Living Network Alliance (DLNA).
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: Attributo MF_MP2DLNA_ENCODE_QUALITY (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c785ff12524d45d096d566014a5c0a5e24eea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050098"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a><span data-ttu-id="678c2-103">\_Attributo MP2DLNA di \_ codifica \_ MF</span><span class="sxs-lookup"><span data-stu-id="678c2-103">MF\_MP2DLNA\_ENCODE\_QUALITY attribute</span></span>

<span data-ttu-id="678c2-104">Specifica la qualità di codifica per il sink multimediale Digital Living Network Alliance (DLNA).</span><span class="sxs-lookup"><span data-stu-id="678c2-104">Specifies the encoding quality for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="678c2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="678c2-105">Data type</span></span>

<span data-ttu-id="678c2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="678c2-106">**UINT32**</span></span>

<span data-ttu-id="678c2-107">Intervallo: 0 – 18</span><span class="sxs-lookup"><span data-stu-id="678c2-107">Range: 0–18</span></span>

## <a name="getset"></a><span data-ttu-id="678c2-108">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="678c2-108">Get/set</span></span>

<span data-ttu-id="678c2-109">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="678c2-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="678c2-110">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="678c2-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="678c2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="678c2-111">Remarks</span></span>

<span data-ttu-id="678c2-112">I numeri più alti indicano una migliore qualità della codifica.</span><span class="sxs-lookup"><span data-stu-id="678c2-112">Higher numbers indicate better encoding quality.</span></span> <span data-ttu-id="678c2-113">I numeri più bassi indicano una codifica più veloce, ma la qualità della codifica è inferiore.</span><span class="sxs-lookup"><span data-stu-id="678c2-113">Lower numbers indicate faster encoding, but lower encoding quality.</span></span> <span data-ttu-id="678c2-114">Il valore predefinito è 9.</span><span class="sxs-lookup"><span data-stu-id="678c2-114">The default value is 9.</span></span>

<span data-ttu-id="678c2-115">Per impostare questo attributo sul sink multimediale DLNA, eseguire una query sul sink multimediale per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="678c2-115">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="678c2-116">Impostare l'attributo prima dell'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="678c2-116">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="678c2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="678c2-117">Requirements</span></span>



| <span data-ttu-id="678c2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="678c2-118">Requirement</span></span> | <span data-ttu-id="678c2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="678c2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="678c2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="678c2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="678c2-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="678c2-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="678c2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="678c2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="678c2-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="678c2-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="678c2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="678c2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="678c2-125"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="678c2-125"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="678c2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="678c2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="678c2-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="678c2-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




