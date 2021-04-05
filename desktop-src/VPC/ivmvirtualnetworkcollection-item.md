---
title: Proprietà Item di IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Oggetto IVMVirtualNetwork che corrisponde all'indice specificato.
ms.assetid: 1c6a3449-f76a-4216-8840-0fb9fb133e67
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMVirtualNetworkCollection
- Interfaccia IVMVirtualNetworkCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Item
- IVMVirtualNetworkCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac5a7648db4708fbc1b445029419ee794809abcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048456"
---
# <a name="ivmvirtualnetworkcollectionitem-property"></a><span data-ttu-id="6c6a1-106">Proprietà IVMVirtualNetworkCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="6c6a1-106">IVMVirtualNetworkCollection::Item property</span></span>

<span data-ttu-id="6c6a1-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6c6a1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6c6a1-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6c6a1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6c6a1-109">Recupera l'oggetto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="6c6a1-109">Retrieves the [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="6c6a1-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6c6a1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6a1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c6a1-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="6c6a1-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6c6a1-112">Property value</span></span>

<span data-ttu-id="6c6a1-113">Oggetto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="6c6a1-113">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6c6a1-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="6c6a1-114">Error codes</span></span>



| <span data-ttu-id="6c6a1-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="6c6a1-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6c6a1-116">Significato</span><span class="sxs-lookup"><span data-stu-id="6c6a1-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c6a1-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6c6a1-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="6c6a1-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="6c6a1-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6c6a1-120">Il parametro *virtualNetwork* è **null**.</span><span class="sxs-lookup"><span data-stu-id="6c6a1-120">The *virtualNetwork* parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="6c6a1-121"><dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a1-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="6c6a1-122">L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="6c6a1-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="6c6a1-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6c6a1-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6c6a1-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="6c6a1-124">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="6c6a1-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c6a1-125">Requirements</span></span>



| <span data-ttu-id="6c6a1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c6a1-126">Requirement</span></span> | <span data-ttu-id="6c6a1-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6c6a1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6a1-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c6a1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6c6a1-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6c6a1-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c6a1-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c6a1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6c6a1-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6c6a1-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6c6a1-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6c6a1-132">End of client support</span></span><br/>    | <span data-ttu-id="6c6a1-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6c6a1-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="6c6a1-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6c6a1-134">Product</span></span><br/>                  | <span data-ttu-id="6c6a1-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6c6a1-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="6c6a1-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c6a1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c6a1-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c6a1-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="6c6a1-138">IID</span><span class="sxs-lookup"><span data-stu-id="6c6a1-138">IID</span></span><br/>                      | <span data-ttu-id="6c6a1-139">IID \_ IVMVirtualNetworkCollection è definito come 8ed680be-4242-4B2A-A21C-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="6c6a1-139">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c6a1-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c6a1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6a1-141">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="6c6a1-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> <dt>

[<span data-ttu-id="6c6a1-142">**IVMVirtualNetworkCollection**</span><span class="sxs-lookup"><span data-stu-id="6c6a1-142">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

