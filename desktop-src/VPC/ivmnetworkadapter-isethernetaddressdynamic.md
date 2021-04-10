---
title: Proprietà IVMNetworkAdapter IsEthernetAddressDynamic (VPCCOMInterfaces. h)
description: Determina se l'indirizzo Ethernet viene generato dinamicamente.
ms.assetid: 7bd87868-f1d1-48e5-9e1b-04d2126f9dad
keywords:
- Proprietà IsEthernetAddressDynamic Virtual PC
- Proprietà IsEthernetAddressDynamic Virtual PC, interfaccia IVMNetworkAdapter
- Interfaccia IVMNetworkAdapter Virtual PC, proprietà IsEthernetAddressDynamic
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.IsEthernetAddressDynamic
- IVMNetworkAdapter.get_IsEthernetAddressDynamic
- IVMNetworkAdapter.put_IsEthernetAddressDynamic
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b16074243094d410e8d39538b024120daa1871e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047804"
---
# <a name="ivmnetworkadapterisethernetaddressdynamic-property"></a><span data-ttu-id="d642f-106">Proprietà IVMNetworkAdapter:: IsEthernetAddressDynamic</span><span class="sxs-lookup"><span data-stu-id="d642f-106">IVMNetworkAdapter::IsEthernetAddressDynamic property</span></span>

<span data-ttu-id="d642f-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d642f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d642f-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d642f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d642f-109">Determina se l'indirizzo Ethernet viene generato dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="d642f-109">Determines whether the Ethernet address is dynamically generated.</span></span>

<span data-ttu-id="d642f-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d642f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d642f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d642f-111">Syntax</span></span>


```C++
HRESULT put_IsEthernetAddressDynamic(
  [in]          VARIANT_BOOL isDynamic
);

HRESULT get_IsEthernetAddressDynamic(
  [out, retval] VARIANT_BOOL *isDynamic
);
```



## <a name="property-value"></a><span data-ttu-id="d642f-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d642f-112">Property value</span></span>

<span data-ttu-id="d642f-113">Impostare su VARIANT \_ true se l'indirizzo Ethernet deve essere generato in modo dinamico e Variant \_ false se l'indirizzo Ethernet è statico.</span><span class="sxs-lookup"><span data-stu-id="d642f-113">Set to VARIANT\_TRUE if the Ethernet address should be dynamically generated and VARIANT\_FALSE if the Ethernet address is static.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d642f-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d642f-114">Error codes</span></span>



| <span data-ttu-id="d642f-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="d642f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d642f-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d642f-116">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d642f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d642f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d642f-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d642f-118">The operation was successful.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="d642f-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d642f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d642f-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="d642f-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="d642f-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d642f-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d642f-122">La macchina virtuale non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="d642f-122">The virtual machine was not found.</span></span> <span data-ttu-id="d642f-123">Questo problema può verificarsi se il computer è stato rimosso dopo la creazione dell'oggetto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="d642f-123">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/> |
| <dl> <span data-ttu-id="d642f-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d642f-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d642f-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d642f-125">An unexpected error has occurred.</span></span><br/>                                                                                                                         |



## <a name="remarks"></a><span data-ttu-id="d642f-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="d642f-126">Remarks</span></span>

<span data-ttu-id="d642f-127">Questa proprietà deve essere impostata su **true** (impostazione predefinita) per la maggior parte delle interfacce di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d642f-127">This property should be set to **TRUE** (default) for most virtual network interfaces.</span></span> <span data-ttu-id="d642f-128">Se il software nel guest richiede un indirizzo Ethernet statico, questa proprietà deve essere impostata su **false**.</span><span class="sxs-lookup"><span data-stu-id="d642f-128">If software in the guest requires a static Ethernet address, this property should be set to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d642f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d642f-129">Requirements</span></span>



| <span data-ttu-id="d642f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d642f-130">Requirement</span></span> | <span data-ttu-id="d642f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="d642f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d642f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d642f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d642f-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d642f-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d642f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d642f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d642f-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d642f-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d642f-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d642f-136">End of client support</span></span><br/>    | <span data-ttu-id="d642f-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d642f-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d642f-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d642f-138">Product</span></span><br/>                  | <span data-ttu-id="d642f-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d642f-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d642f-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d642f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d642f-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d642f-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d642f-142">IID</span><span class="sxs-lookup"><span data-stu-id="d642f-142">IID</span></span><br/>                      | <span data-ttu-id="d642f-143">IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="d642f-143">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d642f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d642f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d642f-145">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="d642f-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

