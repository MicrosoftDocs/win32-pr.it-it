---
title: Proprietà Item di IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera l'oggetto unità CD o DVD corrispondente all'indice specificato.
ms.assetid: ecc94eea-9ddc-46c8-87e2-e67aca83eecc
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMDVDDriveCollection
- Interfaccia IVMDVDDriveCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Item
- IVMDVDDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cc631ab6d4de3ab65071bf2b8692236f3ae03ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048324"
---
# <a name="ivmdvddrivecollectionitem-property"></a><span data-ttu-id="f3c4f-106">Proprietà IVMDVDDriveCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="f3c4f-106">IVMDVDDriveCollection::Item property</span></span>

<span data-ttu-id="f3c4f-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f3c4f-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f3c4f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f3c4f-109">Recupera l'oggetto unità CD o DVD corrispondente all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-109">Retrieves the CD or DVD drive object that corresponds to the specified index.</span></span>

<span data-ttu-id="f3c4f-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3c4f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3c4f-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long        index,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="property-value"></a><span data-ttu-id="f3c4f-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f3c4f-112">Property value</span></span>

<span data-ttu-id="f3c4f-113">Oggetto [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c4f-113">The [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f3c4f-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f3c4f-114">Error codes</span></span>



| <span data-ttu-id="f3c4f-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="f3c4f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f3c4f-116">Significato</span><span class="sxs-lookup"><span data-stu-id="f3c4f-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3c4f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f3c4f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f3c4f-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="f3c4f-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f3c4f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f3c4f-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-120">The parameter is **NULL**.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="f3c4f-121"><dt>E \_ ERRORE</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="f3c4f-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="f3c4f-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-122">An unexpected error has occurred.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="f3c4f-123"><dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="f3c4f-123"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="f3c4f-124">L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-124">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="f3c4f-125"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f3c4f-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f3c4f-126">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-126">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="f3c4f-127"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f3c4f-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f3c4f-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-128">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="f3c4f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3c4f-129">Requirements</span></span>



| <span data-ttu-id="f3c4f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3c4f-130">Requirement</span></span> | <span data-ttu-id="f3c4f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f3c4f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c4f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3c4f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c4f-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f3c4f-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3c4f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3c4f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c4f-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f3c4f-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f3c4f-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f3c4f-136">End of client support</span></span><br/>    | <span data-ttu-id="f3c4f-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3c4f-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f3c4f-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f3c4f-138">Product</span></span><br/>                  | <span data-ttu-id="f3c4f-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f3c4f-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f3c4f-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3c4f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3c4f-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3c4f-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f3c4f-142">IID</span><span class="sxs-lookup"><span data-stu-id="f3c4f-142">IID</span></span><br/>                      | <span data-ttu-id="f3c4f-143">IID \_ IVMDVDDriveCollection è definito come bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="f3c4f-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="f3c4f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3c4f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c4f-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="f3c4f-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="f3c4f-146">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="f3c4f-146">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

