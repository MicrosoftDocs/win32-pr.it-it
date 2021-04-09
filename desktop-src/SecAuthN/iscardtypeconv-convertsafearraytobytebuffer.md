---
description: Converte una matrice di byte definita come SAFEARRAY in un buffer universale di byte (oggetto IStream).
ms.assetid: faa07bb5-cfdb-4181-b86a-f82a9c6b251a
title: 'Metodo ISCardTypeConv:: ConvertSafeArrayToByteBuffer (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertSafeArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aa6503f474d96e3c25da3f2780ac43976b6507a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966627"
---
# <a name="iscardtypeconvconvertsafearraytobytebuffer-method"></a><span data-ttu-id="dd313-103">Metodo ISCardTypeConv:: ConvertSafeArrayToByteBuffer</span><span class="sxs-lookup"><span data-stu-id="dd313-103">ISCardTypeConv::ConvertSafeArrayToByteBuffer method</span></span>

<span data-ttu-id="dd313-104">\[Il metodo **ConvertSafeArrayToByteBuffer** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="dd313-104">\[The **ConvertSafeArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dd313-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dd313-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dd313-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="dd313-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dd313-107">Il metodo **ConvertSafeArrayToByteBuffer** converte una matrice di byte definita come SafeArray in un buffer universale di byte (oggetto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="dd313-107">The **ConvertSafeArrayToByteBuffer** method converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="dd313-108">Il buffer di byte creato è un flusso mappato su un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="dd313-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="dd313-109">Per accedere o gestire il buffer, usare i metodi forniti dall'interfaccia **IStream** .</span><span class="sxs-lookup"><span data-stu-id="dd313-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="dd313-110">Una funzionalità univoca di questa implementazione di matrice è che, quando si chiama il metodo **IStream:: Release** , la memoria sottostante verrà rilasciata per l'utente.</span><span class="sxs-lookup"><span data-stu-id="dd313-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd313-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd313-111">Syntax</span></span>


```C++
HRESULT ConvertSafeArrayToByteBuffer(
  [in]  LPSAFEARRAY  pbyArray,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="dd313-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd313-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd313-113">*pbyArray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd313-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd313-114">Puntatore all'elemento SAFEARRAY da convertire.</span><span class="sxs-lookup"><span data-stu-id="dd313-114">Pointer to the SAFEARRAY to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="dd313-115">*ppbyBuff* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dd313-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd313-116">Puntatore all'oggetto **IStream** da restituire.</span><span class="sxs-lookup"><span data-stu-id="dd313-116">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd313-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd313-117">Return value</span></span>

<span data-ttu-id="dd313-118">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd313-118">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="dd313-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="dd313-119">Return code</span></span>                                                                                   | <span data-ttu-id="dd313-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd313-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dd313-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd313-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dd313-122">Memoria allocata correttamente.</span><span class="sxs-lookup"><span data-stu-id="dd313-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="dd313-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dd313-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dd313-124">Si è verificato un problema con uno o più parametri passati nella funzione.</span><span class="sxs-lookup"><span data-stu-id="dd313-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="dd313-125"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="dd313-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dd313-126">Un parametro di tipo puntatore non è corretto.</span><span class="sxs-lookup"><span data-stu-id="dd313-126">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="dd313-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="dd313-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dd313-128">Memoria disponibile insufficiente per soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="dd313-128">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="dd313-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd313-129">Remarks</span></span>

<span data-ttu-id="dd313-130">La memoria allocata è mobile.</span><span class="sxs-lookup"><span data-stu-id="dd313-130">Memory allocated is moveable.</span></span> <span data-ttu-id="dd313-131">Usare il metodo **IStream:: Release** per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="dd313-131">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd313-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd313-132">Requirements</span></span>



| <span data-ttu-id="dd313-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd313-133">Requirement</span></span> | <span data-ttu-id="dd313-134">Valore</span><span class="sxs-lookup"><span data-stu-id="dd313-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd313-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd313-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dd313-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dd313-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dd313-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd313-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dd313-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd313-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dd313-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="dd313-139">End of client support</span></span><br/>    | <span data-ttu-id="dd313-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dd313-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dd313-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="dd313-141">End of server support</span></span><br/>    | <span data-ttu-id="dd313-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd313-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dd313-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd313-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd313-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd313-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd313-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="dd313-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd313-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dd313-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dd313-147">DLL</span><span class="sxs-lookup"><span data-stu-id="dd313-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd313-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd313-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dd313-149">IID</span><span class="sxs-lookup"><span data-stu-id="dd313-149">IID</span></span><br/>                      | <span data-ttu-id="dd313-150">IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="dd313-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="dd313-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd313-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd313-152">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="dd313-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="dd313-153">Valori restituiti da Smart Card</span><span class="sxs-lookup"><span data-stu-id="dd313-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
