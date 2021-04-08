---
description: Specifica il modo in cui il sink multimediale ASF deve applicare Windows Media DRM.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: Proprietà MFPKEY_ASFMEDIASINK_DRMACTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761477"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a><span data-ttu-id="1af4f-103">MFPKEY \_ ASFMEDIASINK- \_ Proprietà DRMACTION</span><span class="sxs-lookup"><span data-stu-id="1af4f-103">MFPKEY\_ASFMEDIASINK\_DRMACTION property</span></span>

<span data-ttu-id="1af4f-104">Specifica il modo in cui il sink multimediale ASF deve applicare Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="1af4f-104">Specifies how the ASF media sink should apply Windows Media DRM.</span></span>



<span data-ttu-id="1af4f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1af4f-105">Data type</span></span>

<span data-ttu-id="1af4f-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="1af4f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1af4f-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="1af4f-107">PROPVARIANT member</span></span>

<span data-ttu-id="1af4f-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="1af4f-108">**ULONG**</span></span>

<span data-ttu-id="1af4f-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="1af4f-109">VT\_UI4</span></span>

<span data-ttu-id="1af4f-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="1af4f-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1af4f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1af4f-111">Remarks</span></span>

<span data-ttu-id="1af4f-112">Il valore di questa proprietà è un membro dell'enumerazione [**MFSINK \_ WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) .</span><span class="sxs-lookup"><span data-stu-id="1af4f-112">The value of this property is a member of the [**MFSINK\_WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) enumeration.</span></span>

<span data-ttu-id="1af4f-113">È possibile utilizzare questo attributo per configurare il sink del supporto ASF.</span><span class="sxs-lookup"><span data-stu-id="1af4f-113">You can use this attribute to configure the ASF media sink.</span></span> <span data-ttu-id="1af4f-114">L'utilizzo dipende dalla funzione chiamata per creare il sink multimediale ASF:</span><span class="sxs-lookup"><span data-stu-id="1af4f-114">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="1af4f-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): esegue una query sul puntatore [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperato per l'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="1af4f-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="1af4f-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sul puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) specificato nel parametro *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="1af4f-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="1af4f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1af4f-117">Requirements</span></span>



| <span data-ttu-id="1af4f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1af4f-118">Requirement</span></span> | <span data-ttu-id="1af4f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1af4f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1af4f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1af4f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1af4f-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1af4f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1af4f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1af4f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1af4f-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1af4f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1af4f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1af4f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1af4f-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1af4f-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af4f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1af4f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af4f-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1af4f-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
