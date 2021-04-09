---
title: Proprietà Item di IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Oggetto floppy che corrisponde all'indice specificato.
ms.assetid: 068a1f1c-ae84-4689-b68a-ce25b68fc06b
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMFloppyDriveCollection
- Interfaccia IVMFloppyDriveCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Item
- IVMFloppyDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315eaea13699d78a75457f39c6c915b30fa2fa9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121359"
---
# <a name="ivmfloppydrivecollectionitem-property"></a><span data-ttu-id="36134-106">Proprietà IVMFloppyDriveCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="36134-106">IVMFloppyDriveCollection::Item property</span></span>

<span data-ttu-id="36134-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="36134-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="36134-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="36134-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="36134-109">Recupera l'oggetto floppy che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="36134-109">Retrieves the floppy object that corresponds to the specified index.</span></span>

<span data-ttu-id="36134-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="36134-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="36134-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36134-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long           index,
  [out, retval] IVMFloppyDrive **floppyDrive
);
```



## <a name="property-value"></a><span data-ttu-id="36134-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="36134-112">Property value</span></span>

<span data-ttu-id="36134-113">Oggetto [**IVMFloppyDrive**](ivmfloppydrive.md) .</span><span class="sxs-lookup"><span data-stu-id="36134-113">The [**IVMFloppyDrive**](ivmfloppydrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="36134-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="36134-114">Error codes</span></span>



| <span data-ttu-id="36134-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="36134-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="36134-116">Significato</span><span class="sxs-lookup"><span data-stu-id="36134-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36134-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="36134-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="36134-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="36134-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="36134-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="36134-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="36134-120">Il parametro *floppyDrive* è **null**.</span><span class="sxs-lookup"><span data-stu-id="36134-120">The *floppyDrive* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="36134-121"><dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="36134-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="36134-122">L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="36134-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="36134-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="36134-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="36134-124">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="36134-124">The configuration is unknown.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="36134-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="36134-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="36134-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="36134-126">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="36134-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36134-127">Requirements</span></span>



| <span data-ttu-id="36134-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="36134-128">Requirement</span></span> | <span data-ttu-id="36134-129">Valore</span><span class="sxs-lookup"><span data-stu-id="36134-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="36134-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36134-130">Minimum supported client</span></span><br/> | <span data-ttu-id="36134-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="36134-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36134-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36134-132">Minimum supported server</span></span><br/> | <span data-ttu-id="36134-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="36134-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="36134-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="36134-134">End of client support</span></span><br/>    | <span data-ttu-id="36134-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="36134-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="36134-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="36134-136">Product</span></span><br/>                  | <span data-ttu-id="36134-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="36134-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="36134-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36134-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="36134-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="36134-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="36134-140">IID</span><span class="sxs-lookup"><span data-stu-id="36134-140">IID</span></span><br/>                      | <span data-ttu-id="36134-141">IID \_ IVMFloppyDriveCollection è definito come 8ba70a25-f698-4ee5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="36134-141">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="36134-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36134-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36134-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="36134-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="36134-144">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="36134-144">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

