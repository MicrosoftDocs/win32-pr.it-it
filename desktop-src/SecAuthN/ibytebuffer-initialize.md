---
description: Il metodo Initialize prepara l'oggetto IByteBuffer per l'utilizzo. Questo metodo deve essere chiamato prima di chiamare altri metodi nell'interfaccia IByteBuffer.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'Metodo IByteBuffer:: Initialize (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 245f9282174ddeef66b130597f0f20ddf21ededc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317080"
---
# <a name="ibytebufferinitialize-method"></a><span data-ttu-id="dba37-104">Metodo IByteBuffer:: Initialize</span><span class="sxs-lookup"><span data-stu-id="dba37-104">IByteBuffer::Initialize method</span></span>

<span data-ttu-id="dba37-105">\[Il metodo **Initialize** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="dba37-105">\[The **Initialize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dba37-106">Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="dba37-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later.</span></span> <span data-ttu-id="dba37-107">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="dba37-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="dba37-108">Il metodo **Initialize** prepara l'oggetto [**IByteBuffer**](ibytebuffer.md) per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="dba37-108">The **Initialize** method prepares the [**IByteBuffer**](ibytebuffer.md) object for use.</span></span> <span data-ttu-id="dba37-109">Questo metodo deve essere chiamato prima di chiamare altri metodi nell'interfaccia **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="dba37-109">This method must be called prior to calling any other methods in the **IByteBuffer** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="dba37-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dba37-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a><span data-ttu-id="dba37-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="dba37-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dba37-112">*lSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dba37-112">*lSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba37-113">Dimensioni iniziali, in byte, dei dati che devono essere contenuti nel flusso.</span><span class="sxs-lookup"><span data-stu-id="dba37-113">Initial size, in bytes, of the data the stream is to contain.</span></span>

</dd> <dt>

<span data-ttu-id="dba37-114">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dba37-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba37-115">Se non è **null**, i dati iniziali da scrivere nel flusso.</span><span class="sxs-lookup"><span data-stu-id="dba37-115">If not **NULL**, the initial data to write to the stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dba37-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dba37-116">Return value</span></span>

<span data-ttu-id="dba37-117">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dba37-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="dba37-118">Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="dba37-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="dba37-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="dba37-119">Remarks</span></span>

<span data-ttu-id="dba37-120">Quando si usa un nuovo flusso [**IByteBuffer**](ibytebuffer.md) , chiamare questo metodo prima di usare uno degli altri metodi **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="dba37-120">When using a new [**IByteBuffer**](ibytebuffer.md) stream, call this method prior to using any of the other **IByteBuffer** methods.</span></span>

## <a name="examples"></a><span data-ttu-id="dba37-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="dba37-121">Examples</span></span>

<span data-ttu-id="dba37-122">Nell'esempio seguente viene illustrato come inizializzare l'oggetto [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="dba37-122">The following example shows initializing the [**IByteBuffer**](ibytebuffer.md) object.</span></span>


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
```



## <a name="requirements"></a><span data-ttu-id="dba37-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dba37-123">Requirements</span></span>



| <span data-ttu-id="dba37-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dba37-124">Requirement</span></span> | <span data-ttu-id="dba37-125">Valore</span><span class="sxs-lookup"><span data-stu-id="dba37-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dba37-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dba37-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dba37-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dba37-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dba37-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dba37-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dba37-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dba37-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dba37-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="dba37-130">End of client support</span></span><br/>    | <span data-ttu-id="dba37-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dba37-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dba37-132">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="dba37-132">End of server support</span></span><br/>    | <span data-ttu-id="dba37-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dba37-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dba37-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dba37-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dba37-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dba37-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dba37-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="dba37-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="dba37-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dba37-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dba37-138">DLL</span><span class="sxs-lookup"><span data-stu-id="dba37-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dba37-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dba37-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dba37-140">IID</span><span class="sxs-lookup"><span data-stu-id="dba37-140">IID</span></span><br/>                      | <span data-ttu-id="dba37-141">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="dba37-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

