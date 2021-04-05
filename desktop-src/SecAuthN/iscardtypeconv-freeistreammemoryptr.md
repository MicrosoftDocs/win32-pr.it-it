---
description: Libera il puntatore di byte che punta al blocco di memoria HGLOBAL gestito da un'interfaccia COM IStream.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: 'Metodo ISCardTypeConv:: FreeIStreamMemoryPtr (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 12912b8130ed6e1ccaa995f88069b59e96f57c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756875"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a><span data-ttu-id="9f81d-103">Metodo ISCardTypeConv:: FreeIStreamMemoryPtr</span><span class="sxs-lookup"><span data-stu-id="9f81d-103">ISCardTypeConv::FreeIStreamMemoryPtr method</span></span>

<span data-ttu-id="9f81d-104">\[Il metodo **FreeIStreamMemoryPtr** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="9f81d-104">\[The **FreeIStreamMemoryPtr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9f81d-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9f81d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9f81d-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="9f81d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9f81d-107">Il metodo **FreeIStreamMemoryPtr** libera il puntatore di byte che punta al blocco di memoria HGLOBAL gestito da un'interfaccia com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="9f81d-107">The **FreeIStreamMemoryPtr** method frees the byte pointer pointing to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f81d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f81d-108">Syntax</span></span>


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a><span data-ttu-id="9f81d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f81d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f81d-110">*pStrm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f81d-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f81d-111">Puntatore all'interfaccia **IStream** che gestisce il blocco di memoria a cui punta *PMEM*.</span><span class="sxs-lookup"><span data-stu-id="9f81d-111">Pointer to the **IStream** interface that manages the memory block pointed to by *pMem*.</span></span>

</dd> <dt>

<span data-ttu-id="9f81d-112">*PMEM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f81d-112">*pMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f81d-113">Puntatore al blocco di memoria gestito dall'interfaccia **IStream** .</span><span class="sxs-lookup"><span data-stu-id="9f81d-113">Pointer to the memory block managed by the **IStream** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f81d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f81d-114">Return value</span></span>

<span data-ttu-id="9f81d-115">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f81d-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="9f81d-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9f81d-116">Return code</span></span>                                                                                   | <span data-ttu-id="9f81d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f81d-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f81d-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9f81d-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9f81d-119">Memoria allocata correttamente.</span><span class="sxs-lookup"><span data-stu-id="9f81d-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="9f81d-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9f81d-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9f81d-121">Si è verificato un problema con uno o più parametri passati nella funzione.</span><span class="sxs-lookup"><span data-stu-id="9f81d-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="9f81d-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="9f81d-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9f81d-123">Un parametro di tipo puntatore non è corretto.</span><span class="sxs-lookup"><span data-stu-id="9f81d-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="9f81d-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="9f81d-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9f81d-125">Memoria disponibile insufficiente per soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="9f81d-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="9f81d-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f81d-126">Remarks</span></span>

<span data-ttu-id="9f81d-127">Questa funzione rilascia completamente e in modo pulito il puntatore di byte che punta al blocco di memoria HGLOBAL gestito dall'interfaccia **IStream** .</span><span class="sxs-lookup"><span data-stu-id="9f81d-127">This function completely and cleanly releases the byte pointer pointing to the HGLOBAL memory block managed by the **IStream** interface.</span></span> <span data-ttu-id="9f81d-128">Il puntatore di byte viene acquisito da una chiamata a [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).</span><span class="sxs-lookup"><span data-stu-id="9f81d-128">The byte pointer is acquired by a call to [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f81d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f81d-129">Requirements</span></span>



| <span data-ttu-id="9f81d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f81d-130">Requirement</span></span> | <span data-ttu-id="9f81d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9f81d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f81d-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f81d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9f81d-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9f81d-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9f81d-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f81d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9f81d-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f81d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9f81d-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9f81d-136">End of client support</span></span><br/>    | <span data-ttu-id="9f81d-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9f81d-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9f81d-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9f81d-138">End of server support</span></span><br/>    | <span data-ttu-id="9f81d-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f81d-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9f81d-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f81d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f81d-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f81d-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f81d-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9f81d-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="9f81d-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9f81d-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9f81d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9f81d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f81d-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f81d-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9f81d-146">IID</span><span class="sxs-lookup"><span data-stu-id="9f81d-146">IID</span></span><br/>                      | <span data-ttu-id="9f81d-147">IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="9f81d-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9f81d-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f81d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f81d-149">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="9f81d-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="9f81d-150">Valori restituiti da Smart Card</span><span class="sxs-lookup"><span data-stu-id="9f81d-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="9f81d-151">**GetAtIStreamMemory**</span><span class="sxs-lookup"><span data-stu-id="9f81d-151">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
