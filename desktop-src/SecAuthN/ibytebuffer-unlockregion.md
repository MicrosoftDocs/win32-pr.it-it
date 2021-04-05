---
description: 'Rimuove la restrizione di accesso in un intervallo di byte precedentemente limitato utilizzando IByteBuffer:: LockRegion.'
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'Metodo IByteBuffer:: UnlockRegion (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92e49ba000177326ad14d3b83002613a15e96e18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968295"
---
# <a name="ibytebufferunlockregion-method"></a><span data-ttu-id="4235e-103">Metodo IByteBuffer:: UnlockRegion</span><span class="sxs-lookup"><span data-stu-id="4235e-103">IByteBuffer::UnlockRegion method</span></span>

<span data-ttu-id="4235e-104">\[Il metodo **UnlockRegion** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="4235e-104">\[The **UnlockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4235e-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4235e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4235e-106">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="4235e-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="4235e-107">Il metodo **UnlockRegion** rimuove la restrizione di accesso in un intervallo di byte precedentemente limitato tramite [**IByteBuffer:: LockRegion**](ibytebuffer-lockregion.md).</span><span class="sxs-lookup"><span data-stu-id="4235e-107">The **UnlockRegion** method removes the access restriction on a range of bytes previously restricted by using [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4235e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4235e-108">Syntax</span></span>


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="4235e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4235e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4235e-110">*libOffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4235e-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4235e-111">Offset di byte per l'inizio dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="4235e-111">Byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="4235e-112">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4235e-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4235e-113">Lunghezza, in byte, dell'intervallo da limitare.</span><span class="sxs-lookup"><span data-stu-id="4235e-113">Length, in bytes, of the range to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="4235e-114">*dwLockType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4235e-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4235e-115">Restrizioni di accesso inserite in precedenza nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="4235e-115">Access restrictions previously placed on the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4235e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4235e-116">Return value</span></span>

<span data-ttu-id="4235e-117">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4235e-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="4235e-118">Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="4235e-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4235e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4235e-119">Remarks</span></span>

<span data-ttu-id="4235e-120">Il metodo **IByteBuffer:: UnlockRegion** Sblocca un'area precedentemente bloccata usando il metodo [**IByteBuffer:: LockRegion**](ibytebuffer-lockregion.md) .</span><span class="sxs-lookup"><span data-stu-id="4235e-120">The **IByteBuffer::UnlockRegion** method unlocks a region previously locked by using the [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md) method.</span></span> <span data-ttu-id="4235e-121">Le aree bloccate devono essere sbloccate in seguito in modo esplicito chiamando **IByteBuffer:: UnlockRegion** con esattamente gli stessi valori per i parametri *libOffset*, *CB* e *dwLockType* .</span><span class="sxs-lookup"><span data-stu-id="4235e-121">Locked regions must later be explicitly unlocked by calling **IByteBuffer::UnlockRegion** with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="4235e-122">L'area deve essere sbloccata prima che il flusso venga rilasciato.</span><span class="sxs-lookup"><span data-stu-id="4235e-122">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="4235e-123">Due aree adiacenti non possono essere bloccate separatamente e quindi sbloccate con una singola chiamata di sblocco.</span><span class="sxs-lookup"><span data-stu-id="4235e-123">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="4235e-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="4235e-124">Examples</span></span>

<span data-ttu-id="4235e-125">Nell'esempio seguente viene illustrato lo sblocco di un intervallo di byte.</span><span class="sxs-lookup"><span data-stu-id="4235e-125">The following example shows unlocking a range of bytes.</span></span>


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="4235e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4235e-126">Requirements</span></span>



| <span data-ttu-id="4235e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4235e-127">Requirement</span></span> | <span data-ttu-id="4235e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="4235e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4235e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4235e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4235e-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4235e-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4235e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4235e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4235e-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4235e-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4235e-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4235e-133">End of client support</span></span><br/>    | <span data-ttu-id="4235e-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4235e-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4235e-135">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4235e-135">End of server support</span></span><br/>    | <span data-ttu-id="4235e-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4235e-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4235e-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4235e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4235e-138"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4235e-138"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4235e-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4235e-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="4235e-140"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4235e-140"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4235e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4235e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4235e-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4235e-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4235e-143">IID</span><span class="sxs-lookup"><span data-stu-id="4235e-143">IID</span></span><br/>                      | <span data-ttu-id="4235e-144">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="4235e-144">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

