---
title: Messaggio MMIOM_OPEN (mmsystem. h)
description: Il \_ messaggio aperto MMIOM viene inviato a una routine di i/O dalla funzione mmioOpen per richiedere l'apertura o l'eliminazione di un file.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- MMIOM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302770"
---
# <a name="mmiom_open-message"></a><span data-ttu-id="bad5a-104">MMIOM \_ messaggio aperto</span><span class="sxs-lookup"><span data-stu-id="bad5a-104">MMIOM\_OPEN message</span></span>

<span data-ttu-id="bad5a-105">Il **messaggio \_ aperto MMIOM** viene inviato a una routine di i/O dalla funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) per richiedere l'apertura o l'eliminazione di un file.</span><span class="sxs-lookup"><span data-stu-id="bad5a-105">The **MMIOM\_OPEN** message is sent to an I/O procedure by the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to request that a file be opened or deleted.</span></span>


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="bad5a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bad5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bad5a-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span><span class="sxs-lookup"><span data-stu-id="bad5a-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span></span>
</dt> <dd>

<span data-ttu-id="bad5a-108">Stringa con terminazione null che contiene il nome del file da aprire.</span><span class="sxs-lookup"><span data-stu-id="bad5a-108">Null-terminated string containing the name of the file to open.</span></span>

</dd> <dt>

<span data-ttu-id="bad5a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="bad5a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="bad5a-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="bad5a-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bad5a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bad5a-111">Return Value</span></span>

<span data-ttu-id="bad5a-112">Restituisce MMSYSERR \_ NOERROR se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bad5a-112">Returns MMSYSERR\_NOERROR if successful or an error otherwise.</span></span> <span data-ttu-id="bad5a-113">Di seguito sono riportati i possibili valori di errore:</span><span class="sxs-lookup"><span data-stu-id="bad5a-113">Possible error values include the following:</span></span>



| <span data-ttu-id="bad5a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad5a-114">Requirement</span></span> | <span data-ttu-id="bad5a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bad5a-115">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="bad5a-116">\_CANNOTOPEN MMIOM</span><span class="sxs-lookup"><span data-stu-id="bad5a-116">MMIOM\_CANNOTOPEN</span></span>  | <span data-ttu-id="bad5a-117">Non è stato possibile aprire il file.</span><span class="sxs-lookup"><span data-stu-id="bad5a-117">The file could not be opened.</span></span>               |
| <span data-ttu-id="bad5a-118">\_OutOfMemory MMIOM</span><span class="sxs-lookup"><span data-stu-id="bad5a-118">MMIOM\_OUTOFMEMORY</span></span> | <span data-ttu-id="bad5a-119">Memoria insufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bad5a-119">Not enough memory to perform the operation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bad5a-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="bad5a-120">Remarks</span></span>

<span data-ttu-id="bad5a-121">Il membro **dwFlags** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) contiene i flag passati alla funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="bad5a-121">The **dwFlags** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure contains flags passed to the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span>

<span data-ttu-id="bad5a-122">Il membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) è inizializzato su zero.</span><span class="sxs-lookup"><span data-stu-id="bad5a-122">The **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure is initialized to zero.</span></span> <span data-ttu-id="bad5a-123">Se questo valore non è corretto, è necessario che la procedura di I/O venga corretta.</span><span class="sxs-lookup"><span data-stu-id="bad5a-123">If this value is incorrect, the I/O procedure must correct it.</span></span>

<span data-ttu-id="bad5a-124">Se l'applicazione ha passato una struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) a [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), il valore restituito viene restituito nel membro **wErrorRet** .</span><span class="sxs-lookup"><span data-stu-id="bad5a-124">If the application passed an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), the return value is returned in the **wErrorRet** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad5a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bad5a-125">Requirements</span></span>



| <span data-ttu-id="bad5a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad5a-126">Requirement</span></span> | <span data-ttu-id="bad5a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="bad5a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bad5a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bad5a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bad5a-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bad5a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bad5a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bad5a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bad5a-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bad5a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bad5a-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bad5a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bad5a-133"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bad5a-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

