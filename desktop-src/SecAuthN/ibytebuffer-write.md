---
description: Il metodo Write scrive un numero specificato da byte nell'oggetto flusso a partire dal puntatore di ricerca corrente.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'Metodo IByteBuffer:: Write (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5f9b60a296041a18fbd850f1405088f5b0da2ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884513"
---
# <a name="ibytebufferwrite-method"></a><span data-ttu-id="59c6b-103">Metodo IByteBuffer:: Write</span><span class="sxs-lookup"><span data-stu-id="59c6b-103">IByteBuffer::Write method</span></span>

<span data-ttu-id="59c6b-104">\[Il metodo **Write** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="59c6b-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="59c6b-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="59c6b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="59c6b-106">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="59c6b-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="59c6b-107">Il metodo **Write** scrive un numero specificato da byte nell'oggetto flusso a partire dal puntatore di ricerca corrente.</span><span class="sxs-lookup"><span data-stu-id="59c6b-107">The **Write** method writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c6b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59c6b-108">Syntax</span></span>


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="59c6b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="59c6b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59c6b-110">*pByte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59c6b-110">*pByte* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c6b-111">Indirizzo del buffer contenente i dati da scrivere nel flusso.</span><span class="sxs-lookup"><span data-stu-id="59c6b-111">Address of the buffer containing the data that is to be written to the stream.</span></span> <span data-ttu-id="59c6b-112">Per questo parametro è necessario specificare un puntatore valido anche quando *CB* è zero.</span><span class="sxs-lookup"><span data-stu-id="59c6b-112">A valid pointer must be provided for this parameter even when *cb* is zero.</span></span>

</dd> <dt>

<span data-ttu-id="59c6b-113">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59c6b-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c6b-114">Numero di byte di dati da provare a scrivere nel flusso.</span><span class="sxs-lookup"><span data-stu-id="59c6b-114">Number of bytes of data to attempt to write into the stream.</span></span> <span data-ttu-id="59c6b-115">Questo parametro può essere zero.</span><span class="sxs-lookup"><span data-stu-id="59c6b-115">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="59c6b-116">*pcbWritten* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="59c6b-116">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59c6b-117">Indirizzo di una variabile **Long** in cui questo metodo scrive il numero effettivo di byte scritti nell'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="59c6b-117">Address of a **LONG** variable where this method writes the actual number of bytes written to the stream object.</span></span> <span data-ttu-id="59c6b-118">Il chiamante può impostare questo puntatore su **null**. in questo caso, questo metodo non fornisce il numero effettivo di byte scritti.</span><span class="sxs-lookup"><span data-stu-id="59c6b-118">The caller can set this pointer to **NULL**, in which case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59c6b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59c6b-119">Return value</span></span>

<span data-ttu-id="59c6b-120">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="59c6b-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="59c6b-121">Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="59c6b-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="59c6b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="59c6b-122">Remarks</span></span>

<span data-ttu-id="59c6b-123">Il metodo **IByteBuffer:: Write** scrive i dati specificati in un oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="59c6b-123">The **IByteBuffer::Write** method writes the specified data to a stream object.</span></span> <span data-ttu-id="59c6b-124">Il puntatore di ricerca viene regolato per il numero di byte effettivamente scritti.</span><span class="sxs-lookup"><span data-stu-id="59c6b-124">The seek pointer is adjusted for the number of bytes actually written.</span></span> <span data-ttu-id="59c6b-125">Il numero di byte effettivamente scritti viene restituito nel parametro *pcbWritten* .</span><span class="sxs-lookup"><span data-stu-id="59c6b-125">The number of bytes actually written is returned in the *pcbWritten* parameter.</span></span> <span data-ttu-id="59c6b-126">Se il numero di byte è pari a zero byte, l'operazione di scrittura non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="59c6b-126">If the byte count is zero bytes, the write operation has no effect.</span></span>

<span data-ttu-id="59c6b-127">Se il puntatore di ricerca è attualmente oltre la fine del flusso e il numero di byte è diverso da zero, questo metodo aumenta le dimensioni del flusso al puntatore di ricerca e scrive i byte specificati a partire dal puntatore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="59c6b-127">If the seek pointer is currently past the end of the stream and the byte count is nonzero, this method increases the size of the stream to the seek pointer and writes the specified bytes starting at the seek pointer.</span></span> <span data-ttu-id="59c6b-128">I byte di riempimento scritti nel flusso non vengono inizializzati su un valore particolare.</span><span class="sxs-lookup"><span data-stu-id="59c6b-128">The fill bytes written to the stream are not initialized to any particular value.</span></span> <span data-ttu-id="59c6b-129">Questo comportamento è identico a quello della fine del file nella file system FAT di MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="59c6b-129">This is the same as the end-of-file behavior in the MS-DOS FAT file system.</span></span>

<span data-ttu-id="59c6b-130">Con un conteggio di zero byte e un puntatore di ricerca oltre la fine del flusso, questo metodo non crea i byte di riempimento per aumentare il flusso al puntatore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="59c6b-130">With a zero byte count and a seek pointer past the end of the stream, this method does not create the fill bytes to increase the stream to the seek pointer.</span></span> <span data-ttu-id="59c6b-131">In questo caso, è necessario chiamare il metodo [**IByteBuffer:: sesize**](ibytebuffer-setsize.md) per aumentare le dimensioni del flusso e scrivere i byte di riempimento.</span><span class="sxs-lookup"><span data-stu-id="59c6b-131">In this case, you must call the [**IByteBuffer::SetSize**](ibytebuffer-setsize.md) method to increase the size of the stream and write the fill bytes.</span></span>

<span data-ttu-id="59c6b-132">Il parametro *pcbWritten* può avere un valore anche se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="59c6b-132">The *pcbWritten* parameter can have a value even if an error occurs.</span></span>

<span data-ttu-id="59c6b-133">Nell'implementazione fornita da COM, gli oggetti flusso non sono di tipo sparse.</span><span class="sxs-lookup"><span data-stu-id="59c6b-133">In the COM-provided implementation, stream objects are not sparse.</span></span> <span data-ttu-id="59c6b-134">Tutti i byte di riempimento vengono infine allocati sul disco e assegnati al flusso.</span><span class="sxs-lookup"><span data-stu-id="59c6b-134">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

## <a name="examples"></a><span data-ttu-id="59c6b-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="59c6b-135">Examples</span></span>

<span data-ttu-id="59c6b-136">Nell'esempio seguente viene illustrata la scrittura di byte nell'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="59c6b-136">The following example shows writing bytes into the stream object.</span></span>


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
```



## <a name="requirements"></a><span data-ttu-id="59c6b-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59c6b-137">Requirements</span></span>



| <span data-ttu-id="59c6b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="59c6b-138">Requirement</span></span> | <span data-ttu-id="59c6b-139">Valore</span><span class="sxs-lookup"><span data-stu-id="59c6b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59c6b-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59c6b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="59c6b-141">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="59c6b-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="59c6b-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59c6b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="59c6b-143">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59c6b-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="59c6b-144">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="59c6b-144">End of client support</span></span><br/>    | <span data-ttu-id="59c6b-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="59c6b-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="59c6b-146">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="59c6b-146">End of server support</span></span><br/>    | <span data-ttu-id="59c6b-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="59c6b-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="59c6b-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59c6b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="59c6b-149"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="59c6b-149"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="59c6b-150">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="59c6b-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="59c6b-151"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="59c6b-151"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="59c6b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="59c6b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59c6b-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59c6b-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="59c6b-154">IID</span><span class="sxs-lookup"><span data-stu-id="59c6b-154">IID</span></span><br/>                      | <span data-ttu-id="59c6b-155">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="59c6b-155">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

