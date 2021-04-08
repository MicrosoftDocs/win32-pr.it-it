---
description: Crea un buffer universale di byte mappato in un oggetto IStream (IByteBuffer).
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: 'Metodo ISCardTypeConv:: CreateByteBuffer (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ab69c8061d2e2740e652e29b2fe6407574fe7076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050079"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a><span data-ttu-id="95036-103">Metodo ISCardTypeConv:: CreateByteBuffer</span><span class="sxs-lookup"><span data-stu-id="95036-103">ISCardTypeConv::CreateByteBuffer method</span></span>

<span data-ttu-id="95036-104">\[Il metodo **CreateByteBuffer** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="95036-104">\[The **CreateByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="95036-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="95036-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="95036-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="95036-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="95036-107">Il metodo **CreateByteBuffer** crea un buffer universale di byte mappato in un oggetto **IStream** ([**IByteBuffer**](ibytebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="95036-107">The **CreateByteBuffer** method creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span>

<span data-ttu-id="95036-108">Il buffer di byte creato è un flusso mappato su un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="95036-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="95036-109">Per accedere o gestire il buffer, usare i metodi forniti dall'interfaccia **IStream** .</span><span class="sxs-lookup"><span data-stu-id="95036-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="95036-110">Una funzionalità univoca di questa implementazione di matrice è che, quando si chiama il metodo **IStream:: Release** , la memoria sottostante verrà rilasciata per l'utente.</span><span class="sxs-lookup"><span data-stu-id="95036-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="95036-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95036-111">Syntax</span></span>


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="95036-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="95036-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95036-113">*dwAllocSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95036-113">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95036-114">Dimensioni in byte della memoria da allocare per la matrice.</span><span class="sxs-lookup"><span data-stu-id="95036-114">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="95036-115">*ppbyBuff* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="95036-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95036-116">Puntatore all'oggetto IStream da restituire.</span><span class="sxs-lookup"><span data-stu-id="95036-116">Pointer to the IStream object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95036-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95036-117">Return value</span></span>

<span data-ttu-id="95036-118">I possibili valori restituiti sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="95036-118">The possible return values are the following:</span></span>



| <span data-ttu-id="95036-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="95036-119">Return code</span></span>                                                                                   | <span data-ttu-id="95036-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95036-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95036-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="95036-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="95036-122">Memoria allocata correttamente.</span><span class="sxs-lookup"><span data-stu-id="95036-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="95036-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="95036-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="95036-124">Si è verificato un problema con uno o più parametri passati nella funzione.</span><span class="sxs-lookup"><span data-stu-id="95036-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="95036-125"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="95036-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="95036-126">Memoria disponibile insufficiente per soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="95036-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="95036-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="95036-127">Remarks</span></span>

<span data-ttu-id="95036-128">La memoria allocata è movibile.</span><span class="sxs-lookup"><span data-stu-id="95036-128">Memory allocated is movable.</span></span> <span data-ttu-id="95036-129">Usare il metodo **IStream:: Release** per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="95036-129">Use the **IStream::Release** method to free the memory.</span></span>

<span data-ttu-id="95036-130">Per creare una matrice di byte C/C++ tipica, chiamare [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span><span class="sxs-lookup"><span data-stu-id="95036-130">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="95036-131">Per creare un SAFEARRAY di automazione di caratteri non firmati (byte), chiamare [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span><span class="sxs-lookup"><span data-stu-id="95036-131">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95036-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95036-132">Requirements</span></span>



| <span data-ttu-id="95036-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="95036-133">Requirement</span></span> | <span data-ttu-id="95036-134">Valore</span><span class="sxs-lookup"><span data-stu-id="95036-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95036-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95036-135">Minimum supported client</span></span><br/> | <span data-ttu-id="95036-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="95036-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="95036-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95036-137">Minimum supported server</span></span><br/> | <span data-ttu-id="95036-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95036-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95036-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="95036-139">End of client support</span></span><br/>    | <span data-ttu-id="95036-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="95036-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="95036-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="95036-141">End of server support</span></span><br/>    | <span data-ttu-id="95036-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="95036-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="95036-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95036-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="95036-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="95036-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="95036-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="95036-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="95036-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="95036-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="95036-147">DLL</span><span class="sxs-lookup"><span data-stu-id="95036-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95036-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95036-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="95036-149">IID</span><span class="sxs-lookup"><span data-stu-id="95036-149">IID</span></span><br/>                      | <span data-ttu-id="95036-150">IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="95036-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="95036-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95036-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95036-152">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="95036-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="95036-153">Valori restituiti da Smart Card</span><span class="sxs-lookup"><span data-stu-id="95036-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="95036-154">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="95036-154">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="95036-155">**CreateSafeArray**</span><span class="sxs-lookup"><span data-stu-id="95036-155">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
