---
title: Metodo IVMVirtualPC GetVirtualMachineFiles (VPCCOMInterfaces. h)
description: Recupera una matrice di file di configurazione della macchina virtuale noti.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- Metodo GetVirtualMachineFiles Virtual PC
- Metodo GetVirtualMachineFiles Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo GetVirtualMachineFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d1fe248b76756b39846d181341278f669d2f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341223"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a><span data-ttu-id="57116-106">Metodo IVMVirtualPC:: GetVirtualMachineFiles</span><span class="sxs-lookup"><span data-stu-id="57116-106">IVMVirtualPC::GetVirtualMachineFiles method</span></span>

<span data-ttu-id="57116-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="57116-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="57116-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="57116-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="57116-109">Recupera una matrice di file di configurazione della macchina virtuale noti.</span><span class="sxs-lookup"><span data-stu-id="57116-109">Retrieves an array of known virtual machine configuration files.</span></span>

## <a name="syntax"></a><span data-ttu-id="57116-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57116-110">Syntax</span></span>


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a><span data-ttu-id="57116-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="57116-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57116-112">*inAdditionalSearchPaths* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57116-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57116-113">Questi percorsi verranno cercati insieme ai percorsi impostati nelle proprietà [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) e [**IVMVirtualPC::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) .</span><span class="sxs-lookup"><span data-stu-id="57116-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="57116-114">*inExcludedRegisteredVMs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57116-114">*inExcludedRegisteredVMs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57116-115">**True** se le macchine virtuali registrate devono essere escluse dalla matrice restituita nel parametro *outVirtualMachineFileList* e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="57116-115">**TRUE** if registered virtual machines should be excluded from the array return in the *outVirtualMachineFileList* parameter and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="57116-116">*outVirtualMachineFileList* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="57116-116">*outVirtualMachineFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="57116-117">Matrice di stringhe di percorso per i file di configurazione della macchina virtuale trovati nei percorsi di ricerca specificati.</span><span class="sxs-lookup"><span data-stu-id="57116-117">An array of path strings for the virtual machine configuration files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57116-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57116-118">Return value</span></span>

<span data-ttu-id="57116-119">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="57116-119">This method can return one of these values.</span></span>



| <span data-ttu-id="57116-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="57116-120">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="57116-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57116-121">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="57116-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="57116-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="57116-123">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="57116-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="57116-124"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="57116-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="57116-125">Il parametro *outVirtualMachineFileList* è **null**.</span><span class="sxs-lookup"><span data-stu-id="57116-125">The *outVirtualMachineFileList* parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="57116-126"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="57116-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="57116-127">Il parametro *inAdditionalSearchPaths* non è una matrice di stringhe.</span><span class="sxs-lookup"><span data-stu-id="57116-127">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="57116-128"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="57116-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="57116-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="57116-129">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="57116-130"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="57116-130"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="57116-131">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="57116-131">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="57116-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="57116-132">Remarks</span></span>

<span data-ttu-id="57116-133">I percorsi di ricerca usati per recuperare la matrice di file di configurazione includeranno quelli impostati in precedenza da [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) e [**IVMVirtualPC::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) , oltre a quelli specificati dal parametro *inAdditionalSearchPaths* .</span><span class="sxs-lookup"><span data-stu-id="57116-133">The search paths used to retrieve the array of configuration files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="57116-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57116-134">Requirements</span></span>



| <span data-ttu-id="57116-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="57116-135">Requirement</span></span> | <span data-ttu-id="57116-136">Valore</span><span class="sxs-lookup"><span data-stu-id="57116-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="57116-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57116-137">Minimum supported client</span></span><br/> | <span data-ttu-id="57116-138">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="57116-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57116-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57116-139">Minimum supported server</span></span><br/> | <span data-ttu-id="57116-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="57116-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="57116-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="57116-141">End of client support</span></span><br/>    | <span data-ttu-id="57116-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="57116-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="57116-143">Prodotto</span><span class="sxs-lookup"><span data-stu-id="57116-143">Product</span></span><br/>                  | <span data-ttu-id="57116-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="57116-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="57116-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57116-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="57116-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="57116-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="57116-147">IID</span><span class="sxs-lookup"><span data-stu-id="57116-147">IID</span></span><br/>                      | <span data-ttu-id="57116-148">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="57116-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="57116-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57116-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57116-150">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="57116-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

