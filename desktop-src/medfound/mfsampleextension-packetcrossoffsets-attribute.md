---
description: Specifica gli offset ai limiti del payload in un frame per gli esempi protetti.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: Attributo MFSampleExtension_PacketCrossOffsets (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416f41fef9caab3d73c2bdd015d345452ccbd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309089"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a><span data-ttu-id="25d33-103">\_Attributo PacketCrossOffsets di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="25d33-103">MFSampleExtension\_PacketCrossOffsets attribute</span></span>

<span data-ttu-id="25d33-104">Specifica gli offset ai limiti del payload in un frame per gli esempi protetti.</span><span class="sxs-lookup"><span data-stu-id="25d33-104">Specifies the offsets to the payload boundaries in a frame for protected samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="25d33-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="25d33-105">Data type</span></span>

<span data-ttu-id="25d33-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="25d33-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="25d33-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="25d33-107">Get/set</span></span>

<span data-ttu-id="25d33-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="25d33-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="25d33-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="25d33-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="25d33-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="25d33-110">Applies to</span></span>

[<span data-ttu-id="25d33-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="25d33-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="25d33-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="25d33-112">Remarks</span></span>

<span data-ttu-id="25d33-113">Questo attributo si applica agli esempi di supporti protetti da Windows Media Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="25d33-113">This attribute applies to media samples protected by Windows Media Digital Rights Management (DRM).</span></span> <span data-ttu-id="25d33-114">Il valore dell'attributo è una matrice di **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="25d33-114">The value of the attribute is an array of **DWORD** s.</span></span> <span data-ttu-id="25d33-115">Ogni voce nella matrice è l'offset di un limite del payload, relativo all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="25d33-115">Each entry in the array is the offset of a payload boundary, relative to the start of the frame.</span></span> <span data-ttu-id="25d33-116">Un'applicazione può usare questi valori per la decrittografia e la ricostruzione dei frame.</span><span class="sxs-lookup"><span data-stu-id="25d33-116">An application can use these values when decrypting and reconstructing the frames.</span></span>

<span data-ttu-id="25d33-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="25d33-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="25d33-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25d33-118">Requirements</span></span>



| <span data-ttu-id="25d33-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="25d33-119">Requirement</span></span> | <span data-ttu-id="25d33-120">Valore</span><span class="sxs-lookup"><span data-stu-id="25d33-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25d33-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25d33-121">Minimum supported client</span></span><br/> | <span data-ttu-id="25d33-122">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="25d33-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="25d33-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25d33-123">Minimum supported server</span></span><br/> | <span data-ttu-id="25d33-124">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="25d33-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="25d33-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25d33-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="25d33-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="25d33-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25d33-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25d33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25d33-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25d33-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="25d33-129">Barra di divisione ASF</span><span class="sxs-lookup"><span data-stu-id="25d33-129">ASF Splitter</span></span>](asf-splitter.md)
</dt> <dt>

[<span data-ttu-id="25d33-130">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="25d33-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="25d33-131">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="25d33-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




