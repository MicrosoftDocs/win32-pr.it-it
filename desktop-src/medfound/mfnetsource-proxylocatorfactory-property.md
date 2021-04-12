---
description: Contiene un puntatore all'interfaccia IMFNetProxyLocatorFactory.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: Proprietà MFNETSOURCE_PROXYLOCATORFACTORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1199333e9eb343ab9d8f96864372b2dc385ab7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130711"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a><span data-ttu-id="76089-103">\_Proprietà PROXYLOCATORFACTORY di MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="76089-103">MFNETSOURCE\_PROXYLOCATORFACTORY property</span></span>

<span data-ttu-id="76089-104">Contiene un puntatore all'interfaccia [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="76089-104">Contains a pointer to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>



<span data-ttu-id="76089-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="76089-105">Data type</span></span>

<span data-ttu-id="76089-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="76089-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="76089-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="76089-107">PROPVARIANT member</span></span>

<span data-ttu-id="76089-108">Puntatore **IUnknown**</span><span class="sxs-lookup"><span data-stu-id="76089-108">**IUnknown** pointer</span></span>

<span data-ttu-id="76089-109">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="76089-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="76089-110">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="76089-110">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="76089-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="76089-111">Remarks</span></span>

<span data-ttu-id="76089-112">La costante **MFNETSOURCE \_ PROXYLOCATORFACTORY** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="76089-112">The constant **MFNETSOURCE\_PROXYLOCATORFACTORY** defines the GUID for this property key.</span></span> <span data-ttu-id="76089-113">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="76089-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="76089-114">Le applicazioni possono usare questa proprietà per fornire un localizzatore proxy personalizzato per l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="76089-114">Applications can use this property to provide a custom proxy locator for the network source.</span></span> <span data-ttu-id="76089-115">Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="76089-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="76089-116">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="76089-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76089-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76089-117">Requirements</span></span>



| <span data-ttu-id="76089-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="76089-118">Requirement</span></span> | <span data-ttu-id="76089-119">Valore</span><span class="sxs-lookup"><span data-stu-id="76089-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76089-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76089-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76089-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76089-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="76089-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76089-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76089-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76089-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="76089-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76089-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="76089-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="76089-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76089-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76089-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76089-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76089-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="76089-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76089-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="76089-129">Supporto del proxy per le origini di rete</span><span class="sxs-lookup"><span data-stu-id="76089-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




