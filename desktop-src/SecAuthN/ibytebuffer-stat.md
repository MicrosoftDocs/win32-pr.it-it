---
description: Il metodo stat recupera le informazioni statistiche dall'oggetto flusso.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'Metodo IByteBuffer:: stat (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317078"
---
# <a name="ibytebufferstat-method"></a><span data-ttu-id="a9482-103">Metodo IByteBuffer:: stat</span><span class="sxs-lookup"><span data-stu-id="a9482-103">IByteBuffer::Stat method</span></span>

<span data-ttu-id="a9482-104">\[Il metodo **Stat** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a9482-104">\[The **Stat** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a9482-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a9482-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a9482-106">L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a9482-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="a9482-107">Il metodo **Stat** recupera le informazioni statistiche dall'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="a9482-107">The **Stat** method retrieves statistical information from the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9482-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9482-108">Syntax</span></span>


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a><span data-ttu-id="a9482-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9482-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9482-110">*pstatstg* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a9482-110">*pstatstg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9482-111">Punta a una struttura **STATSTRUCT** in cui questo metodo inserisce informazioni su questo oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="a9482-111">Points to a **STATSTRUCT** structure where this method places information about this stream object.</span></span> <span data-ttu-id="a9482-112">Questo puntatore è **null** se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="a9482-112">This pointer is **NULL** if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="a9482-113">*grfStatFlag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9482-113">*grfStatFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9482-114">Specifica che questo metodo non restituisce alcuni dei campi nella struttura **STATSTRUCT** , salvando così un'operazione di allocazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="a9482-114">Specifies that this method does not return some of the fields in the **STATSTRUCT** structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="a9482-115">I valori vengono ricavati dall'enumerazione [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag)</span><span class="sxs-lookup"><span data-stu-id="a9482-115">Values are taken from the [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag) enumeration</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9482-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9482-116">Return value</span></span>

<span data-ttu-id="a9482-117">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a9482-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="a9482-118">Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="a9482-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9482-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9482-119">Remarks</span></span>

<span data-ttu-id="a9482-120">Il metodo **IByteBuffer:: stat** recupera un puntatore alla struttura **STATSTRUCT** che contiene informazioni su questo flusso aperto.</span><span class="sxs-lookup"><span data-stu-id="a9482-120">The **IByteBuffer::Stat** method retrieves a pointer to the **STATSTRUCT** structure that contains information about this open stream.</span></span>

## <a name="examples"></a><span data-ttu-id="a9482-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="a9482-121">Examples</span></span>

<span data-ttu-id="a9482-122">Nell'esempio seguente viene illustrato come recuperare informazioni statistiche dal flusso.</span><span class="sxs-lookup"><span data-stu-id="a9482-122">The following example shows retrieving statistical information from the stream.</span></span>


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
```



## <a name="requirements"></a><span data-ttu-id="a9482-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9482-123">Requirements</span></span>



| <span data-ttu-id="a9482-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9482-124">Requirement</span></span> | <span data-ttu-id="a9482-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a9482-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9482-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9482-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a9482-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a9482-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a9482-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9482-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a9482-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a9482-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9482-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a9482-130">End of client support</span></span><br/>    | <span data-ttu-id="a9482-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a9482-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a9482-132">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a9482-132">End of server support</span></span><br/>    | <span data-ttu-id="a9482-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9482-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a9482-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9482-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9482-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9482-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9482-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a9482-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="a9482-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a9482-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a9482-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a9482-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9482-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9482-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a9482-140">IID</span><span class="sxs-lookup"><span data-stu-id="a9482-140">IID</span></span><br/>                      | <span data-ttu-id="a9482-141">IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="a9482-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

