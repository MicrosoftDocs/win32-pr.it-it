---
title: Metodo _ID IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Recupera l'identificatore interno di questa interfaccia di rete.
ms.assetid: 3e71c2cd-1a75-44d9-9a6d-04e6344dfec3
keywords:
- Metodo di _ID Virtual PC
- Metodo _ID Virtual PC, interfaccia IVMNetworkAdapter
- Interfaccia IVMNetworkAdapter Virtual PC, metodo _ID
topic_type:
- apiref
api_name:
- IVMNetworkAdapter._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9df514d24f9826b58964b4c51c9a76a9ba982e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964345"
---
# <a name="ivmnetworkadapter_id-method"></a><span data-ttu-id="2da05-106">Metodo IVMNetworkAdapter:: \_ ID</span><span class="sxs-lookup"><span data-stu-id="2da05-106">IVMNetworkAdapter::\_ID method</span></span>

<span data-ttu-id="2da05-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2da05-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2da05-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2da05-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2da05-109">Recupera l'identificatore interno di questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="2da05-109">Retrieves the internal identifier of this network interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da05-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2da05-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *identifier
);
```



## <a name="parameters"></a><span data-ttu-id="2da05-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="2da05-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da05-112">*identificatore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="2da05-112">*identifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2da05-113">Identificatore interno.</span><span class="sxs-lookup"><span data-stu-id="2da05-113">The internal identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da05-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2da05-114">Return value</span></span>

<span data-ttu-id="2da05-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="2da05-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2da05-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="2da05-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="2da05-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2da05-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="2da05-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2da05-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2da05-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="2da05-119">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="2da05-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2da05-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2da05-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="2da05-121">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="2da05-122"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2da05-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="2da05-123">Impossibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2da05-123">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="2da05-124"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2da05-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2da05-125">Errore sconosciuto durante l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2da05-125">The operation had an unknown error.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="2da05-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="2da05-126">Remarks</span></span>

<span data-ttu-id="2da05-127">Questo metodo non è utilizzabile dai linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="2da05-127">This method is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da05-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2da05-128">Requirements</span></span>



| <span data-ttu-id="2da05-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2da05-129">Requirement</span></span> | <span data-ttu-id="2da05-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2da05-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da05-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2da05-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2da05-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2da05-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2da05-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2da05-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2da05-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2da05-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2da05-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2da05-135">End of client support</span></span><br/>    | <span data-ttu-id="2da05-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2da05-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2da05-137">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2da05-137">Product</span></span><br/>                  | <span data-ttu-id="2da05-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2da05-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2da05-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2da05-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2da05-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2da05-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2da05-141">IID</span><span class="sxs-lookup"><span data-stu-id="2da05-141">IID</span></span><br/>                      | <span data-ttu-id="2da05-142">IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="2da05-142">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2da05-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2da05-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da05-144">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="2da05-144">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

