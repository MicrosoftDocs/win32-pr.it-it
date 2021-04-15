---
title: Proprietà ResourceLocator. FragmentDialect (WSManDisp. h)
description: Ottiene o imposta il dialetto del linguaggio per un sottolinguaggio di frammenti di risorse quando ResourceLocator viene utilizzato nelle operazioni di oggetti sessione come Session. Get, Session. put o Session. enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà FragmentDialect
- Gestione remota Windows proprietà FragmentDialect, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, proprietà FragmentDialect
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478784"
---
# <a name="resourcelocatorfragmentdialect-property"></a><span data-ttu-id="490df-106">Proprietà ResourceLocator. FragmentDialect</span><span class="sxs-lookup"><span data-stu-id="490df-106">ResourceLocator.FragmentDialect property</span></span>

<span data-ttu-id="490df-107">Ottiene o imposta il dialetto del linguaggio per un *sottolinguaggio* di [*frammenti*](windows-remote-management-glossary.md) di [*risorse*](windows-remote-management-glossary.md) quando [**resourceLocator**](resourcelocator.md) viene utilizzato nelle operazioni di oggetti [**sessione**](session.md) come [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="490df-107">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) *dialect* when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="490df-108">Un frammento rappresenta una proprietà o una parte di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="490df-108">A fragment represents one property or part of a resource.</span></span> <span data-ttu-id="490df-109">È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="490df-109">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="490df-110">Il dialetto indica il linguaggio XML che descrive il frammento al servizio che implementa l' [protocollo WS-Management](ws-management-protocol.md) e riceve la richiesta.</span><span class="sxs-lookup"><span data-stu-id="490df-110">The dialect indicates what XML language describes the fragment to the service that implements the [WS-Management Protocol](ws-management-protocol.md) and receives the request.</span></span>

<span data-ttu-id="490df-111">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="490df-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="490df-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="490df-112">Syntax</span></span>


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a><span data-ttu-id="490df-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="490df-113">Property value</span></span>

<span data-ttu-id="490df-114">Stringa XML che identifica la lingua utilizzata nella proprietà [**FragmentPath**](resourcelocator-fragmentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="490df-114">An XML string that identifies the language used in the [**FragmentPath**](resourcelocator-fragmentpath.md) property.</span></span> <span data-ttu-id="490df-115">Per impostazione predefinita, la stringa di dialetto è la specifica XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="490df-115">The dialect string defaults to the XPath 1.0 specification.</span></span> <span data-ttu-id="490df-116">Per altre informazioni, vedere [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="490df-116">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="remarks"></a><span data-ttu-id="490df-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="490df-117">Remarks</span></span>

<span data-ttu-id="490df-118">[**IWSManResourceLocator:: FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) è la proprietà C++ corrispondente.</span><span class="sxs-lookup"><span data-stu-id="490df-118">[**IWSManResourceLocator::FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="490df-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="490df-119">Requirements</span></span>



| <span data-ttu-id="490df-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="490df-120">Requirement</span></span> | <span data-ttu-id="490df-121">Valore</span><span class="sxs-lookup"><span data-stu-id="490df-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="490df-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="490df-122">Minimum supported client</span></span><br/> | <span data-ttu-id="490df-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="490df-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="490df-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="490df-124">Minimum supported server</span></span><br/> | <span data-ttu-id="490df-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="490df-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="490df-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="490df-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="490df-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="490df-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="490df-128">IDL</span><span class="sxs-lookup"><span data-stu-id="490df-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="490df-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="490df-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="490df-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="490df-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="490df-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="490df-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="490df-132">DLL</span><span class="sxs-lookup"><span data-stu-id="490df-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="490df-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="490df-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="490df-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="490df-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="490df-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="490df-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





