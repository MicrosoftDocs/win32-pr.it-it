---
title: Proprietà _NewEnum IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Recupera un enumeratore per l'insieme. | Proprietà _NewEnum IVMSerialPortCollection (VPCCOMInterfaces. h)
ms.assetid: 4bf7bbde-d97f-424e-afa0-ff0e334740b5
keywords:
- Proprietà _NewEnum Virtual PC
- Proprietà _NewEnum Virtual PC, interfaccia IVMSerialPortCollection
- Interfaccia IVMSerialPortCollection Virtual PC, _NewEnum proprietà
topic_type:
- apiref
api_name:
- IVMSerialPortCollection._NewEnum
- IVMSerialPortCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fdfc2b300823c674cf5d4fd8e36dffeb58f8c1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530804"
---
# <a name="ivmserialportcollection_newenum-property"></a><span data-ttu-id="ebe3b-107">Proprietà IVMSerialPortCollection:: \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="ebe3b-107">IVMSerialPortCollection::\_NewEnum property</span></span>

<span data-ttu-id="ebe3b-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ebe3b-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ebe3b-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ebe3b-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ebe3b-110">Recupera un enumeratore per l'insieme.</span><span class="sxs-lookup"><span data-stu-id="ebe3b-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="ebe3b-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ebe3b-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe3b-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebe3b-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="ebe3b-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ebe3b-113">Property value</span></span>

<span data-ttu-id="ebe3b-114">Enumeratore [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="ebe3b-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ebe3b-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ebe3b-115">Error codes</span></span>



| <span data-ttu-id="ebe3b-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="ebe3b-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="ebe3b-117">Significato</span><span class="sxs-lookup"><span data-stu-id="ebe3b-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="ebe3b-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ebe3b-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ebe3b-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ebe3b-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="ebe3b-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ebe3b-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ebe3b-121">Il parametro è NULL.</span><span class="sxs-lookup"><span data-stu-id="ebe3b-121">The parameter is NULL.</span></span><br/>        |
| <dl> <span data-ttu-id="ebe3b-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ebe3b-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ebe3b-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="ebe3b-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ebe3b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebe3b-124">Requirements</span></span>



| <span data-ttu-id="ebe3b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebe3b-125">Requirement</span></span> | <span data-ttu-id="ebe3b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ebe3b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe3b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebe3b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ebe3b-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ebe3b-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ebe3b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebe3b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ebe3b-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ebe3b-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ebe3b-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ebe3b-131">End of client support</span></span><br/>    | <span data-ttu-id="ebe3b-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ebe3b-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ebe3b-133">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ebe3b-133">Product</span></span><br/>                  | <span data-ttu-id="ebe3b-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ebe3b-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ebe3b-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebe3b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebe3b-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebe3b-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ebe3b-137">IID</span><span class="sxs-lookup"><span data-stu-id="ebe3b-137">IID</span></span><br/>                      | <span data-ttu-id="ebe3b-138">IID \_ IVMSerialPortCollection è definito come dd3c6175-1F04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="ebe3b-138">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="ebe3b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebe3b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe3b-140">**IVMSerialPortCollection**</span><span class="sxs-lookup"><span data-stu-id="ebe3b-140">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

