---
description: Crea un SAFEARRAY di automazione di caratteri non firmati (byte).
ms.assetid: 67cc8cd1-95be-4498-ac25-6c418089af27
title: 'Metodo ISCardTypeConv:: CreateSafeArray (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bc27a3f50f0740eca178787fd021f76c9b6729e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128095"
---
# <a name="iscardtypeconvcreatesafearray-method"></a><span data-ttu-id="76a1d-103">Metodo ISCardTypeConv:: CreateSafeArray</span><span class="sxs-lookup"><span data-stu-id="76a1d-103">ISCardTypeConv::CreateSafeArray method</span></span>

<span data-ttu-id="76a1d-104">\[Il metodo **CreateSafeArray** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="76a1d-104">\[The **CreateSafeArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="76a1d-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="76a1d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="76a1d-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="76a1d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="76a1d-107">Il metodo **CreateSafeArray** crea un SAFEARRAY di automazione di caratteri non firmati (byte).</span><span class="sxs-lookup"><span data-stu-id="76a1d-107">The **CreateSafeArray** method creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span>

## <a name="syntax"></a><span data-ttu-id="76a1d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76a1d-108">Syntax</span></span>


```C++
HRESULT CreateSafeArray(
  [in]  UINT        nAllocSize,
  [out] LPSAFEARRAY *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="76a1d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="76a1d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76a1d-110">*nAllocSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76a1d-110">*nAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76a1d-111">Dimensioni in byte della memoria da allocare per la matrice.</span><span class="sxs-lookup"><span data-stu-id="76a1d-111">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="76a1d-112">*ppArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="76a1d-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76a1d-113">Puntatore all'oggetto SAFEARRAY da restituire.</span><span class="sxs-lookup"><span data-stu-id="76a1d-113">Pointer to the SAFEARRAY object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76a1d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76a1d-114">Return value</span></span>

<span data-ttu-id="76a1d-115">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="76a1d-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="76a1d-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="76a1d-116">Return code</span></span>                                                                                   | <span data-ttu-id="76a1d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76a1d-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76a1d-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="76a1d-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="76a1d-119">Memoria allocata correttamente.</span><span class="sxs-lookup"><span data-stu-id="76a1d-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="76a1d-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="76a1d-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="76a1d-121">Si è verificato un problema con uno o più parametri passati nella funzione.</span><span class="sxs-lookup"><span data-stu-id="76a1d-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="76a1d-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="76a1d-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="76a1d-123">Memoria disponibile insufficiente per soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="76a1d-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="76a1d-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="76a1d-124">Remarks</span></span>

<span data-ttu-id="76a1d-125">Per creare una matrice di byte C/C++ tipica, chiamare [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span><span class="sxs-lookup"><span data-stu-id="76a1d-125">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="76a1d-126">Per creare un buffer universale di byte mappato in un oggetto **IStream** ([**IByteBuffer**](ibytebuffer.md)), chiamare [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="76a1d-126">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76a1d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76a1d-127">Requirements</span></span>



| <span data-ttu-id="76a1d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="76a1d-128">Requirement</span></span> | <span data-ttu-id="76a1d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="76a1d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76a1d-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76a1d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="76a1d-131">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="76a1d-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="76a1d-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76a1d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="76a1d-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="76a1d-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76a1d-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="76a1d-134">End of client support</span></span><br/>    | <span data-ttu-id="76a1d-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="76a1d-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="76a1d-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="76a1d-136">End of server support</span></span><br/>    | <span data-ttu-id="76a1d-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76a1d-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="76a1d-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76a1d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="76a1d-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="76a1d-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="76a1d-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="76a1d-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="76a1d-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="76a1d-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="76a1d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="76a1d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76a1d-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76a1d-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="76a1d-144">IID</span><span class="sxs-lookup"><span data-stu-id="76a1d-144">IID</span></span><br/>                      | <span data-ttu-id="76a1d-145">IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="76a1d-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="76a1d-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76a1d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76a1d-147">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="76a1d-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="76a1d-148">Valori restituiti da Smart Card</span><span class="sxs-lookup"><span data-stu-id="76a1d-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="76a1d-149">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="76a1d-149">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="76a1d-150">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="76a1d-150">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> </dl>

 

 
