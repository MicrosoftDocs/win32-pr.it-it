---
description: Il metodo Clone crea un nuovo oggetto con il proprio puntatore di ricerca che fa riferimento agli stessi byte dell'oggetto IByteBuffer originale.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'Metodo IByteBuffer:: Clone (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232838"
---
# <a name="ibytebufferclone-method"></a><span data-ttu-id="6a938-103">Metodo IByteBuffer:: Clone</span><span class="sxs-lookup"><span data-stu-id="6a938-103">IByteBuffer::Clone method</span></span>

<span data-ttu-id="6a938-104">\[Il metodo **Clone** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="6a938-104">\[The **Clone** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6a938-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6a938-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6a938-106">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="6a938-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="6a938-107">Il metodo **Clone** crea un nuovo oggetto con il proprio puntatore di ricerca che fa riferimento agli stessi byte dell'oggetto [**IByteBuffer**](ibytebuffer.md) originale.</span><span class="sxs-lookup"><span data-stu-id="6a938-107">The **Clone** method creates a new object with its own seek pointer that references the same bytes as the original [**IByteBuffer**](ibytebuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a938-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a938-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="6a938-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a938-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a938-110">*ppByteBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6a938-110">*ppByteBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a938-111">Quando ha esito positivo, punta alla posizione di un puntatore [**IByteBuffer**](ibytebuffer.md) al nuovo oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="6a938-111">When successful, points to the location of an [**IByteBuffer**](ibytebuffer.md) pointer to the new stream object.</span></span> <span data-ttu-id="6a938-112">Al termine dell'uso del puntatore **IByteBuffer** , rilasciarlo chiamando la funzione [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="6a938-112">When you have finished using the **IByteBuffer** pointer, release it by calling the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) function.</span></span> <span data-ttu-id="6a938-113">Se si verifica un errore, questo parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="6a938-113">If an error occurs, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a938-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a938-114">Return value</span></span>

<span data-ttu-id="6a938-115">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6a938-115">The return value is an **HRESULT**.</span></span> <span data-ttu-id="6a938-116">Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="6a938-116">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a938-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a938-117">Remarks</span></span>

<span data-ttu-id="6a938-118">Questo metodo crea un nuovo oggetto flusso per accedere agli stessi byte ma utilizzando un puntatore di ricerca separato.</span><span class="sxs-lookup"><span data-stu-id="6a938-118">This method creates a new stream object for accessing the same bytes but using a separate seek pointer.</span></span> <span data-ttu-id="6a938-119">Il nuovo oggetto flusso Visualizza gli stessi dati dell'oggetto flusso di origine.</span><span class="sxs-lookup"><span data-stu-id="6a938-119">The new stream object sees the same data as the source stream object.</span></span> <span data-ttu-id="6a938-120">Le modifiche scritte in un oggetto sono immediatamente visibili nell'altra.</span><span class="sxs-lookup"><span data-stu-id="6a938-120">Changes written to one object are immediately visible in the other.</span></span> <span data-ttu-id="6a938-121">Il blocco di intervallo è condiviso tra gli oggetti flusso.</span><span class="sxs-lookup"><span data-stu-id="6a938-121">Range locking is shared between the stream objects.</span></span>

<span data-ttu-id="6a938-122">L'impostazione iniziale del puntatore di ricerca nell'istanza del flusso clonato è uguale all'impostazione corrente del puntatore di ricerca nel flusso originale al momento dell'operazione di clonazione.</span><span class="sxs-lookup"><span data-stu-id="6a938-122">The initial setting of the seek pointer in the cloned stream instance is the same as the current setting of the seek pointer in the original stream at the time of the clone operation.</span></span>

## <a name="examples"></a><span data-ttu-id="6a938-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="6a938-123">Examples</span></span>

<span data-ttu-id="6a938-124">Nell'esempio seguente viene illustrata la clonazione dell'interfaccia [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6a938-124">The following example shows cloning the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
```



## <a name="requirements"></a><span data-ttu-id="6a938-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a938-125">Requirements</span></span>



| <span data-ttu-id="6a938-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a938-126">Requirement</span></span> | <span data-ttu-id="6a938-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6a938-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a938-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a938-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6a938-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6a938-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6a938-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a938-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6a938-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6a938-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a938-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6a938-132">End of client support</span></span><br/>    | <span data-ttu-id="6a938-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6a938-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6a938-134">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6a938-134">End of server support</span></span><br/>    | <span data-ttu-id="6a938-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a938-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6a938-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a938-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a938-137"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a938-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a938-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6a938-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a938-139"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6a938-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6a938-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6a938-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a938-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a938-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6a938-142">IID</span><span class="sxs-lookup"><span data-stu-id="6a938-142">IID</span></span><br/>                      | <span data-ttu-id="6a938-143">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="6a938-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

