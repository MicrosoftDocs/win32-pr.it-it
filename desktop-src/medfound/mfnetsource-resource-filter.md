---
description: Contiene un puntatore all'interfaccia di callback IMFNetResourceFilter per il flusso di byte HTTP Microsoft Media Foundation.
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: Proprietà MFNETSOURCE_RESOURCE_FILTER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754258"
---
# <a name="mfnetsource_resource_filter-property"></a><span data-ttu-id="358b1-103">\_Proprietà del \_ filtro risorse MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="358b1-103">MFNETSOURCE\_RESOURCE\_FILTER property</span></span>

<span data-ttu-id="358b1-104">Contiene un puntatore all'interfaccia di callback [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) per il flusso di byte http Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="358b1-104">Contains a pointer to the [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) callback interface for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="358b1-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="358b1-105">Data type</span></span>

<span data-ttu-id="358b1-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="358b1-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="358b1-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="358b1-107">PROPVARIANT member</span></span>

<span data-ttu-id="358b1-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="358b1-108">\**IUnknown\** _</span></span>

<span data-ttu-id="358b1-109">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="358b1-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="358b1-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="358b1-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="358b1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="358b1-111">Remarks</span></span>

<span data-ttu-id="358b1-112">Usare questa proprietà per configurare il flusso di byte HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="358b1-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="358b1-113">Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="358b1-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="358b1-114">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="358b1-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="358b1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="358b1-115">Requirements</span></span>



| <span data-ttu-id="358b1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="358b1-116">Requirement</span></span> | <span data-ttu-id="358b1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="358b1-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="358b1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="358b1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="358b1-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="358b1-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="358b1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="358b1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="358b1-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="358b1-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="358b1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="358b1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="358b1-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="358b1-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="358b1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="358b1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="358b1-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="358b1-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
