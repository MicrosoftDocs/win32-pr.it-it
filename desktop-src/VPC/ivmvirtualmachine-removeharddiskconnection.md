---
title: Metodo IVMVirtualMachine RemoveHardDiskConnection (VPCCOMInterfaces. h)
description: Rimuove la connessione al disco rigido specificata dalla macchina virtuale.
ms.assetid: d31f2442-aae4-4987-9188-fd32778604a1
keywords:
- Metodo RemoveHardDiskConnection Virtual PC
- Metodo RemoveHardDiskConnection Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo RemoveHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62a9bbf8b3aac0dd35c8390343c20a1b67b59101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400666"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a><span data-ttu-id="8fc45-106">Metodo IVMVirtualMachine:: RemoveHardDiskConnection</span><span class="sxs-lookup"><span data-stu-id="8fc45-106">IVMVirtualMachine::RemoveHardDiskConnection method</span></span>

<span data-ttu-id="8fc45-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8fc45-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8fc45-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8fc45-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8fc45-109">Rimuove la connessione al disco rigido specificata dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8fc45-109">Removes the specified hard disk connection from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc45-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fc45-110">Syntax</span></span>


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="8fc45-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fc45-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc45-112">*hardDiskConnection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fc45-112">*hardDiskConnection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc45-113">Oggetto [**IVMHardDiskConnection**](ivmharddiskconnection.md) che rappresenta la connessione al disco rigido da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8fc45-113">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object that represents the hard disk connection to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc45-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fc45-114">Return value</span></span>

<span data-ttu-id="8fc45-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="8fc45-115">This method can return one of these values.</span></span>



| <span data-ttu-id="8fc45-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fc45-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="8fc45-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fc45-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="8fc45-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8fc45-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="8fc45-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8fc45-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="8fc45-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8fc45-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="8fc45-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="8fc45-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="8fc45-122"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8fc45-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="8fc45-123">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="8fc45-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="8fc45-124"><dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="8fc45-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="8fc45-125">Lo stato della macchina virtuale è in esecuzione o salvato.</span><span class="sxs-lookup"><span data-stu-id="8fc45-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="8fc45-126"><dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8fc45-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="8fc45-127">L'unità specificata non è connessa a questo percorso del bus.</span><span class="sxs-lookup"><span data-stu-id="8fc45-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="8fc45-128"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8fc45-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="8fc45-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="8fc45-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="8fc45-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fc45-130">Remarks</span></span>

<span data-ttu-id="8fc45-131">È possibile rimuovere una connessione a un disco rigido esistente solo da una macchina virtuale arrestata.</span><span class="sxs-lookup"><span data-stu-id="8fc45-131">You can only remove an existing hard disk connection from a stopped virtual machine.</span></span> <span data-ttu-id="8fc45-132">Un elenco di connessioni attualmente collegate alla macchina virtuale viene ottenuto enumerando la proprietà [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="8fc45-132">A list of connections currently attached to the virtual machine is obtained by enumerating the [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc45-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fc45-133">Requirements</span></span>



| <span data-ttu-id="8fc45-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fc45-134">Requirement</span></span> | <span data-ttu-id="8fc45-135">Valore</span><span class="sxs-lookup"><span data-stu-id="8fc45-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc45-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fc45-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc45-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8fc45-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8fc45-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fc45-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc45-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8fc45-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8fc45-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8fc45-140">End of client support</span></span><br/>    | <span data-ttu-id="8fc45-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8fc45-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8fc45-142">Prodotto</span><span class="sxs-lookup"><span data-stu-id="8fc45-142">Product</span></span><br/>                  | <span data-ttu-id="8fc45-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8fc45-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8fc45-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fc45-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fc45-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc45-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8fc45-146">IID</span><span class="sxs-lookup"><span data-stu-id="8fc45-146">IID</span></span><br/>                      | <span data-ttu-id="8fc45-147">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="8fc45-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="8fc45-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fc45-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc45-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="8fc45-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

