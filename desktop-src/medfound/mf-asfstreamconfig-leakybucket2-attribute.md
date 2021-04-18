---
description: Imposta il picco &\# 0034; bucket a perdita&\# 0034; parametri (vedere la sezione Osservazioni) per la codifica di un file di Windows Media. Questi parametri vengono usati per la velocità in bit di picco. Impostare questo attributo usando l'interfaccia IMFASFStreamConfig.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: Attributo MF_ASFSTREAMCONFIG_LEAKYBUCKET2 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c4cca3252d543d35bef37d70dcb612c24df6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314550"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a><span data-ttu-id="68364-105">\_Attributo MF ASFSTREAMCONFIG \_ LEAKYBUCKET2</span><span class="sxs-lookup"><span data-stu-id="68364-105">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2 attribute</span></span>

<span data-ttu-id="68364-106">Imposta il picco dei parametri "leaky bucket" (vedere la sezione Osservazioni) per la codifica di un file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="68364-106">Sets the peak "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="68364-107">Questi parametri vengono usati per la velocità in bit di picco.</span><span class="sxs-lookup"><span data-stu-id="68364-107">These parameters are used for the peak bit rate.</span></span> <span data-ttu-id="68364-108">Impostare questo attributo usando l'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="68364-108">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="68364-109">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="68364-109">Data type</span></span>

<span data-ttu-id="68364-110">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="68364-110">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="68364-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="68364-111">Remarks</span></span>

<span data-ttu-id="68364-112">Il valore di questo attributo è una matrice di tre **DWORD** s, nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="68364-112">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="68364-113">Velocità in bit, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="68364-113">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="68364-114">Finestra buffer, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="68364-114">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="68364-115">Completezza del buffer iniziale, in byte.</span><span class="sxs-lookup"><span data-stu-id="68364-115">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="68364-116">Per ulteriori informazioni sul concetto di bucket con perdite, vedere l'argomento [modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md) nella documentazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="68364-116">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="68364-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="68364-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68364-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68364-118">Requirements</span></span>



| <span data-ttu-id="68364-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="68364-119">Requirement</span></span> | <span data-ttu-id="68364-120">Valore</span><span class="sxs-lookup"><span data-stu-id="68364-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68364-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68364-121">Minimum supported client</span></span><br/> | <span data-ttu-id="68364-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68364-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="68364-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68364-123">Minimum supported server</span></span><br/> | <span data-ttu-id="68364-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68364-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="68364-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68364-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="68364-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="68364-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68364-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68364-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68364-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68364-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68364-129">Attributi ASF</span><span class="sxs-lookup"><span data-stu-id="68364-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="68364-130">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="68364-130">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="68364-131">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="68364-131">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="68364-132">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="68364-132">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




