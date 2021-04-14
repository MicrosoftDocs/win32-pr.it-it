---
title: Metodo IVMVirtualPC FindVirtualNetwork (VPCCOMInterfaces. h)
description: Recupera un oggetto rete virtuale che corrisponde al nome richiesto.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- Metodo FindVirtualNetwork Virtual PC
- Metodo FindVirtualNetwork Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo FindVirtualNetwork
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59306d2e2022c1323ab52f1a47bd386347f504e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518471"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a><span data-ttu-id="64988-106">Metodo IVMVirtualPC:: FindVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="64988-106">IVMVirtualPC::FindVirtualNetwork method</span></span>

<span data-ttu-id="64988-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="64988-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="64988-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="64988-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="64988-109">Recupera un oggetto rete virtuale che corrisponde al nome richiesto.</span><span class="sxs-lookup"><span data-stu-id="64988-109">Retrieves a virtual network object that matches the requested name.</span></span>

## <a name="syntax"></a><span data-ttu-id="64988-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64988-110">Syntax</span></span>


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="64988-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="64988-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64988-112">*virtualNetworkName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64988-112">*virtualNetworkName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64988-113">Nome della rete virtuale da trovare.</span><span class="sxs-lookup"><span data-stu-id="64988-113">The name of the virtual network to find.</span></span>

</dd> <dt>

<span data-ttu-id="64988-114">*virtualNetwork* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="64988-114">*virtualNetwork* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="64988-115">Puntatore a un nuovo oggetto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) che rappresenta la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="64988-115">A pointer to a new [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that represents this virtual network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64988-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64988-116">Return value</span></span>

<span data-ttu-id="64988-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="64988-117">This method can return one of these values.</span></span>



| <span data-ttu-id="64988-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="64988-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="64988-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64988-119">Description</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="64988-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="64988-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="64988-121">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="64988-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="64988-122"><dt>**S \_ FALSE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="64988-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="64988-123">La rete virtuale specificata non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="64988-123">The specified virtual network could not be found.</span></span><br/>                                    |
| <dl> <span data-ttu-id="64988-124"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="64988-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="64988-125">Il parametro *virtualNetwork* è **null** o non è possibile trovare la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="64988-125">The *virtualNetwork* parameter is **NULL** or the virtual network cannot be found.</span></span><br/>   |
| <dl> <span data-ttu-id="64988-126"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="64988-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="64988-127">Il parametro *virtualNetworkName* non è valido o è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="64988-127">The *virtualNetworkName* parameter is not valid or is an empty string.</span></span><br/>               |
| <dl> <span data-ttu-id="64988-128"><dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="64988-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="64988-129">Impossibile trovare il file della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="64988-129">The virtual network file could not be found.</span></span><br/>                                         |
| <dl> <span data-ttu-id="64988-130"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="64988-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="64988-131">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="64988-131">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="64988-132"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="64988-132"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="64988-133">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="64988-133">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="64988-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="64988-134">Remarks</span></span>

<span data-ttu-id="64988-135">I nomi delle reti virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio, "rete" e "rete" si riferiscono alla stessa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="64988-135">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="64988-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64988-136">Requirements</span></span>



| <span data-ttu-id="64988-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="64988-137">Requirement</span></span> | <span data-ttu-id="64988-138">Valore</span><span class="sxs-lookup"><span data-stu-id="64988-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="64988-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64988-139">Minimum supported client</span></span><br/> | <span data-ttu-id="64988-140">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="64988-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="64988-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64988-141">Minimum supported server</span></span><br/> | <span data-ttu-id="64988-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="64988-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="64988-143">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="64988-143">End of client support</span></span><br/>    | <span data-ttu-id="64988-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="64988-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="64988-145">Prodotto</span><span class="sxs-lookup"><span data-stu-id="64988-145">Product</span></span><br/>                  | <span data-ttu-id="64988-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="64988-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="64988-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64988-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="64988-148"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="64988-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="64988-149">IID</span><span class="sxs-lookup"><span data-stu-id="64988-149">IID</span></span><br/>                      | <span data-ttu-id="64988-150">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="64988-150">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="64988-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64988-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64988-152">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="64988-152">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

