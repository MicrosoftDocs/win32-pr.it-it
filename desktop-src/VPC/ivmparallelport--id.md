---
title: Metodo _ID IVMParallelPort (VPCCOMInterfaces. h)
description: Recupera l'identificatore interno della porta parallela.
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- Metodo di _ID Virtual PC
- Metodo _ID Virtual PC, interfaccia IVMParallelPort
- Interfaccia IVMParallelPort Virtual PC, metodo _ID
topic_type:
- apiref
api_name:
- IVMParallelPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267061204ea92dd8f5cae37fc5cb279e7dc2b010
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300926"
---
# <a name="ivmparallelport_id-method"></a><span data-ttu-id="d3c94-106">Metodo IVMParallelPort:: \_ ID</span><span class="sxs-lookup"><span data-stu-id="d3c94-106">IVMParallelPort::\_ID method</span></span>

<span data-ttu-id="d3c94-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d3c94-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d3c94-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d3c94-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d3c94-109">Recupera l'identificatore interno della porta parallela.</span><span class="sxs-lookup"><span data-stu-id="d3c94-109">Retrieves the internal identifier of the parallel port.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c94-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3c94-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a><span data-ttu-id="d3c94-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3c94-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c94-112">*ID porta* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d3c94-112">*portID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c94-113">Identificatore della porta parallela.</span><span class="sxs-lookup"><span data-stu-id="d3c94-113">The parallel port identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c94-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3c94-114">Return value</span></span>

<span data-ttu-id="d3c94-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d3c94-115">This method can return one of these values.</span></span>



| <span data-ttu-id="d3c94-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3c94-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="d3c94-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3c94-117">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3c94-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d3c94-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d3c94-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d3c94-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="d3c94-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d3c94-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d3c94-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="d3c94-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="d3c94-122"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d3c94-122"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d3c94-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d3c94-123">An unexpected error has occurred.</span></span><br/>                        |
| <dl> <span data-ttu-id="d3c94-124"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d3c94-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d3c94-125">La configurazione per questa macchina virtuale non è valida.</span><span class="sxs-lookup"><span data-stu-id="d3c94-125">The configuration for this virtual machine is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3c94-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3c94-126">Remarks</span></span>

<span data-ttu-id="d3c94-127">Questa proprietà non è utilizzabile dai linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="d3c94-127">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c94-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3c94-128">Requirements</span></span>



| <span data-ttu-id="d3c94-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c94-129">Requirement</span></span> | <span data-ttu-id="d3c94-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d3c94-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c94-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3c94-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c94-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d3c94-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3c94-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3c94-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c94-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d3c94-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d3c94-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d3c94-135">End of client support</span></span><br/>    | <span data-ttu-id="d3c94-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3c94-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d3c94-137">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d3c94-137">Product</span></span><br/>                  | <span data-ttu-id="d3c94-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d3c94-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d3c94-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3c94-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3c94-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3c94-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d3c94-141">IID</span><span class="sxs-lookup"><span data-stu-id="d3c94-141">IID</span></span><br/>                      | <span data-ttu-id="d3c94-142">IID \_ IVMParallelPort è definito come 097beecb-0A02-474F-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="d3c94-142">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d3c94-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3c94-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c94-144">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="d3c94-144">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> </dl>

 

