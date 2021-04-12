---
description: Limita l'accesso a un intervallo di byte specificato nell'oggetto buffer.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'Metodo IByteBuffer:: LockRegion (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233280"
---
# <a name="ibytebufferlockregion-method"></a><span data-ttu-id="cd9e4-103">Metodo IByteBuffer:: LockRegion</span><span class="sxs-lookup"><span data-stu-id="cd9e4-103">IByteBuffer::LockRegion method</span></span>

<span data-ttu-id="cd9e4-104">\[Il metodo **LockRegion** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-104">\[The **LockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cd9e4-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cd9e4-106">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="cd9e4-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="cd9e4-107">Il metodo **LockRegion** limita l'accesso a un intervallo di byte specificato nell'oggetto buffer.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-107">The **LockRegion** method restricts access to a specified range of bytes in the buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd9e4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd9e4-108">Syntax</span></span>


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="cd9e4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd9e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd9e4-110">*libOffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd9e4-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9e4-111">Integer che specifica l'offset di byte per l'inizio dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-111">Integer that specifies the byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="cd9e4-112">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd9e4-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9e4-113">Integer che specifica la lunghezza dell'intervallo, in byte, da limitare.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-113">Integer that specifies the length of the range, in bytes, to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="cd9e4-114">*dwLockType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd9e4-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd9e4-115">Specifica le restrizioni richieste per l'accesso all'intervallo.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-115">Specifies the restrictions being requested on accessing the range.</span></span> <span data-ttu-id="cd9e4-116">Può corrispondere a uno dei valori riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-116">This can be one of the values in the following table.</span></span>



| <span data-ttu-id="cd9e4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9e4-117">Value</span></span>                                                                                                                                                            | <span data-ttu-id="cd9e4-118">Significato</span><span class="sxs-lookup"><span data-stu-id="cd9e4-118">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <span data-ttu-id="cd9e4-119"><dt>**\_scrittura blocco**</dt></span><span class="sxs-lookup"><span data-stu-id="cd9e4-119"><dt>**LOCK\_WRITE**</dt></span></span> </dl>             | <span data-ttu-id="cd9e4-120">L'intervallo di byte specificato può essere aperto e letto un numero qualsiasi di volte, ma non è consentito scrivere nell'intervallo bloccato, ad eccezione del proprietario a cui è stato concesso il blocco.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-120">The specified range of bytes can be opened and read any number of times, but writing to the locked range is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <span data-ttu-id="cd9e4-121"><dt>**BLOCCO \_ esclusivo**</dt></span><span class="sxs-lookup"><span data-stu-id="cd9e4-121"><dt>**LOCK\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="cd9e4-122">La scrittura nell'intervallo di byte specificato non è consentita ad eccezione del proprietario a cui è stato concesso il blocco.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-122">Writing to the specified range of bytes is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <span data-ttu-id="cd9e4-123"><dt>**BLOCCA \_ ONLYONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="cd9e4-123"><dt>**LOCK\_ONLYONCE**</dt></span></span> </dl>    | <span data-ttu-id="cd9e4-124">Se questo blocco viene concesso, non è \_ possibile ottenere nessun altro blocco ONLYONCE di blocco sull'intervallo.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-124">If this lock is granted, no other LOCK\_ONLYONCE lock can be obtained on the range.</span></span> <span data-ttu-id="cd9e4-125">In genere questo tipo di blocco è un alias per un altro tipo di blocco.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-125">Usually this lock type is an alias for some other lock type.</span></span> <span data-ttu-id="cd9e4-126">In questo modo, le implementazioni specifiche possono avere un comportamento aggiuntivo associato a questo tipo di blocco.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-126">Thus, specific implementations can have additional behavior associated with this lock type.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd9e4-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd9e4-127">Return value</span></span>

<span data-ttu-id="cd9e4-128">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="cd9e4-129">Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-129">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd9e4-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd9e4-130">Remarks</span></span>

<span data-ttu-id="cd9e4-131">L'intervallo di byte può estendersi oltre la fine corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-131">The byte range can extend past the current end of the stream.</span></span> <span data-ttu-id="cd9e4-132">Il blocco oltre la fine di un flusso è utile come metodo di comunicazione tra istanze diverse del flusso senza modificare i dati che fanno effettivamente parte del flusso.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-132">Locking beyond the end of a stream is useful as a method of communication between different instances of the stream without changing data that is actually part of the stream.</span></span>

<span data-ttu-id="cd9e4-133">È possibile supportare tre tipi di blocco: blocco per escludere altri writer, blocco per escludere altri Reader o writer e blocco che consente a un solo richiedente di ottenere un blocco sull'intervallo specificato, che è in genere un alias per uno degli altri due tipi di blocco.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-133">Three types of locking can be supported: locking to exclude other writers, locking to exclude other readers or writers, and locking that allows only one requester to obtain a lock on the given range, which is usually an alias for one of the other two lock types.</span></span> <span data-ttu-id="cd9e4-134">Un'istanza del flusso specificata può supportare uno dei primi due tipi o entrambi.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-134">A given stream instance might support either of the first two types, or both.</span></span> <span data-ttu-id="cd9e4-135">Il tipo di blocco viene specificato da *dwLockType*, usando un valore dell'enumerazione [**LockType**](/windows/win32/api/objidl/ne-objidl-locktype) .</span><span class="sxs-lookup"><span data-stu-id="cd9e4-135">The lock type is specified by *dwLockType*, using a value from the [**LOCKTYPE**](/windows/win32/api/objidl/ne-objidl-locktype) enumeration.</span></span>

<span data-ttu-id="cd9e4-136">Qualsiasi area bloccata con **LockRegion** deve essere sbloccata in seguito in modo esplicito tramite la chiamata a [**IByteBuffer:: UnlockRegion**](ibytebuffer-unlockregion.md) con esattamente gli stessi valori per i parametri *libOffset*, *CB* e *dwLockType* .</span><span class="sxs-lookup"><span data-stu-id="cd9e4-136">Any region locked with **LockRegion** must later be explicitly unlocked by calling [**IByteBuffer::UnlockRegion**](ibytebuffer-unlockregion.md) with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="cd9e4-137">L'area deve essere sbloccata prima che il flusso venga rilasciato.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-137">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="cd9e4-138">Due aree adiacenti non possono essere bloccate separatamente e quindi sbloccate con una singola chiamata di sblocco.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-138">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="cd9e4-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="cd9e4-139">Examples</span></span>

<span data-ttu-id="cd9e4-140">Nell'esempio seguente viene illustrato come limitare l'accesso a un intervallo di byte.</span><span class="sxs-lookup"><span data-stu-id="cd9e4-140">The following example shows restricting access to a range of bytes.</span></span>


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="cd9e4-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd9e4-141">Requirements</span></span>



| <span data-ttu-id="cd9e4-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd9e4-142">Requirement</span></span> | <span data-ttu-id="cd9e4-143">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9e4-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9e4-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd9e4-144">Minimum supported client</span></span><br/> | <span data-ttu-id="cd9e4-145">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cd9e4-145">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cd9e4-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd9e4-146">Minimum supported server</span></span><br/> | <span data-ttu-id="cd9e4-147">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd9e4-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cd9e4-148">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="cd9e4-148">End of client support</span></span><br/>    | <span data-ttu-id="cd9e4-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd9e4-149">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cd9e4-150">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="cd9e4-150">End of server support</span></span><br/>    | <span data-ttu-id="cd9e4-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd9e4-151">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cd9e4-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd9e4-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd9e4-153"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd9e4-153"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd9e4-154">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="cd9e4-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd9e4-155"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cd9e4-155"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cd9e4-156">DLL</span><span class="sxs-lookup"><span data-stu-id="cd9e4-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd9e4-157"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd9e4-157"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cd9e4-158">IID</span><span class="sxs-lookup"><span data-stu-id="cd9e4-158">IID</span></span><br/>                      | <span data-ttu-id="cd9e4-159">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="cd9e4-159">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

