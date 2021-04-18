---
title: Proprietà IVMGuestOS IsHostTimeSyncEnabled (VPCCOMInterfaces. h)
description: Indica se i componenti di integrazione in questa macchina virtuale devono sincronizzare il clock del Guest con l'orologio dell'host.
ms.assetid: 57e3d49c-4acf-402f-9332-58ea443b363b
keywords:
- Proprietà IsHostTimeSyncEnabled Virtual PC
- Proprietà IsHostTimeSyncEnabled Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà IsHostTimeSyncEnabled
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHostTimeSyncEnabled
- IVMGuestOS.get_IsHostTimeSyncEnabled
- IVMGuestOS.put_IsHostTimeSyncEnabled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87afddb2e3bc940c5dba7e2548e4355d36142012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301734"
---
# <a name="ivmguestosishosttimesyncenabled-property"></a><span data-ttu-id="4e37e-106">Proprietà IVMGuestOS:: IsHostTimeSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="4e37e-106">IVMGuestOS::IsHostTimeSyncEnabled property</span></span>

<span data-ttu-id="4e37e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4e37e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4e37e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4e37e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4e37e-109">Indica se i componenti di integrazione in questa macchina virtuale (VM) devono sincronizzare il clock del Guest con il clock dell'host.</span><span class="sxs-lookup"><span data-stu-id="4e37e-109">Indicates whether the Integration Components in this virtual machine (VM) should synchronize the guest's clock with the host's clock.</span></span>

<span data-ttu-id="4e37e-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4e37e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e37e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e37e-111">Syntax</span></span>


```C++
HRESULT put_IsHostTimeSyncEnabled(
  [in]          VARIANT_BOOL shouldEnable
);

HRESULT get_IsHostTimeSyncEnabled(
  [out, retval] VARIANT_BOOL *isEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="4e37e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4e37e-112">Property value</span></span>

<span data-ttu-id="4e37e-113">Usare la **variante \_ true** se i componenti di integrazione in questa macchina virtuale devono sincronizzare il clock del Guest con l'orologio dell'host e la **variante \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4e37e-113">Use **VARIANT\_TRUE** if the integration components in this VM should synchronize the guest's clock with the host's clock and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4e37e-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4e37e-114">Error codes</span></span>



| <span data-ttu-id="4e37e-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="4e37e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4e37e-116">Significato</span><span class="sxs-lookup"><span data-stu-id="4e37e-116">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="4e37e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4e37e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4e37e-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4e37e-118">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="4e37e-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4e37e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4e37e-120">Il parametro *IsEnabled* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="4e37e-120">The *isEnabled* parameter is not specified.</span></span><br/> |
| <dl> <span data-ttu-id="4e37e-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4e37e-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="4e37e-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="4e37e-122">The configuration is unknown.</span></span><br/>               |
| <dl> <span data-ttu-id="4e37e-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4e37e-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4e37e-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="4e37e-124">An unexpected error has occurred.</span></span><br/>           |



## <a name="remarks"></a><span data-ttu-id="4e37e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e37e-125">Remarks</span></span>

<span data-ttu-id="4e37e-126">Non è possibile modificare questa impostazione mentre la macchina virtuale è attiva, ovvero è in esecuzione o in stato salvato.</span><span class="sxs-lookup"><span data-stu-id="4e37e-126">You cannot change this setting while the virtual machine is active (that is, running or in saved state).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e37e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e37e-127">Requirements</span></span>



| <span data-ttu-id="4e37e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e37e-128">Requirement</span></span> | <span data-ttu-id="4e37e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4e37e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e37e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e37e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4e37e-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4e37e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4e37e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e37e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4e37e-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4e37e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4e37e-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4e37e-134">End of client support</span></span><br/>    | <span data-ttu-id="4e37e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4e37e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4e37e-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4e37e-136">Product</span></span><br/>                  | <span data-ttu-id="4e37e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4e37e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4e37e-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e37e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e37e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e37e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4e37e-140">IID</span><span class="sxs-lookup"><span data-stu-id="4e37e-140">IID</span></span><br/>                      | <span data-ttu-id="4e37e-141">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="4e37e-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4e37e-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e37e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e37e-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="4e37e-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

