---
description: Specifica il protocollo di trasporto utilizzato dall'origine di rete.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: Proprietà MFNETSOURCE_TRANSPORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd41653f2b5ea0686527af4d6ee8c8b9962005aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879801"
---
# <a name="mfnetsource_transport-property"></a><span data-ttu-id="12dc5-103">\_Proprietà del trasporto MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="12dc5-103">MFNETSOURCE\_TRANSPORT property</span></span>

<span data-ttu-id="12dc5-104">Specifica il protocollo di trasporto utilizzato dall'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="12dc5-104">Specifies the transport protocol used by the network source.</span></span> <span data-ttu-id="12dc5-105">Il valore di questa proprietà è un membro dell'enumerazione [**del \_ \_ tipo di trasporto MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .</span><span class="sxs-lookup"><span data-stu-id="12dc5-105">The value of this property is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>



<span data-ttu-id="12dc5-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="12dc5-106">Data type</span></span>

<span data-ttu-id="12dc5-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="12dc5-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="12dc5-108">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="12dc5-108">PROPVARIANT member</span></span>

<span data-ttu-id="12dc5-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="12dc5-109">**LONG**</span></span>

<span data-ttu-id="12dc5-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="12dc5-110">VT\_I4</span></span>

<span data-ttu-id="12dc5-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="12dc5-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="12dc5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="12dc5-112">Remarks</span></span>

<span data-ttu-id="12dc5-113">Il **\_ trasporto costante MFNETSOURCE** definisce il GUID per la chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="12dc5-113">The constant **MFNETSOURCE\_TRANSPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="12dc5-114">L'identificatore di proprietà (PID) è zero.</span><span class="sxs-lookup"><span data-stu-id="12dc5-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="12dc5-115">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="12dc5-115">This property is read-only.</span></span> <span data-ttu-id="12dc5-116">Per recuperare questa proprietà, eseguire una query sull'origine di rete per l'interfaccia **IPropertyStore** e chiamare **IPropertyStore:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="12dc5-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="12dc5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12dc5-117">Requirements</span></span>



| <span data-ttu-id="12dc5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="12dc5-118">Requirement</span></span> | <span data-ttu-id="12dc5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="12dc5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="12dc5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12dc5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="12dc5-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12dc5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="12dc5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12dc5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="12dc5-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="12dc5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="12dc5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12dc5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="12dc5-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12dc5-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12dc5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12dc5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12dc5-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12dc5-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="12dc5-128">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12dc5-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="12dc5-129">Protocolli supportati</span><span class="sxs-lookup"><span data-stu-id="12dc5-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




