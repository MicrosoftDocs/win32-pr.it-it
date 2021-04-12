---
title: Metodo IVMHardDiskConnection SetBusLocation (VPCCOMInterfaces. h)
description: Imposta la posizione del bus a cui è collegato il disco rigido.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- Metodo SetBusLocation Virtual PC
- Metodo SetBusLocation Virtual PC, interfaccia IVMHardDiskConnection
- Interfaccia IVMHardDiskConnection Virtual PC, metodo SetBusLocation
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61de0f595bc06d497e7f5913da9173ccb3bf1ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340333"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a><span data-ttu-id="c9fd7-106">Metodo IVMHardDiskConnection:: SetBusLocation</span><span class="sxs-lookup"><span data-stu-id="c9fd7-106">IVMHardDiskConnection::SetBusLocation method</span></span>

<span data-ttu-id="c9fd7-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c9fd7-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c9fd7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c9fd7-109">Imposta la posizione del bus a cui è collegato il disco rigido.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-109">Sets the bus location to which this hard disk is attached.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9fd7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9fd7-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="c9fd7-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9fd7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9fd7-112">*vmBusNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9fd7-112">*vmBusNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9fd7-113">Numero del bus da usare.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-113">The bus number to be used.</span></span>

</dd> <dt>

<span data-ttu-id="c9fd7-114">*vmDeviceNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9fd7-114">*vmDeviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9fd7-115">Numero di dispositivo da usare.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-115">The device number to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9fd7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9fd7-116">Return value</span></span>

<span data-ttu-id="c9fd7-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-117">This method can return one of these values.</span></span>



| <span data-ttu-id="c9fd7-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9fd7-118">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="c9fd7-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9fd7-119">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9fd7-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c9fd7-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="c9fd7-121">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-121">The operation was successful.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="c9fd7-122"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c9fd7-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="c9fd7-123">Il percorso del bus specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-123">The bus location specified is not valid.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="c9fd7-124"><dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="c9fd7-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="c9fd7-125">Non è stato possibile impostare il percorso del bus perché lo stato della macchina virtuale è in esecuzione o salvato.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-125">The bus location could not be set because the virtual machine is in a running or saved state.</span></span><br/>    |
| <dl> <span data-ttu-id="c9fd7-126"><dt>**Macchina virtuale \_ E \_ la \_ \_ loc \_ del bus di unità in \_ use**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="c9fd7-126"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="c9fd7-127">Non è stato possibile impostare il percorso del bus perché un altro dispositivo è attualmente collegato a questo percorso.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-127">The bus location could not be set because another device is currently attached to this location.</span></span><br/> |
| <dl> <span data-ttu-id="c9fd7-128"><dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c9fd7-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="c9fd7-129">L'unità corrente non è valida.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-129">The current drive is not valid.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="c9fd7-130"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c9fd7-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="c9fd7-131">La macchina virtuale corrente non è valida.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-131">The current virtual machine is not valid.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="c9fd7-132"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c9fd7-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="c9fd7-133">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-133">An unexpected error has occurred.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="c9fd7-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9fd7-134">Requirements</span></span>



| <span data-ttu-id="c9fd7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9fd7-135">Requirement</span></span> | <span data-ttu-id="c9fd7-136">Valore</span><span class="sxs-lookup"><span data-stu-id="c9fd7-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9fd7-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9fd7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c9fd7-138">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c9fd7-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9fd7-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9fd7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c9fd7-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c9fd7-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c9fd7-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c9fd7-141">End of client support</span></span><br/>    | <span data-ttu-id="c9fd7-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9fd7-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c9fd7-143">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c9fd7-143">Product</span></span><br/>                  | <span data-ttu-id="c9fd7-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c9fd7-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c9fd7-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9fd7-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9fd7-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9fd7-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c9fd7-147">IID</span><span class="sxs-lookup"><span data-stu-id="c9fd7-147">IID</span></span><br/>                      | <span data-ttu-id="c9fd7-148">IID \_ IVMHardDiskconnection è definito come aefa36a5-463A-46AE-9E6C-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="c9fd7-148">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="c9fd7-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9fd7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9fd7-150">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="c9fd7-150">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

