---
description: Il metodo Read legge un numero specificato di byte dall'oggetto buffer in memoria a partire dal puntatore di ricerca corrente.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'Metodo IByteBuffer:: Read (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0574fb640d60fd8af824ff54abce5d109675ba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233278"
---
# <a name="ibytebufferread-method"></a><span data-ttu-id="d817b-103">Metodo IByteBuffer:: Read</span><span class="sxs-lookup"><span data-stu-id="d817b-103">IByteBuffer::Read method</span></span>

<span data-ttu-id="d817b-104">\[Il metodo **Read** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d817b-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d817b-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d817b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d817b-106">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="d817b-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="d817b-107">Il metodo **Read** legge un numero specificato di byte dall'oggetto buffer in memoria a partire dal puntatore di ricerca corrente.</span><span class="sxs-lookup"><span data-stu-id="d817b-107">The **Read** method reads a specified number of bytes from the buffer object into memory starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d817b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d817b-108">Syntax</span></span>


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="d817b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d817b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d817b-110">*pByte* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d817b-110">*pByte* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d817b-111">Punta al buffer in cui vengono letti i dati del flusso.</span><span class="sxs-lookup"><span data-stu-id="d817b-111">Points to the buffer into which the stream data is read.</span></span> <span data-ttu-id="d817b-112">Se si verifica un errore, questo valore è **null**.</span><span class="sxs-lookup"><span data-stu-id="d817b-112">If an error occurs, this value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d817b-113">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d817b-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d817b-114">Numero di byte di dati da tentare di leggere dall'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="d817b-114">Number of bytes of data to attempt to read from the stream object.</span></span>

</dd> <dt>

<span data-ttu-id="d817b-115">*pcbRead* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d817b-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d817b-116">Indirizzo di una variabile **Long** che riceve il numero effettivo di byte letti dall'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="d817b-116">Address of a **LONG** variable that receives the actual number of bytes read from the stream object.</span></span> <span data-ttu-id="d817b-117">È possibile impostare questo puntatore su **null** per indicare che non si è interessati a questo valore.</span><span class="sxs-lookup"><span data-stu-id="d817b-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="d817b-118">In questo caso, questo metodo non fornisce il numero effettivo di byte letti.</span><span class="sxs-lookup"><span data-stu-id="d817b-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d817b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d817b-119">Return value</span></span>

<span data-ttu-id="d817b-120">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d817b-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="d817b-121">Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="d817b-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d817b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="d817b-122">Remarks</span></span>

<span data-ttu-id="d817b-123">Questo metodo legge i byte da questo oggetto flusso in memoria.</span><span class="sxs-lookup"><span data-stu-id="d817b-123">This method reads bytes from this stream object into memory.</span></span> <span data-ttu-id="d817b-124">L'oggetto flusso deve essere aperto in \_ modalità di lettura STGM.</span><span class="sxs-lookup"><span data-stu-id="d817b-124">The stream object must be opened in STGM\_READ mode.</span></span> <span data-ttu-id="d817b-125">Questo metodo regola il puntatore di ricerca in base al numero effettivo di byte letti.</span><span class="sxs-lookup"><span data-stu-id="d817b-125">This method adjusts the seek pointer by the actual number of bytes read.</span></span>

<span data-ttu-id="d817b-126">Il numero di byte effettivamente letti viene restituito anche nel parametro *pcbRead* .</span><span class="sxs-lookup"><span data-stu-id="d817b-126">The number of bytes actually read is also returned in the *pcbRead* parameter.</span></span>

<span data-ttu-id="d817b-127">Note per i chiamanti</span><span class="sxs-lookup"><span data-stu-id="d817b-127">Notes to Callers</span></span>

<span data-ttu-id="d817b-128">Il numero effettivo di byte letti può essere inferiore al numero di byte richiesti se si verifica un errore o se viene raggiunta la fine del flusso durante l'operazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="d817b-128">The actual number of bytes read can be fewer than the number of bytes requested if an error occurs or if the end of the stream is reached during the read operation.</span></span>

<span data-ttu-id="d817b-129">Alcune implementazioni potrebbero restituire un errore se viene raggiunta la fine del flusso durante la lettura.</span><span class="sxs-lookup"><span data-stu-id="d817b-129">Some implementations might return an error if the end of the stream is reached during the read.</span></span> <span data-ttu-id="d817b-130">È necessario essere pronti a gestire la restituzione dell'errore o i \_ valori restituiti OK alla fine delle letture del flusso.</span><span class="sxs-lookup"><span data-stu-id="d817b-130">You must be prepared to deal with the error return or S\_OK return values on end of stream reads.</span></span>

## <a name="examples"></a><span data-ttu-id="d817b-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="d817b-131">Examples</span></span>

<span data-ttu-id="d817b-132">Nell'esempio seguente viene illustrato come leggere i byte dal buffer.</span><span class="sxs-lookup"><span data-stu-id="d817b-132">The following example shows reading bytes from the buffer.</span></span>


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="d817b-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d817b-133">Requirements</span></span>



| <span data-ttu-id="d817b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d817b-134">Requirement</span></span> | <span data-ttu-id="d817b-135">Valore</span><span class="sxs-lookup"><span data-stu-id="d817b-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d817b-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d817b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d817b-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d817b-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d817b-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d817b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d817b-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d817b-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d817b-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d817b-140">End of client support</span></span><br/>    | <span data-ttu-id="d817b-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d817b-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d817b-142">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="d817b-142">End of server support</span></span><br/>    | <span data-ttu-id="d817b-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d817b-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d817b-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d817b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d817b-145"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d817b-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d817b-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d817b-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="d817b-147"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d817b-147"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d817b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d817b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d817b-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d817b-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d817b-150">IID</span><span class="sxs-lookup"><span data-stu-id="d817b-150">IID</span></span><br/>                      | <span data-ttu-id="d817b-151">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="d817b-151">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

