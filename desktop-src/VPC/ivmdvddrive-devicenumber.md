---
title: Proprietà IVMDVDDrive DeviceNumber (VPCCOMInterfaces. h)
description: Recupera il numero di dispositivo a cui è collegata l'unità.
ms.assetid: 57b09400-e0c8-4ca2-bcd4-e6dd047daf95
keywords:
- Proprietà DeviceNumber Virtual PC
- Proprietà DeviceNumber Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, proprietà DeviceNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.DeviceNumber
- IVMDVDDrive.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de189b162ed2c880819f4c8729e996236ace250a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048501"
---
# <a name="ivmdvddrivedevicenumber-property"></a><span data-ttu-id="37f0b-106">IVMDVDDrive::D Proprietà eviceNumber</span><span class="sxs-lookup"><span data-stu-id="37f0b-106">IVMDVDDrive::DeviceNumber property</span></span>

<span data-ttu-id="37f0b-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="37f0b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="37f0b-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="37f0b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="37f0b-109">Recupera il numero di dispositivo a cui è collegata l'unità.</span><span class="sxs-lookup"><span data-stu-id="37f0b-109">Retrieves the device number to which this drive is attached.</span></span>

<span data-ttu-id="37f0b-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="37f0b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="37f0b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37f0b-111">Syntax</span></span>


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a><span data-ttu-id="37f0b-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="37f0b-112">Property value</span></span>

<span data-ttu-id="37f0b-113">Numero del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37f0b-113">The device number.</span></span> <span data-ttu-id="37f0b-114">Ad esempio, in un bus IDE, questo valore rappresenterebbe la posizione primaria o secondaria.</span><span class="sxs-lookup"><span data-stu-id="37f0b-114">For example, on an IDE bus, this value would represent either the primary or secondary location.</span></span>

## <a name="error-codes"></a><span data-ttu-id="37f0b-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="37f0b-115">Error codes</span></span>



| <span data-ttu-id="37f0b-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="37f0b-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="37f0b-117">Significato</span><span class="sxs-lookup"><span data-stu-id="37f0b-117">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="37f0b-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="37f0b-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="37f0b-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="37f0b-119">The operation was successful.</span></span><br/>                                          |
| <dl> <span data-ttu-id="37f0b-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="37f0b-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="37f0b-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="37f0b-121">The parameter is **NULL**.</span></span><br/>                                             |
| <dl> <span data-ttu-id="37f0b-122"><dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="37f0b-122"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="37f0b-123">Il percorso del bus per questa unità DVD non è stato inizializzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="37f0b-123">The bus location for this DVD drive has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="37f0b-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="37f0b-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="37f0b-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="37f0b-125">An unexpected error has occurred.</span></span><br/>                                      |



## <a name="requirements"></a><span data-ttu-id="37f0b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37f0b-126">Requirements</span></span>



| <span data-ttu-id="37f0b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="37f0b-127">Requirement</span></span> | <span data-ttu-id="37f0b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="37f0b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37f0b-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37f0b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="37f0b-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="37f0b-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37f0b-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37f0b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="37f0b-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="37f0b-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="37f0b-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="37f0b-133">End of client support</span></span><br/>    | <span data-ttu-id="37f0b-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="37f0b-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="37f0b-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="37f0b-135">Product</span></span><br/>                  | <span data-ttu-id="37f0b-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="37f0b-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="37f0b-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37f0b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="37f0b-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="37f0b-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="37f0b-139">IID</span><span class="sxs-lookup"><span data-stu-id="37f0b-139">IID</span></span><br/>                      | <span data-ttu-id="37f0b-140">IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="37f0b-140">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="37f0b-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37f0b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f0b-142">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="37f0b-142">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

