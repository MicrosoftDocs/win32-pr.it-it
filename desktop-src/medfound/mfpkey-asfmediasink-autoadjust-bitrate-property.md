---
description: Specifica se il sink multimediale ASF regola automaticamente la velocità in bit.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: Proprietà MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320752"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a><span data-ttu-id="1696f-103">\_ \_ Proprietà velocità in bit regolazione automatica ASFMEDIASINK MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="1696f-103">MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE property</span></span>

<span data-ttu-id="1696f-104">Specifica se il sink multimediale ASF regola automaticamente la velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="1696f-104">Specifies whether the ASF media sink automatically adjusts the bit rate.</span></span>



<span data-ttu-id="1696f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1696f-105">Data type</span></span>

<span data-ttu-id="1696f-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="1696f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1696f-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="1696f-107">PROPVARIANT member</span></span>

<span data-ttu-id="1696f-108">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="1696f-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="1696f-109">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="1696f-109">VT\_BOOL</span></span>

<span data-ttu-id="1696f-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="1696f-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1696f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1696f-111">Remarks</span></span>

<span data-ttu-id="1696f-112">Se il valore di questa proprietà è VARIANT \_ true, il sink multimediale ASF regola automaticamente la velocità in bit del contenuto ASF in risposta alle caratteristiche dei flussi sottoposto a multiplexing.</span><span class="sxs-lookup"><span data-stu-id="1696f-112">If the value of this property is VARIANT\_TRUE, the ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span>

<span data-ttu-id="1696f-113">Questa proprietà influisce sul comportamento del sink multimediale ASF quando un flusso causa un overflow dei parametri "leaky bucket" del sink:</span><span class="sxs-lookup"><span data-stu-id="1696f-113">This property affects how the ASF media sink behaves when a stream overflows the sink's "leaky bucket" parameters:</span></span>



| <span data-ttu-id="1696f-114">valore</span><span class="sxs-lookup"><span data-stu-id="1696f-114">Value</span></span>              | <span data-ttu-id="1696f-115">Comportamento</span><span class="sxs-lookup"><span data-stu-id="1696f-115">Behavior</span></span>                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1696f-116">**VARIANT \_ true**</span><span class="sxs-lookup"><span data-stu-id="1696f-116">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="1696f-117">Il sink multimediale ASF regola automaticamente la velocità in bit del contenuto ASF in risposta alle caratteristiche dei flussi sottoposte a multiplexing.</span><span class="sxs-lookup"><span data-stu-id="1696f-117">The ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span> |
| <span data-ttu-id="1696f-118">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="1696f-118">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="1696f-119">Il sink multimediale ASF usa il valore della velocità in bit del flusso fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1696f-119">The ASF media sink uses the stream bit rate value provided by the application.</span></span>                                                                |



 

<span data-ttu-id="1696f-120">Il valore predefinito è **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="1696f-120">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="1696f-121">Impostare questa proprietà quando si configura il sink del supporto ASF.</span><span class="sxs-lookup"><span data-stu-id="1696f-121">Set this property when you configure the ASF media sink.</span></span> <span data-ttu-id="1696f-122">L'utilizzo dipende dalla funzione chiamata per creare il sink multimediale ASF:</span><span class="sxs-lookup"><span data-stu-id="1696f-122">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="1696f-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): esegue una query sul puntatore [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperato per l'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="1696f-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="1696f-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sul puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) specificato nel parametro *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="1696f-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

<span data-ttu-id="1696f-125">Se si imposta questa proprietà su VARIANT \_ true, il sink multimediale ASF imposterà il flag di **velocità in bit di MFASF \_ multiplexer \_ AutoAdjust \_** in ASF Multiplexer.</span><span class="sxs-lookup"><span data-stu-id="1696f-125">Setting this property to VARIANT\_TRUE causes the ASF media sink to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag on the ASF multiplexer.</span></span> <span data-ttu-id="1696f-126">Vedere [**IMFASFMultiplexer:: Flags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span><span class="sxs-lookup"><span data-stu-id="1696f-126">See [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span></span>

<span data-ttu-id="1696f-127">Per ulteriori informazioni sul concetto di bucket con perdite, vedere l'argomento relativo al modello di buffer di bucket a perdita nella documentazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="1696f-127">For more information about the leaky bucket concept, see the topic "The Leaky Bucket Buffer Model" in the Windows Media Format SDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="1696f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1696f-128">Requirements</span></span>



| <span data-ttu-id="1696f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1696f-129">Requirement</span></span> | <span data-ttu-id="1696f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="1696f-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1696f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1696f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1696f-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1696f-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1696f-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1696f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1696f-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1696f-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1696f-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1696f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1696f-136"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1696f-136"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1696f-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1696f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1696f-138">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1696f-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1696f-139">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="1696f-139">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[<span data-ttu-id="1696f-140">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="1696f-140">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




