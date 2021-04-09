---
title: Proprietà IVMVirtualMachine AttachedDriveTypes (VPCCOMInterfaces. h)
description: Matrice che indica il tipo di unità collegata a ogni posizione della macchina virtuale.
ms.assetid: 6896c9cd-5448-4fbb-8c8e-eef306a5cea1
keywords:
- Proprietà AttachedDriveTypes Virtual PC
- Proprietà AttachedDriveTypes Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà AttachedDriveTypes
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachedDriveTypes
- IVMVirtualMachine.get_AttachedDriveTypes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5f01802b7fa7e3a4f1ccbfc1b5c4bf70e06614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121087"
---
# <a name="ivmvirtualmachineattacheddrivetypes-property"></a><span data-ttu-id="ba89b-106">Proprietà IVMVirtualMachine:: AttachedDriveTypes</span><span class="sxs-lookup"><span data-stu-id="ba89b-106">IVMVirtualMachine::AttachedDriveTypes property</span></span>

<span data-ttu-id="ba89b-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ba89b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ba89b-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ba89b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ba89b-109">Recupera una matrice che indica il tipo di unità collegata a ogni posizione della macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="ba89b-109">Retrieves an array indicating the type of drive attached to each location in the virtual machine (VM).</span></span>

<span data-ttu-id="ba89b-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ba89b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba89b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba89b-111">Syntax</span></span>


```C++
HRESULT get_AttachedDriveTypes(
  [out, retval] VARIANT *driveTypes
);
```



## <a name="property-value"></a><span data-ttu-id="ba89b-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ba89b-112">Property value</span></span>

<span data-ttu-id="ba89b-113">Variante di tipo VT **\_ Array** VT \| **\_ Variant** contenente voci di tipo **VT \_ Ui1**.</span><span class="sxs-lookup"><span data-stu-id="ba89b-113">A variant of type **VT\_ARRAY** \| **VT\_VARIANT** containing entries of type **VT\_UI1**.</span></span> <span data-ttu-id="ba89b-114">La matrice contiene il valore [**VMDriveType**](vmdrivetype.md) di ogni dispositivo connesso a ogni percorso del bus.</span><span class="sxs-lookup"><span data-stu-id="ba89b-114">The array contains the [**VMDriveType**](vmdrivetype.md) value of each device connected to every bus location.</span></span> <span data-ttu-id="ba89b-115">La matrice viene ordinata in base a \[ *busNumber* \] \[ *DeviceID* \] .</span><span class="sxs-lookup"><span data-stu-id="ba89b-115">The array is ordered by \[*busNumber*\]\[*deviceID*\].</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba89b-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ba89b-116">Error codes</span></span>



| <span data-ttu-id="ba89b-117">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="ba89b-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="ba89b-118">Significato</span><span class="sxs-lookup"><span data-stu-id="ba89b-118">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ba89b-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ba89b-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ba89b-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ba89b-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="ba89b-121"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ba89b-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ba89b-122">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="ba89b-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="ba89b-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ba89b-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="ba89b-124">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="ba89b-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="ba89b-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ba89b-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ba89b-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="ba89b-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ba89b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba89b-127">Requirements</span></span>



| <span data-ttu-id="ba89b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba89b-128">Requirement</span></span> | <span data-ttu-id="ba89b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ba89b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba89b-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba89b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ba89b-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ba89b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba89b-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba89b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ba89b-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ba89b-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ba89b-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ba89b-134">End of client support</span></span><br/>    | <span data-ttu-id="ba89b-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ba89b-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ba89b-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ba89b-136">Product</span></span><br/>                  | <span data-ttu-id="ba89b-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ba89b-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ba89b-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba89b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba89b-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba89b-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ba89b-140">IID</span><span class="sxs-lookup"><span data-stu-id="ba89b-140">IID</span></span><br/>                      | <span data-ttu-id="ba89b-141">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="ba89b-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ba89b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba89b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba89b-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="ba89b-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

