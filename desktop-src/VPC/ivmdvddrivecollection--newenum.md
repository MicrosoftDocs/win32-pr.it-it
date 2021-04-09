---
title: Proprietà _NewEnum IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera un enumeratore per la raccolta CD/DVD.
ms.assetid: e911628b-2a92-41e5-9271-556a297d747d
keywords:
- Proprietà _NewEnum Virtual PC
- Proprietà _NewEnum Virtual PC, interfaccia IVMDVDDriveCollection
- Interfaccia IVMDVDDriveCollection Virtual PC, _NewEnum proprietà
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection._NewEnum
- IVMDVDDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfd0de3aaf6b25808d1afa591b0c2099599e6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964172"
---
# <a name="ivmdvddrivecollection_newenum-property"></a><span data-ttu-id="5e8eb-106">Proprietà IVMDVDDriveCollection:: \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="5e8eb-106">IVMDVDDriveCollection::\_NewEnum property</span></span>

<span data-ttu-id="5e8eb-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5e8eb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5e8eb-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5e8eb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5e8eb-109">Recupera un enumeratore per la raccolta CD/DVD.</span><span class="sxs-lookup"><span data-stu-id="5e8eb-109">Retrieves an enumerator for the CD/DVD collection.</span></span>

<span data-ttu-id="5e8eb-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5e8eb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e8eb-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e8eb-111">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="5e8eb-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5e8eb-112">Property value</span></span>

<span data-ttu-id="5e8eb-113">Enumeratore [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="5e8eb-113">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5e8eb-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5e8eb-114">Error codes</span></span>



| <span data-ttu-id="5e8eb-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="5e8eb-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="5e8eb-116">Significato</span><span class="sxs-lookup"><span data-stu-id="5e8eb-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="5e8eb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5e8eb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5e8eb-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="5e8eb-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="5e8eb-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="5e8eb-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="5e8eb-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="5e8eb-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="5e8eb-121"><dt>E \_ ERRORE</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="5e8eb-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="5e8eb-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="5e8eb-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="5e8eb-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5e8eb-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="5e8eb-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="5e8eb-124">An unexpected error occurred.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="5e8eb-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e8eb-125">Requirements</span></span>



| <span data-ttu-id="5e8eb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e8eb-126">Requirement</span></span> | <span data-ttu-id="5e8eb-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5e8eb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8eb-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e8eb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5e8eb-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5e8eb-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e8eb-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e8eb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5e8eb-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5e8eb-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5e8eb-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5e8eb-132">End of client support</span></span><br/>    | <span data-ttu-id="5e8eb-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5e8eb-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5e8eb-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="5e8eb-134">Product</span></span><br/>                  | <span data-ttu-id="5e8eb-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5e8eb-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5e8eb-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e8eb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e8eb-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e8eb-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5e8eb-138">IID</span><span class="sxs-lookup"><span data-stu-id="5e8eb-138">IID</span></span><br/>                      | <span data-ttu-id="5e8eb-139">IID \_ IVMDVDDriveCollection è definito come bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="5e8eb-139">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="5e8eb-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e8eb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e8eb-141">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="5e8eb-141">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

