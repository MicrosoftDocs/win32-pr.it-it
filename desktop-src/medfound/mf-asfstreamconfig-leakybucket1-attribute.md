---
description: Imposta la media &\# 0034; bucket a perdita&\# 0034; parametri (vedere la sezione Osservazioni) per la codifica di un file di Windows Media. Impostare questo attributo usando l'interfaccia IMFASFStreamConfig.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: Attributo MF_ASFSTREAMCONFIG_LEAKYBUCKET1 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309592"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a><span data-ttu-id="06abf-104">\_Attributo MF ASFSTREAMCONFIG \_ LEAKYBUCKET1</span><span class="sxs-lookup"><span data-stu-id="06abf-104">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1 attribute</span></span>

<span data-ttu-id="06abf-105">Imposta i parametri medi "bucket Leak" (vedere le note) per la codifica di un file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="06abf-105">Sets the average "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="06abf-106">Impostare questo attributo usando l'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="06abf-106">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="06abf-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="06abf-107">Data type</span></span>

<span data-ttu-id="06abf-108">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="06abf-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="06abf-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="06abf-109">Remarks</span></span>

<span data-ttu-id="06abf-110">Il valore di questo attributo è una matrice di tre **DWORD** s, nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="06abf-110">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="06abf-111">Velocità in bit, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="06abf-111">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="06abf-112">Finestra buffer, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="06abf-112">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="06abf-113">Completezza del buffer iniziale, in byte.</span><span class="sxs-lookup"><span data-stu-id="06abf-113">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="06abf-114">Per ulteriori informazioni sul concetto di bucket con perdite, vedere l'argomento [modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md) nella documentazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="06abf-114">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="06abf-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="06abf-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="06abf-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06abf-116">Requirements</span></span>



| <span data-ttu-id="06abf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="06abf-117">Requirement</span></span> | <span data-ttu-id="06abf-118">Valore</span><span class="sxs-lookup"><span data-stu-id="06abf-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06abf-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06abf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="06abf-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06abf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="06abf-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06abf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="06abf-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06abf-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="06abf-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06abf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="06abf-124"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="06abf-124"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06abf-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06abf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06abf-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06abf-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="06abf-127">Attributi ASF</span><span class="sxs-lookup"><span data-stu-id="06abf-127">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="06abf-128">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="06abf-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="06abf-129">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="06abf-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="06abf-130">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="06abf-130">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




