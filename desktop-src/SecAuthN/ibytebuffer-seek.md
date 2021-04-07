---
description: Il metodo Seek modifica il puntatore di ricerca in un nuovo percorso relativo all'inizio del buffer, alla fine del buffer o al puntatore di ricerca corrente.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'Metodo IByteBuffer:: Seek (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eacfedc3ed23a7a4cf1f60e6c6ac21936c3c94f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884514"
---
# <a name="ibytebufferseek-method"></a><span data-ttu-id="cf857-103">Metodo IByteBuffer:: Seek</span><span class="sxs-lookup"><span data-stu-id="cf857-103">IByteBuffer::Seek method</span></span>

<span data-ttu-id="cf857-104">\[Il metodo **Seek** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="cf857-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cf857-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cf857-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cf857-106">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="cf857-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="cf857-107">Il metodo **Seek** modifica il puntatore di ricerca in un nuovo percorso relativo all'inizio del buffer, alla fine del buffer o al puntatore di ricerca corrente.</span><span class="sxs-lookup"><span data-stu-id="cf857-107">The **Seek** method changes the seek pointer to a new location relative to the beginning of the buffer, to the end of the buffer, or to the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf857-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf857-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a><span data-ttu-id="cf857-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf857-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf857-110">*dlibMove* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf857-110">*dlibMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf857-111">Spostamento da aggiungere alla posizione indicata da *dwOrigin*.</span><span class="sxs-lookup"><span data-stu-id="cf857-111">Displacement to be added to the location indicated by *dwOrigin*.</span></span> <span data-ttu-id="cf857-112">Se *dwOrigin* è \_ \_ un set di ricerca del flusso, viene interpretato come un valore senza segno anziché con segno.</span><span class="sxs-lookup"><span data-stu-id="cf857-112">If *dwOrigin* is STREAM\_SEEK\_SET, this is interpreted as an unsigned value rather than signed.</span></span>

</dd> <dt>

<span data-ttu-id="cf857-113">*dwOrigin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf857-113">*dwOrigin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf857-114">Specifica l'origine per lo spostamento specificato in *dlibMove*.</span><span class="sxs-lookup"><span data-stu-id="cf857-114">Specifies the origin for the displacement specified in *dlibMove*.</span></span> <span data-ttu-id="cf857-115">L'origine può essere uno dei valori riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="cf857-115">The origin can be one of the values in the following table.</span></span>



| <span data-ttu-id="cf857-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cf857-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="cf857-117">Significato</span><span class="sxs-lookup"><span data-stu-id="cf857-117">Meaning</span></span>                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <span data-ttu-id="cf857-118"><dt>**\_set di ricerca di flusso \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf857-118"><dt>**STREAM\_SEEK\_SET**</dt></span></span> </dl> | <span data-ttu-id="cf857-119">Il nuovo puntatore di ricerca è un offset relativo all'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="cf857-119">The new seek pointer is an offset relative to the beginning of the stream.</span></span> <span data-ttu-id="cf857-120">In questo caso, il parametro *dlibMove* è la nuova posizione di ricerca relativa all'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="cf857-120">In this case, the *dlibMove* parameter is the new seek position relative to the beginning of the stream.</span></span><br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <span data-ttu-id="cf857-121"><dt>**\_cur ricerca \_ flusso**</dt></span><span class="sxs-lookup"><span data-stu-id="cf857-121"><dt>**STREAM\_SEEK\_CUR**</dt></span></span> </dl> | <span data-ttu-id="cf857-122">Il nuovo puntatore di ricerca è un offset relativo alla posizione corrente del puntatore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="cf857-122">The new seek pointer is an offset relative to the current seek pointer location.</span></span> <span data-ttu-id="cf857-123">In questo caso, il parametro *dlibMove* è lo spostamento firmato dalla posizione di ricerca corrente.</span><span class="sxs-lookup"><span data-stu-id="cf857-123">In this case, the *dlibMove* parameter is the signed displacement from the current seek position.</span></span><br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <span data-ttu-id="cf857-124"><dt>**\_fine ricerca \_ flusso**</dt></span><span class="sxs-lookup"><span data-stu-id="cf857-124"><dt>**STREAM\_SEEK\_END**</dt></span></span> </dl> | <span data-ttu-id="cf857-125">Il nuovo puntatore di ricerca è un offset relativo alla fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="cf857-125">The new seek pointer is an offset relative to the end of the stream.</span></span> <span data-ttu-id="cf857-126">In questo caso, il parametro *dlibMove* è la nuova posizione di ricerca relativa alla fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="cf857-126">In this case, the *dlibMove* parameter is the new seek position relative to the end of the stream.</span></span><br/>             |



 

</dd> <dt>

<span data-ttu-id="cf857-127">*plibNewPosition* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf857-127">*plibNewPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf857-128">Puntatore alla posizione in cui questo metodo scrive il valore del nuovo puntatore di ricerca dall'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="cf857-128">Pointer to the location where this method writes the value of the new seek pointer from the beginning of the stream.</span></span> <span data-ttu-id="cf857-129">È possibile impostare questo puntatore su **null** per indicare che non si è interessati a questo valore.</span><span class="sxs-lookup"><span data-stu-id="cf857-129">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="cf857-130">In questo caso, questo metodo non fornisce il nuovo puntatore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="cf857-130">In this case, this method does not provide the new seek pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf857-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf857-131">Return value</span></span>

<span data-ttu-id="cf857-132">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cf857-132">The return value is an **HRESULT**.</span></span> <span data-ttu-id="cf857-133">Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="cf857-133">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf857-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf857-134">Remarks</span></span>

<span data-ttu-id="cf857-135">Il metodo **Seek** modifica il puntatore di ricerca in modo che le operazioni di lettura e scrittura successive possano avvenire in un percorso diverso nell'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="cf857-135">The **Seek** method changes the seek pointer so subsequent read and write operations can take place at a different location in the stream object.</span></span> <span data-ttu-id="cf857-136">Si tratta di un errore di ricerca prima dell'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="cf857-136">It is an error to seek before the beginning of the stream.</span></span> <span data-ttu-id="cf857-137">Non è, tuttavia, un errore di ricerca oltre la fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="cf857-137">It is not, however, an error to seek past the end of the stream.</span></span> <span data-ttu-id="cf857-138">La ricerca oltre la fine del flusso è utile per le successive operazioni di scrittura, poiché il flusso verrà esteso alla posizione di ricerca immediatamente prima del termine dell'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="cf857-138">Seeking past the end of the stream is useful for subsequent write operations, as the stream will at that time be extended to the seek position immediately before the write operation is done.</span></span>

<span data-ttu-id="cf857-139">È anche possibile usare questo metodo per ottenere il valore corrente del puntatore di ricerca chiamando questo metodo con il parametro *dwOrigin* impostato su Stream \_ Seek \_ cur e il parametro *dlibMove* impostato su zero, in modo che il puntatore Seek non venga modificato.</span><span class="sxs-lookup"><span data-stu-id="cf857-139">You can also use this method to obtain the current value of the seek pointer by calling this method with the *dwOrigin* parameter set to STREAM\_SEEK\_CUR and the *dlibMove* parameter set to zero so the seek pointer is not changed.</span></span> <span data-ttu-id="cf857-140">Il puntatore di ricerca corrente viene restituito nel parametro *plibNewPosition* .</span><span class="sxs-lookup"><span data-stu-id="cf857-140">The current seek pointer is returned in the *plibNewPosition* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="cf857-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="cf857-141">Examples</span></span>

<span data-ttu-id="cf857-142">Nell'esempio seguente viene illustrato il posizionamento del puntatore di ricerca in una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="cf857-142">The following example shows positioning the seek pointer to a new location.</span></span>


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
```



## <a name="requirements"></a><span data-ttu-id="cf857-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf857-143">Requirements</span></span>



| <span data-ttu-id="cf857-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf857-144">Requirement</span></span> | <span data-ttu-id="cf857-145">Valore</span><span class="sxs-lookup"><span data-stu-id="cf857-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf857-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf857-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cf857-147">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cf857-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cf857-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf857-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cf857-149">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf857-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf857-150">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="cf857-150">End of client support</span></span><br/>    | <span data-ttu-id="cf857-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cf857-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cf857-152">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="cf857-152">End of server support</span></span><br/>    | <span data-ttu-id="cf857-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf857-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cf857-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf857-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf857-155"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf857-155"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf857-156">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="cf857-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="cf857-157"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cf857-157"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cf857-158">DLL</span><span class="sxs-lookup"><span data-stu-id="cf857-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf857-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf857-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cf857-160">IID</span><span class="sxs-lookup"><span data-stu-id="cf857-160">IID</span></span><br/>                      | <span data-ttu-id="cf857-161">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="cf857-161">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

