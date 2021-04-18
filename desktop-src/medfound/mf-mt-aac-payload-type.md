---
description: Specifica il tipo di payload di un flusso AAC (Advanced Audio Coding).
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: Attributo MF_MT_AAC_PAYLOAD_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324708"
---
# <a name="mf_mt_aac_payload_type-attribute"></a><span data-ttu-id="499bc-103">\_Attributo del \_ \_ tipo di payload MF mt AAC \_</span><span class="sxs-lookup"><span data-stu-id="499bc-103">MF\_MT\_AAC\_PAYLOAD\_TYPE attribute</span></span>

<span data-ttu-id="499bc-104">Specifica il tipo di payload di un flusso AAC (Advanced Audio Coding).</span><span class="sxs-lookup"><span data-stu-id="499bc-104">Specifies the payload type of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="499bc-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="499bc-105">Data type</span></span>

<span data-ttu-id="499bc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="499bc-106">**UINT32**</span></span>

<span data-ttu-id="499bc-107">Sono possibili i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="499bc-107">The following values are possible.</span></span>



| <span data-ttu-id="499bc-108">Valore</span><span class="sxs-lookup"><span data-stu-id="499bc-108">Value</span></span>                                                                        | <span data-ttu-id="499bc-109">Significato</span><span class="sxs-lookup"><span data-stu-id="499bc-109">Meaning</span></span>                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="499bc-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="499bc-110"><dt>0</dt></span></span> </dl> | <span data-ttu-id="499bc-111">Il flusso contiene solo elementi di blocco di dati non elaborati \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="499bc-111">The stream contains raw\_data\_block elements only.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="499bc-112"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="499bc-112"><dt>1</dt></span></span> </dl> | <span data-ttu-id="499bc-113">Flusso di trasporto dati audio (ADTS).</span><span class="sxs-lookup"><span data-stu-id="499bc-113">Audio Data Transport Stream (ADTS).</span></span> <span data-ttu-id="499bc-114">Il flusso contiene una \_ sequenza ADTS, come definito da MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="499bc-114">The stream contains an adts\_sequence, as defined by MPEG-2.</span></span><br/>                       |
| <dl> <span data-ttu-id="499bc-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="499bc-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="499bc-116">Formato di interscambio dati audio (ADIF).</span><span class="sxs-lookup"><span data-stu-id="499bc-116">Audio Data Interchange Format (ADIF).</span></span> <span data-ttu-id="499bc-117">Il flusso contiene una \_ sequenza ADIF, come definito da MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="499bc-117">The stream contains an adif\_sequence, as defined by MPEG-2.</span></span><br/>                     |
| <dl> <span data-ttu-id="499bc-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="499bc-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="499bc-119">Il flusso contiene un flusso di trasporto audio MPEG-4 con un livello di sincronizzazione (LOAS) e un livello multiplex (LATM).</span><span class="sxs-lookup"><span data-stu-id="499bc-119">The stream contains an MPEG-4 audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="499bc-120">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="499bc-120">Get/set</span></span>

<span data-ttu-id="499bc-121">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="499bc-121">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="499bc-122">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="499bc-122">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="499bc-123">Si applica a</span><span class="sxs-lookup"><span data-stu-id="499bc-123">Applies To</span></span>

[<span data-ttu-id="499bc-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="499bc-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="499bc-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="499bc-125">Remarks</span></span>

<span data-ttu-id="499bc-126">Il \_ tipo di payload MF mt \_ AAC \_ \_ è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="499bc-126">MF\_MT\_AAC\_PAYLOAD\_TYPE is optional.</span></span> <span data-ttu-id="499bc-127">Se questo attributo non viene specificato, viene usato il valore predefinito 0, che specifica che il flusso contiene \_ solo elementi di blocco di dati non elaborati \_ .</span><span class="sxs-lookup"><span data-stu-id="499bc-127">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw\_data\_block elements only.</span></span>

<span data-ttu-id="499bc-128">Si applica solo a **MFAudioFormat \_ AAC**.</span><span class="sxs-lookup"><span data-stu-id="499bc-128">Applies only to **MFAudioFormat\_AAC**.</span></span>

<span data-ttu-id="499bc-129">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="499bc-129">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="499bc-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="499bc-130">Requirements</span></span>



| <span data-ttu-id="499bc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="499bc-131">Requirement</span></span> | <span data-ttu-id="499bc-132">Valore</span><span class="sxs-lookup"><span data-stu-id="499bc-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="499bc-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="499bc-133">Header</span></span><br/> | <dl> <span data-ttu-id="499bc-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="499bc-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="499bc-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="499bc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="499bc-136">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="499bc-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="499bc-137">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="499bc-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




