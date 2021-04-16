---
title: Metodo IVMVirtualPC GetHardDiskFiles (VPCCOMInterfaces. h)
description: Recupera una matrice di file di disco rigido virtuale noti.
ms.assetid: 3f949ebc-5974-4919-84a2-8411f558f85f
keywords:
- Metodo GetHardDiskFiles Virtual PC
- Metodo GetHardDiskFiles Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo GetHardDiskFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4162ae2667d389b445f44973c89a60fafd4c772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518784"
---
# <a name="ivmvirtualpcgetharddiskfiles-method"></a><span data-ttu-id="2dde3-106">Metodo IVMVirtualPC:: GetHardDiskFiles</span><span class="sxs-lookup"><span data-stu-id="2dde3-106">IVMVirtualPC::GetHardDiskFiles method</span></span>

<span data-ttu-id="2dde3-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2dde3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2dde3-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2dde3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2dde3-109">Recupera una matrice di file di disco rigido virtuale noti.</span><span class="sxs-lookup"><span data-stu-id="2dde3-109">Retrieves an array of known virtual hard disk files.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dde3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2dde3-110">Syntax</span></span>


```C++
HRESULT GetHardDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outHardDiskFileList
);
```



## <a name="parameters"></a><span data-ttu-id="2dde3-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="2dde3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dde3-112">*inAdditionalSearchPaths* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dde3-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dde3-113">Questi percorsi verranno cercati insieme ai percorsi impostati nella proprietà [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) .</span><span class="sxs-lookup"><span data-stu-id="2dde3-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="2dde3-114">*outHardDiskFileList* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2dde3-114">*outHardDiskFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2dde3-115">Matrice di stringhe di percorso per i file del disco rigido virtuale trovati nei percorsi di ricerca specificati.</span><span class="sxs-lookup"><span data-stu-id="2dde3-115">An array of path strings for the virtual hard disk files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dde3-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2dde3-116">Return value</span></span>

<span data-ttu-id="2dde3-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="2dde3-117">This method can return one of these values.</span></span>



| <span data-ttu-id="2dde3-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="2dde3-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="2dde3-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dde3-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2dde3-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2dde3-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="2dde3-121">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="2dde3-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="2dde3-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2dde3-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="2dde3-123">Il parametro *outHardDiskFileList* è **null**.</span><span class="sxs-lookup"><span data-stu-id="2dde3-123">The *outHardDiskFileList* parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="2dde3-124"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2dde3-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="2dde3-125">Il parametro *inAdditionalSearchPaths* non è una matrice di stringhe.</span><span class="sxs-lookup"><span data-stu-id="2dde3-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="2dde3-126"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2dde3-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="2dde3-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="2dde3-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="2dde3-128"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="2dde3-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="2dde3-129">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="2dde3-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2dde3-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="2dde3-130">Remarks</span></span>

<span data-ttu-id="2dde3-131">I percorsi di ricerca usati per recuperare la matrice di file includeranno quelli impostati in precedenza da [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) , oltre a quelli specificati dal parametro *inAdditionalSearchPaths* .</span><span class="sxs-lookup"><span data-stu-id="2dde3-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dde3-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2dde3-132">Requirements</span></span>



| <span data-ttu-id="2dde3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dde3-133">Requirement</span></span> | <span data-ttu-id="2dde3-134">Valore</span><span class="sxs-lookup"><span data-stu-id="2dde3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dde3-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dde3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2dde3-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2dde3-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2dde3-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dde3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2dde3-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2dde3-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2dde3-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2dde3-139">End of client support</span></span><br/>    | <span data-ttu-id="2dde3-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2dde3-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2dde3-141">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2dde3-141">Product</span></span><br/>                  | <span data-ttu-id="2dde3-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2dde3-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2dde3-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2dde3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dde3-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dde3-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2dde3-145">IID</span><span class="sxs-lookup"><span data-stu-id="2dde3-145">IID</span></span><br/>                      | <span data-ttu-id="2dde3-146">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="2dde3-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2dde3-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2dde3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dde3-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="2dde3-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

