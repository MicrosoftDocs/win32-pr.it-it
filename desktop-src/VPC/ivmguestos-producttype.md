---
title: Proprietà IVMGuestOS ProductType (VPCCOMInterfaces. h)
description: Recupera il tipo di prodotto del sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- Proprietà ProductType Virtual PC
- Proprietà ProductType Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà ProductType
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301564"
---
# <a name="ivmguestosproducttype-property"></a><span data-ttu-id="fb9a2-106">IVMGuestOS::P proprietà roductType</span><span class="sxs-lookup"><span data-stu-id="fb9a2-106">IVMGuestOS::ProductType property</span></span>

<span data-ttu-id="fb9a2-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fb9a2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fb9a2-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fb9a2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fb9a2-109">Recupera il tipo di prodotto del sistema operativo guest in esecuzione nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb9a2-109">Retrieves the product type of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="fb9a2-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fb9a2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb9a2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb9a2-111">Syntax</span></span>


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a><span data-ttu-id="fb9a2-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fb9a2-112">Property value</span></span>

<span data-ttu-id="fb9a2-113">Tipo di prodotto.</span><span class="sxs-lookup"><span data-stu-id="fb9a2-113">The product type.</span></span> <span data-ttu-id="fb9a2-114">Sono supportati i valori stringa seguenti.</span><span class="sxs-lookup"><span data-stu-id="fb9a2-114">The following string values are supported.</span></span>



| <span data-ttu-id="fb9a2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fb9a2-115">Value</span></span>                                                                                  | <span data-ttu-id="fb9a2-116">Significato</span><span class="sxs-lookup"><span data-stu-id="fb9a2-116">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb9a2-117"><dt>"0x0000002"</dt></span><span class="sxs-lookup"><span data-stu-id="fb9a2-117"><dt>"0x0000002"</dt></span></span> </dl> | <span data-ttu-id="fb9a2-118">Il sistema è un controller di dominio e il sistema operativo è Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fb9a2-118">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="fb9a2-119"><dt>"0x0000003"</dt></span><span class="sxs-lookup"><span data-stu-id="fb9a2-119"><dt>"0x0000003"</dt></span></span> </dl> | <span data-ttu-id="fb9a2-120">Il sistema operativo è Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fb9a2-120">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="fb9a2-121">Si noti che un server che è anche un controller di dominio viene segnalato come **\_ controller di \_ dominio \_ ver NT**, non come **\_ \_ Server ver NT**.</span><span class="sxs-lookup"><span data-stu-id="fb9a2-121">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <dl> <span data-ttu-id="fb9a2-122"><dt>"0x0000001"</dt></span><span class="sxs-lookup"><span data-stu-id="fb9a2-122"><dt>"0x0000001"</dt></span></span> </dl> | <span data-ttu-id="fb9a2-123">Il sistema operativo è Windows 7, Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fb9a2-123">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="fb9a2-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb9a2-124">Requirements</span></span>



| <span data-ttu-id="fb9a2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb9a2-125">Requirement</span></span> | <span data-ttu-id="fb9a2-126">Valore</span><span class="sxs-lookup"><span data-stu-id="fb9a2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9a2-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb9a2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fb9a2-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fb9a2-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb9a2-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb9a2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fb9a2-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fb9a2-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fb9a2-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fb9a2-131">End of client support</span></span><br/>    | <span data-ttu-id="fb9a2-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fb9a2-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fb9a2-133">Prodotto</span><span class="sxs-lookup"><span data-stu-id="fb9a2-133">Product</span></span><br/>                  | <span data-ttu-id="fb9a2-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fb9a2-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fb9a2-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb9a2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb9a2-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb9a2-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fb9a2-137">IID</span><span class="sxs-lookup"><span data-stu-id="fb9a2-137">IID</span></span><br/>                      | <span data-ttu-id="fb9a2-138">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="fb9a2-138">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fb9a2-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb9a2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb9a2-140">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="fb9a2-140">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

