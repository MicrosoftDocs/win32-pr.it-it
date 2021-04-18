---
description: Specifica un elenco di velocità in bit e finestre del buffer corrispondenti per un file di formato ASF (Advanced Systems rate) a velocità in bit variabile.
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: Attributo MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7426d15a806a8c61c9a2ea1fdfb0565372c5f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314547"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a><span data-ttu-id="b8258-103">\_Attributo delle \_ \_ coppie di \_ \_ bucket \_ per i metadati di MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="b8258-103">MF\_PD\_ASF\_METADATA\_LEAKY\_BUCKET\_PAIRS attribute</span></span>

<span data-ttu-id="b8258-104">Specifica un elenco di velocità in bit e finestre del buffer corrispondenti per un file di formato ASF (Advanced Systems rate) a velocità in bit variabile.</span><span class="sxs-lookup"><span data-stu-id="b8258-104">Specifies a list of bit rates and corresponding buffer windows for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="b8258-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b8258-105">Data type</span></span>

<span data-ttu-id="b8258-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="b8258-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="b8258-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8258-107">Remarks</span></span>

<span data-ttu-id="b8258-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="b8258-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="b8258-109">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo che si applica al descrittore di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="b8258-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

<span data-ttu-id="b8258-110">Il valore dell'attributo ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="b8258-110">The value of the attribute has the following format:</span></span>

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="b8258-111">La struttura delle coppie di bucket a perdita di WM è definita nel modo seguente: **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b8258-111">The **WM\_LEAKY\_BUCKET\_PAIR** structure is defined as follows:</span></span>

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

<span data-ttu-id="b8258-112">Per ogni velocità in bit, il membro **msBufferWindow** indica la quantità di contenuto memorizzato nel buffer prima che inizi la riproduzione, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="b8258-112">For each bit rate, the **msBufferWindow** member indicates how much content is buffered before playback begins, in milliseconds.</span></span> <span data-ttu-id="b8258-113">La dimensione del buffer in byte equivale a **msBufferWinow** x **dwBitrate** /8000.</span><span class="sxs-lookup"><span data-stu-id="b8258-113">The size of the buffer in bytes equals **msBufferWinow** x **dwBitrate** / 8000.</span></span>

> [!Note]  
> <span data-ttu-id="b8258-114">Questo attributo corrisponde all'attributo **ASFLeakyBucketPairs** in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="b8258-114">This attribute corresponds to the **ASFLeakyBucketPairs** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8258-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8258-115">Requirements</span></span>



| <span data-ttu-id="b8258-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8258-116">Requirement</span></span> | <span data-ttu-id="b8258-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b8258-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8258-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8258-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8258-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8258-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b8258-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8258-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8258-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8258-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b8258-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8258-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8258-123"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8258-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8258-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8258-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8258-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b8258-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b8258-126">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="b8258-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="b8258-127">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="b8258-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="b8258-128">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b8258-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b8258-129">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="b8258-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="b8258-130">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="b8258-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="b8258-131">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="b8258-131">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




