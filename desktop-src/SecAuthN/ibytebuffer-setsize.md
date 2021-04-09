---
description: Il metodo sesize modifica la dimensione dell'oggetto flusso.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'Metodo IByteBuffer:: sesize (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968296"
---
# <a name="ibytebuffersetsize-method"></a><span data-ttu-id="fc77a-103">Metodo IByteBuffer:: sesize</span><span class="sxs-lookup"><span data-stu-id="fc77a-103">IByteBuffer::SetSize method</span></span>

<span data-ttu-id="fc77a-104">\[Il metodo **sesize** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="fc77a-104">\[The **SetSize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fc77a-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fc77a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fc77a-106">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="fc77a-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="fc77a-107">Il metodo **sesize** modifica la dimensione dell'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="fc77a-107">The **SetSize** method changes the size of the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc77a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc77a-108">Syntax</span></span>


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a><span data-ttu-id="fc77a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc77a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc77a-110">*libNewSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc77a-110">*libNewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc77a-111">Nuove dimensioni del flusso come numero di byte</span><span class="sxs-lookup"><span data-stu-id="fc77a-111">New size of the stream as a number of bytes</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc77a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc77a-112">Return value</span></span>

<span data-ttu-id="fc77a-113">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fc77a-113">The return value is an **HRESULT**.</span></span> <span data-ttu-id="fc77a-114">Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="fc77a-114">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc77a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc77a-115">Remarks</span></span>

<span data-ttu-id="fc77a-116">Il metodo **IByteBuffer:: sesize** modifica la dimensione dell'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="fc77a-116">The **IByteBuffer::SetSize** method changes the size of the stream object.</span></span> <span data-ttu-id="fc77a-117">Chiamare questo metodo per preallocare lo spazio per il flusso.</span><span class="sxs-lookup"><span data-stu-id="fc77a-117">Call this method to preallocate space for the stream.</span></span> <span data-ttu-id="fc77a-118">Se il parametro *libNewSize* è maggiore della dimensione corrente del flusso, il flusso viene esteso alle dimensioni indicate riempiendo lo spazio corrispondente con i byte di un valore non definito.</span><span class="sxs-lookup"><span data-stu-id="fc77a-118">If the *libNewSize* parameter is larger than the current stream size, the stream is extended to the indicated size by filling the intervening space with bytes of undefined value.</span></span> <span data-ttu-id="fc77a-119">Questa operazione è simile al metodo [**IByteBuffer:: Write**](ibytebuffer-write.md) se il puntatore di ricerca è oltre la fine del flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="fc77a-119">This operation is similar to the [**IByteBuffer::Write**](ibytebuffer-write.md) method if the seek pointer is past the current end-of-stream.</span></span>

<span data-ttu-id="fc77a-120">Se il parametro *libNewSize* è minore del flusso corrente, il flusso viene troncato alla dimensione indicata.</span><span class="sxs-lookup"><span data-stu-id="fc77a-120">If the *libNewSize* parameter is smaller than the current stream, then the stream is truncated to the indicated size.</span></span>

<span data-ttu-id="fc77a-121">Il puntatore di ricerca non è influenzato dalla modifica delle dimensioni del flusso.</span><span class="sxs-lookup"><span data-stu-id="fc77a-121">The seek pointer is not affected by the change in stream size.</span></span>

<span data-ttu-id="fc77a-122">La chiamata di **IByteBuffer:: sesize** può essere un modo efficace per ottenere un grande blocco di spazio contiguo.</span><span class="sxs-lookup"><span data-stu-id="fc77a-122">Calling **IByteBuffer::SetSize** can be an effective way of trying to obtain a large chunk of contiguous space.</span></span>

## <a name="examples"></a><span data-ttu-id="fc77a-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="fc77a-123">Examples</span></span>

<span data-ttu-id="fc77a-124">Nell'esempio seguente viene illustrata l'impostazione delle dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="fc77a-124">The following example shows setting the buffer size.</span></span>


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
```



## <a name="requirements"></a><span data-ttu-id="fc77a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc77a-125">Requirements</span></span>



| <span data-ttu-id="fc77a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc77a-126">Requirement</span></span> | <span data-ttu-id="fc77a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="fc77a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc77a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc77a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fc77a-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fc77a-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fc77a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc77a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fc77a-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc77a-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc77a-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fc77a-132">End of client support</span></span><br/>    | <span data-ttu-id="fc77a-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc77a-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fc77a-134">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="fc77a-134">End of server support</span></span><br/>    | <span data-ttu-id="fc77a-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fc77a-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fc77a-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc77a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc77a-137"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc77a-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc77a-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fc77a-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="fc77a-139"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fc77a-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fc77a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="fc77a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc77a-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc77a-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fc77a-142">IID</span><span class="sxs-lookup"><span data-stu-id="fc77a-142">IID</span></span><br/>                      | <span data-ttu-id="fc77a-143">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="fc77a-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

