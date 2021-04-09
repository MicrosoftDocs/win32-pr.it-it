---
title: Metodo _ID IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Recupera l'identificatore interno della rete virtuale.
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- Metodo di _ID Virtual PC
- Metodo _ID Virtual PC, interfaccia IVMVirtualNetwork
- Interfaccia IVMVirtualNetwork Virtual PC, metodo _ID
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b79c4d6f4dfa778fee156b1bfa09ab39b8bedf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048663"
---
# <a name="ivmvirtualnetwork_id-method"></a><span data-ttu-id="7f46c-106">Metodo IVMVirtualNetwork:: \_ ID</span><span class="sxs-lookup"><span data-stu-id="7f46c-106">IVMVirtualNetwork::\_ID method</span></span>

<span data-ttu-id="7f46c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7f46c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7f46c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7f46c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7f46c-109">Recupera l'identificatore interno della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f46c-109">Retrieves the internal identifier of the virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f46c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f46c-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a><span data-ttu-id="7f46c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f46c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f46c-112">*virtualNetworkID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7f46c-112">*virtualNetworkID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f46c-113">Identificatore della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f46c-113">The virtual network identifier.</span></span> <span data-ttu-id="7f46c-114">L'identificatore per la rete virtuale NAT (Shared Networking) è 01010101010101010101010101010101.</span><span class="sxs-lookup"><span data-stu-id="7f46c-114">The identifier for the Shared Networking (NAT) virtual network is 01010101010101010101010101010101.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f46c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f46c-115">Return value</span></span>

<span data-ttu-id="7f46c-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7f46c-116">This method can return one of these values.</span></span>



| <span data-ttu-id="7f46c-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f46c-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="7f46c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f46c-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7f46c-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7f46c-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7f46c-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7f46c-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="7f46c-121"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7f46c-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7f46c-122">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="7f46c-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="7f46c-123"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7f46c-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7f46c-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="7f46c-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f46c-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f46c-125">Remarks</span></span>

<span data-ttu-id="7f46c-126">Questa proprietà non è utilizzabile dai linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="7f46c-126">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f46c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f46c-127">Requirements</span></span>



| <span data-ttu-id="7f46c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f46c-128">Requirement</span></span> | <span data-ttu-id="7f46c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7f46c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f46c-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f46c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7f46c-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7f46c-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f46c-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f46c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7f46c-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7f46c-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7f46c-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7f46c-134">End of client support</span></span><br/>    | <span data-ttu-id="7f46c-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f46c-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7f46c-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="7f46c-136">Product</span></span><br/>                  | <span data-ttu-id="7f46c-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7f46c-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7f46c-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f46c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f46c-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f46c-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7f46c-140">IID</span><span class="sxs-lookup"><span data-stu-id="7f46c-140">IID</span></span><br/>                      | <span data-ttu-id="7f46c-141">IID \_ IVMVirtualNetwork è definito come 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="7f46c-141">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7f46c-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f46c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f46c-143">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="7f46c-143">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

