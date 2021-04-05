---
description: Converte una matrice di byte C/C++ tipica in un buffer universale di byte (oggetto IStream).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'Metodo ISCardTypeConv:: ConvertByteArrayToByteBuffer (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884482"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a><span data-ttu-id="b2f0b-103">Metodo ISCardTypeConv:: ConvertByteArrayToByteBuffer</span><span class="sxs-lookup"><span data-stu-id="b2f0b-103">ISCardTypeConv::ConvertByteArrayToByteBuffer method</span></span>

<span data-ttu-id="b2f0b-104">\[Il metodo **ConvertByteArrayToByteBuffer** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-104">\[The **ConvertByteArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b2f0b-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b2f0b-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="b2f0b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b2f0b-107">Il metodo **ConvertByteArrayToByteBuffer** converte una matrice di byte C/C++ tipica in un buffer universale di byte (oggetto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="b2f0b-107">The **ConvertByteArrayToByteBuffer** method converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="b2f0b-108">Il buffer di byte creato è un flusso mappato su un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="b2f0b-109">Per accedere o gestire il buffer, usare i metodi forniti dall'interfaccia **IStream** .</span><span class="sxs-lookup"><span data-stu-id="b2f0b-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="b2f0b-110">Una funzionalità univoca di questa implementazione di matrice è che, quando si chiama il metodo **IStream:: Release** , la memoria sottostante verrà rilasciata per l'utente.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f0b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2f0b-111">Syntax</span></span>


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b2f0b-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2f0b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2f0b-113">*pbyArray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2f0b-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2f0b-114">Puntatore alla matrice di byte da convertire.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-114">Pointer to the array of bytes to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="b2f0b-115">*dwArraySize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2f0b-115">*dwArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2f0b-116">Dimensioni della matrice di byte da convertire.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-116">Size of the byte array to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="b2f0b-117">*ppbyBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2f0b-117">*ppbyBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2f0b-118">Puntatore all'oggetto **IStream** da restituire.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-118">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2f0b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2f0b-119">Return value</span></span>

<span data-ttu-id="b2f0b-120">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="b2f0b-120">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="b2f0b-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b2f0b-121">Return code</span></span>                                                                                   | <span data-ttu-id="b2f0b-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2f0b-122">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2f0b-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b2f0b-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b2f0b-124">Memoria allocata correttamente.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-124">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b2f0b-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b2f0b-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b2f0b-126">Si è verificato un problema con uno o più parametri passati nella funzione.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-126">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="b2f0b-127"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="b2f0b-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b2f0b-128">Un parametro di tipo puntatore non è corretto.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-128">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b2f0b-129"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="b2f0b-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b2f0b-130">Memoria disponibile insufficiente per soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-130">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="b2f0b-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2f0b-131">Remarks</span></span>

<span data-ttu-id="b2f0b-132">La memoria allocata è movibile.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-132">Memory allocated is movable.</span></span> <span data-ttu-id="b2f0b-133">Usare il metodo **IStream:: Release** per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="b2f0b-133">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f0b-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2f0b-134">Requirements</span></span>



| <span data-ttu-id="b2f0b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2f0b-135">Requirement</span></span> | <span data-ttu-id="b2f0b-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b2f0b-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f0b-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2f0b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b2f0b-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b2f0b-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b2f0b-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2f0b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b2f0b-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2f0b-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2f0b-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b2f0b-141">End of client support</span></span><br/>    | <span data-ttu-id="b2f0b-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b2f0b-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b2f0b-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b2f0b-143">End of server support</span></span><br/>    | <span data-ttu-id="b2f0b-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b2f0b-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b2f0b-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2f0b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2f0b-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2f0b-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2f0b-147">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b2f0b-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2f0b-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b2f0b-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b2f0b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b2f0b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2f0b-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2f0b-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2f0b-151">IID</span><span class="sxs-lookup"><span data-stu-id="b2f0b-151">IID</span></span><br/>                      | <span data-ttu-id="b2f0b-152">IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b2f0b-152">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b2f0b-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2f0b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f0b-154">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="b2f0b-154">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="b2f0b-155">Valori restituiti da Smart Card</span><span class="sxs-lookup"><span data-stu-id="b2f0b-155">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
