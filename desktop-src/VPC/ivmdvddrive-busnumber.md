---
title: Proprietà IVMDVDDrive BusNumber (VPCCOMInterfaces. h)
description: Recupera il numero di bus a cui è collegato il dispositivo.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- Proprietà BusNumber Virtual PC
- Proprietà BusNumber Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, proprietà BusNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056770b7eb11518645f3c28a6d45685795c7107a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302100"
---
# <a name="ivmdvddrivebusnumber-property"></a><span data-ttu-id="c6f89-106">Proprietà IVMDVDDrive:: BusNumber</span><span class="sxs-lookup"><span data-stu-id="c6f89-106">IVMDVDDrive::BusNumber property</span></span>

<span data-ttu-id="c6f89-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c6f89-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c6f89-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c6f89-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c6f89-109">Recupera il numero di bus a cui è collegato il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6f89-109">Retrieves the bus number to which this device is attached.</span></span>

<span data-ttu-id="c6f89-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c6f89-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f89-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6f89-111">Syntax</span></span>


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a><span data-ttu-id="c6f89-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c6f89-112">Property value</span></span>

<span data-ttu-id="c6f89-113">Numero del bus.</span><span class="sxs-lookup"><span data-stu-id="c6f89-113">The bus number.</span></span> <span data-ttu-id="c6f89-114">Ad esempio, in un bus IDE, questo valore rappresenterebbe la posizione primaria o secondaria.</span><span class="sxs-lookup"><span data-stu-id="c6f89-114">For example, on an IDE bus, this value would represent either the primary or secondary location.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c6f89-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c6f89-115">Error codes</span></span>



| <span data-ttu-id="c6f89-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="c6f89-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="c6f89-117">Significato</span><span class="sxs-lookup"><span data-stu-id="c6f89-117">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6f89-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c6f89-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="c6f89-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c6f89-119">The operation was successful.</span></span><br/>                                          |
| <dl> <span data-ttu-id="c6f89-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c6f89-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="c6f89-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="c6f89-121">The parameter is **NULL**.</span></span><br/>                                             |
| <dl> <span data-ttu-id="c6f89-122"><dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c6f89-122"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="c6f89-123">Il percorso del bus per questa unità DVD non è stato inizializzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="c6f89-123">The bus location for this DVD drive has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="c6f89-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c6f89-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="c6f89-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c6f89-125">An unexpected error has occurred.</span></span><br/>                                      |



## <a name="requirements"></a><span data-ttu-id="c6f89-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6f89-126">Requirements</span></span>



| <span data-ttu-id="c6f89-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6f89-127">Requirement</span></span> | <span data-ttu-id="c6f89-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c6f89-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f89-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6f89-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c6f89-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c6f89-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6f89-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6f89-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c6f89-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c6f89-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c6f89-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c6f89-133">End of client support</span></span><br/>    | <span data-ttu-id="c6f89-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c6f89-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c6f89-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c6f89-135">Product</span></span><br/>                  | <span data-ttu-id="c6f89-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c6f89-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c6f89-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6f89-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6f89-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6f89-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c6f89-139">IID</span><span class="sxs-lookup"><span data-stu-id="c6f89-139">IID</span></span><br/>                      | <span data-ttu-id="c6f89-140">IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="c6f89-140">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="c6f89-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6f89-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f89-142">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="c6f89-142">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

