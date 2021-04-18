---
title: Metodo IVMVirtualPC GetDVDFiles (VPCCOMInterfaces. h)
description: Recupera una matrice di file DVD noti.
ms.assetid: 9fe2191f-c5c0-464d-a190-29b2aba69682
keywords:
- Metodo GetDVDFiles Virtual PC
- Metodo GetDVDFiles Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo GetDVDFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetDVDFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a91d7f0d65d1f62feb21d41bd9b27bf6ce112ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302160"
---
# <a name="ivmvirtualpcgetdvdfiles-method"></a><span data-ttu-id="e0c56-106">Metodo IVMVirtualPC:: GetDVDFiles</span><span class="sxs-lookup"><span data-stu-id="e0c56-106">IVMVirtualPC::GetDVDFiles method</span></span>

<span data-ttu-id="e0c56-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e0c56-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e0c56-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e0c56-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e0c56-109">Recupera una matrice di file DVD noti.</span><span class="sxs-lookup"><span data-stu-id="e0c56-109">Retrieves an array of known DVD files.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c56-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0c56-110">Syntax</span></span>


```C++
HRESULT GetDVDFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outDVDFileList
);
```



## <a name="parameters"></a><span data-ttu-id="e0c56-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0c56-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0c56-112">*inAdditionalSearchPaths* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0c56-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0c56-113">Questi percorsi verranno cercati insieme ai percorsi impostati nella proprietà [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) .</span><span class="sxs-lookup"><span data-stu-id="e0c56-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="e0c56-114">*outDVDFileList* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e0c56-114">*outDVDFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e0c56-115">Matrice di file DVD virtuali trovati nei percorsi di ricerca specificati.</span><span class="sxs-lookup"><span data-stu-id="e0c56-115">An array of virtual DVD files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0c56-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0c56-116">Return value</span></span>

<span data-ttu-id="e0c56-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="e0c56-117">This method can return one of these values.</span></span>



| <span data-ttu-id="e0c56-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0c56-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="e0c56-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0c56-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0c56-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e0c56-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="e0c56-121">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e0c56-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e0c56-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e0c56-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="e0c56-123">Il parametro *outDVDFileList* è **null**.</span><span class="sxs-lookup"><span data-stu-id="e0c56-123">The *outDVDFileList* parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="e0c56-124"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e0c56-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="e0c56-125">Il parametro *inAdditionalSearchPaths* non è una matrice di stringhe.</span><span class="sxs-lookup"><span data-stu-id="e0c56-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="e0c56-126"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e0c56-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="e0c56-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="e0c56-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="e0c56-128"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="e0c56-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="e0c56-129">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="e0c56-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e0c56-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0c56-130">Remarks</span></span>

<span data-ttu-id="e0c56-131">I percorsi di ricerca usati per recuperare la matrice di file includeranno quelli impostati in precedenza da [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) , oltre a quelli specificati dal parametro *inAdditionalSearchPaths* e dal percorso del programma di installazione per il modulo Integration Components.</span><span class="sxs-lookup"><span data-stu-id="e0c56-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter and the installer location for the integration components module.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c56-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0c56-132">Requirements</span></span>



| <span data-ttu-id="e0c56-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0c56-133">Requirement</span></span> | <span data-ttu-id="e0c56-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e0c56-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c56-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0c56-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e0c56-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e0c56-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e0c56-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0c56-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e0c56-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e0c56-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e0c56-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e0c56-139">End of client support</span></span><br/>    | <span data-ttu-id="e0c56-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0c56-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e0c56-141">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e0c56-141">Product</span></span><br/>                  | <span data-ttu-id="e0c56-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e0c56-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e0c56-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0c56-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0c56-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0c56-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e0c56-145">IID</span><span class="sxs-lookup"><span data-stu-id="e0c56-145">IID</span></span><br/>                      | <span data-ttu-id="e0c56-146">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="e0c56-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e0c56-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0c56-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0c56-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="e0c56-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

