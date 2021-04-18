---
description: Il metodo commit garantisce che tutte le modifiche apportate a un oggetto aperto in modalità transazionale vengano riflesse nell'archivio padre.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'Metodo IByteBuffer:: commit (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 066925361d0ee4391bcd1eaafe33e0ae2d4b9120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315881"
---
# <a name="ibytebuffercommit-method"></a><span data-ttu-id="d144c-103">Metodo IByteBuffer:: commit</span><span class="sxs-lookup"><span data-stu-id="d144c-103">IByteBuffer::Commit method</span></span>

<span data-ttu-id="d144c-104">\[Il metodo **commit** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d144c-104">\[The **Commit** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d144c-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d144c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d144c-106">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="d144c-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="d144c-107">Il metodo **commit** garantisce che tutte le modifiche apportate a un oggetto aperto in modalità transazionale vengano riflesse nell'archivio padre.</span><span class="sxs-lookup"><span data-stu-id="d144c-107">The **Commit** method ensures that any changes made to an object open in transacted mode are reflected in the parent storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="d144c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d144c-108">Syntax</span></span>


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d144c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d144c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d144c-110">*grfCommitFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d144c-110">*grfCommitFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d144c-111">Controlla la modalità di esecuzione del commit delle modifiche dell'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="d144c-111">Controls how the changes for the stream object are committed.</span></span> <span data-ttu-id="d144c-112">Per una definizione di questi valori, vedere l'enumerazione STGC.</span><span class="sxs-lookup"><span data-stu-id="d144c-112">For a definition of these values, see the STGC enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d144c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d144c-113">Return value</span></span>

<span data-ttu-id="d144c-114">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d144c-114">The return value is an **HRESULT**.</span></span> <span data-ttu-id="d144c-115">Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="d144c-115">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d144c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d144c-116">Remarks</span></span>

<span data-ttu-id="d144c-117">Questo metodo garantisce che le modifiche apportate a un oggetto flusso aperto in modalità transazionale siano riflesse nell'archivio padre.</span><span class="sxs-lookup"><span data-stu-id="d144c-117">This method ensures that changes to a stream object opened in transacted mode are reflected in the parent storage.</span></span> <span data-ttu-id="d144c-118">Le modifiche apportate al flusso dopo l'apertura o l'ultimo commit vengono riflesse nell'oggetto di archiviazione padre.</span><span class="sxs-lookup"><span data-stu-id="d144c-118">Changes that have been made to the stream since it was opened or last committed are reflected to the parent storage object.</span></span> <span data-ttu-id="d144c-119">Se l'elemento padre viene aperto in modalità transazionale, l'elemento padre può comunque ripristinare in un secondo momento il rollback delle modifiche apportate a questo oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="d144c-119">If the parent is opened in transacted mode, the parent may still revert at a later time rolling back the changes to this stream object.</span></span> <span data-ttu-id="d144c-120">L'implementazione del file composto non supporta l'apertura di flussi in modalità transazionale, quindi questo metodo ha un effetto molto ridotto oltre a scaricare i buffer di memoria.</span><span class="sxs-lookup"><span data-stu-id="d144c-120">The compound file implementation does not support opening streams in transacted mode, so this method has very little effect other than to flush memory buffers.</span></span>

## <a name="examples"></a><span data-ttu-id="d144c-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="d144c-121">Examples</span></span>

<span data-ttu-id="d144c-122">Nell'esempio seguente viene illustrato il commit delle modifiche nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="d144c-122">The following example shows committing changes to storage.</span></span>


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
```



## <a name="requirements"></a><span data-ttu-id="d144c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d144c-123">Requirements</span></span>



| <span data-ttu-id="d144c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d144c-124">Requirement</span></span> | <span data-ttu-id="d144c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d144c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d144c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d144c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d144c-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d144c-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d144c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d144c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d144c-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d144c-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d144c-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d144c-130">End of client support</span></span><br/>    | <span data-ttu-id="d144c-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d144c-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d144c-132">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="d144c-132">End of server support</span></span><br/>    | <span data-ttu-id="d144c-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d144c-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d144c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d144c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d144c-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d144c-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d144c-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d144c-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="d144c-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d144c-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d144c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d144c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d144c-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d144c-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d144c-140">IID</span><span class="sxs-lookup"><span data-stu-id="d144c-140">IID</span></span><br/>                      | <span data-ttu-id="d144c-141">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="d144c-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

