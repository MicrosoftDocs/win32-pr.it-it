---
description: Tempo di invio di base per il sink del supporto ASF, in millisecondi.
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: Proprietà MFPKEY_ASFMEDIASINK_BASE_SENDTIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320751"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a><span data-ttu-id="f8468-103">MFPKEY \_ ASFMEDIASINK \_ - \_ proprietà di base SENDTIME</span><span class="sxs-lookup"><span data-stu-id="f8468-103">MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME property</span></span>

<span data-ttu-id="f8468-104">Tempo di invio di base per il sink del supporto ASF, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="f8468-104">Base send time for the ASF media sink, in milliseconds.</span></span>



<span data-ttu-id="f8468-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f8468-105">Data type</span></span>

<span data-ttu-id="f8468-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="f8468-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f8468-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f8468-107">PROPVARIANT member</span></span>

<span data-ttu-id="f8468-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="f8468-108">**ULONG**</span></span>

<span data-ttu-id="f8468-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="f8468-109">VT\_UI4</span></span>

<span data-ttu-id="f8468-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="f8468-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f8468-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8468-111">Remarks</span></span>

<span data-ttu-id="f8468-112">L'ora di invio è l'ora in cui un pacchetto ASF viene inviato attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="f8468-112">The send time is the time at which an ASF packet is sent across the network.</span></span> <span data-ttu-id="f8468-113">Non corrisponde direttamente all'ora di presentazione dei dati nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f8468-113">It does not correspond directly to the presentation time of the data in the packet.</span></span>

<span data-ttu-id="f8468-114">È possibile utilizzare questa proprietà per configurare il sink multimediale ASF.</span><span class="sxs-lookup"><span data-stu-id="f8468-114">You can use this property to configure the ASF media sink.</span></span> <span data-ttu-id="f8468-115">L'utilizzo dipende dalla funzione chiamata per creare il sink multimediale ASF:</span><span class="sxs-lookup"><span data-stu-id="f8468-115">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="f8468-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): esegue una query sul puntatore [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperato per l'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="f8468-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="f8468-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sul puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) specificato nel parametro *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="f8468-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8468-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8468-118">Requirements</span></span>



| <span data-ttu-id="f8468-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8468-119">Requirement</span></span> | <span data-ttu-id="f8468-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f8468-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8468-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8468-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f8468-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8468-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f8468-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8468-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f8468-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8468-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f8468-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8468-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8468-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8468-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8468-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8468-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8468-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f8468-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




