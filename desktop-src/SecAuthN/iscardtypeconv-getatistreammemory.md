---
description: Acquisisce un puntatore di byte al blocco di memoria HGLOBAL gestito dall'interfaccia COM IStream.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'Metodo ISCardTypeConv:: GetAtIStreamMemory (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bdd828921f18c3d06edd2d41da189260a4ed4394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750034"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a><span data-ttu-id="9fda5-103">Metodo ISCardTypeConv:: GetAtIStreamMemory</span><span class="sxs-lookup"><span data-stu-id="9fda5-103">ISCardTypeConv::GetAtIStreamMemory method</span></span>

<span data-ttu-id="9fda5-104">\[Il metodo **GetAtIStreamMemory** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="9fda5-104">\[The **GetAtIStreamMemory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9fda5-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9fda5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9fda5-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="9fda5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9fda5-107">Il metodo **GetAtIStreamMemory** acquisisce un puntatore di byte al blocco di memoria HGLOBAL gestito dall'interfaccia com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="9fda5-107">The **GetAtIStreamMemory** method acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span>

<span data-ttu-id="9fda5-108">Si tratta di un modo per ottenere la memoria sotto il **IStream** senza dover ottenere il valore sizeof per il blocco di memoria in byte e leggere i byte in una matrice di byte temporanea usando l'interfaccia **IStream** .</span><span class="sxs-lookup"><span data-stu-id="9fda5-108">This is a way to get at the memory under the **IStream** without having to get the sizeof value for the memory block in bytes and read the bytes into a temporary byte array using the **IStream** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fda5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fda5-109">Syntax</span></span>


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a><span data-ttu-id="9fda5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fda5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fda5-111">*pStrm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fda5-111">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fda5-112">Puntatore all'interfaccia com **IStream** che gestisce il blocco di memoria HGLOBAL.</span><span class="sxs-lookup"><span data-stu-id="9fda5-112">A pointer to the **IStream** COM interface that manages the HGLOBAL memory block.</span></span>

</dd> <dt>

<span data-ttu-id="9fda5-113">*ppMem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9fda5-113">*ppMem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fda5-114">Puntatore al primo byte del blocco di memoria HGLOBAL in caso di esito positivo; else, **null** se l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9fda5-114">A pointer to the first byte of the HGLOBAL memory block if successful; else, **NULL** if operation fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fda5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fda5-115">Return value</span></span>

<span data-ttu-id="9fda5-116">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="9fda5-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9fda5-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9fda5-117">Return code</span></span>                                                                                   | <span data-ttu-id="9fda5-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fda5-118">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9fda5-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9fda5-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9fda5-120">Memoria allocata correttamente.</span><span class="sxs-lookup"><span data-stu-id="9fda5-120">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="9fda5-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9fda5-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9fda5-122">Si è verificato un problema con uno o più parametri passati nella funzione.</span><span class="sxs-lookup"><span data-stu-id="9fda5-122">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="9fda5-123"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="9fda5-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9fda5-124">Un parametro di tipo puntatore non è corretto.</span><span class="sxs-lookup"><span data-stu-id="9fda5-124">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="9fda5-125"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="9fda5-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9fda5-126">Memoria disponibile insufficiente per soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="9fda5-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="9fda5-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fda5-127">Remarks</span></span>

<span data-ttu-id="9fda5-128">Il conteggio dei riferimenti **IStream** verrà incrementato per ogni puntatore *ppMem* acquisito.</span><span class="sxs-lookup"><span data-stu-id="9fda5-128">The **IStream** reference count will be incremented for each *ppMem* pointer acquired.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fda5-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fda5-129">Requirements</span></span>



| <span data-ttu-id="9fda5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fda5-130">Requirement</span></span> | <span data-ttu-id="9fda5-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9fda5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fda5-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fda5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9fda5-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9fda5-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9fda5-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fda5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9fda5-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9fda5-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9fda5-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9fda5-136">End of client support</span></span><br/>    | <span data-ttu-id="9fda5-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9fda5-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9fda5-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9fda5-138">End of server support</span></span><br/>    | <span data-ttu-id="9fda5-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9fda5-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9fda5-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fda5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fda5-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fda5-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9fda5-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9fda5-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="9fda5-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9fda5-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9fda5-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9fda5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fda5-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fda5-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9fda5-146">IID</span><span class="sxs-lookup"><span data-stu-id="9fda5-146">IID</span></span><br/>                      | <span data-ttu-id="9fda5-147">IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="9fda5-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9fda5-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fda5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fda5-149">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="9fda5-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="9fda5-150">Valori restituiti da Smart Card</span><span class="sxs-lookup"><span data-stu-id="9fda5-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
