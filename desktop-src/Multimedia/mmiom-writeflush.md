---
title: Messaggio MMIOM_WRITEFLUSH (mmsystem. h)
description: Il \_ messaggio MMIOM WRITEFLUSH viene inviato a una routine di i/o dalla funzione mmioWrite per richiedere che i dati vengano scritti in un file aperto e che i buffer interni utilizzati dalla procedura di i/o vengano scaricati su disco.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- MMIOM_WRITEFLUSH messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_WRITEFLUSH
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b294d4c461970a3304f09088cf63a6564acd50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743359"
---
# <a name="mmiom_writeflush-message"></a><span data-ttu-id="4b306-104">\_Messaggio MMIOM WRITEFLUSH</span><span class="sxs-lookup"><span data-stu-id="4b306-104">MMIOM\_WRITEFLUSH message</span></span>

<span data-ttu-id="4b306-105">Il messaggio **MMIOM \_ WRITEFLUSH** viene inviato a una routine di i/o dalla funzione [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) per richiedere che i dati vengano scritti in un file aperto e che i buffer interni utilizzati dalla procedura di i/o vengano scaricati su disco.</span><span class="sxs-lookup"><span data-stu-id="4b306-105">The **MMIOM\_WRITEFLUSH** message is sent to an I/O procedure by the [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) function to request that data be written to an open file and that any internal buffers used by the I/O procedure be flushed to disk.</span></span>


```C++
MMIOM_WRITEFLUSH 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a><span data-ttu-id="4b306-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b306-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b306-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span><span class="sxs-lookup"><span data-stu-id="4b306-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="4b306-108">Puntatore a un buffer contenente i dati da scrivere nel file.</span><span class="sxs-lookup"><span data-stu-id="4b306-108">Pointer to a buffer containing the data to write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="4b306-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span><span class="sxs-lookup"><span data-stu-id="4b306-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span></span>
</dt> <dd>

<span data-ttu-id="4b306-110">Numero di byte da scrivere nel file.</span><span class="sxs-lookup"><span data-stu-id="4b306-110">Number of bytes to write to file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b306-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b306-111">Return Value</span></span>

<span data-ttu-id="4b306-112">Restituisce il numero di byte effettivamente scritti nel file.</span><span class="sxs-lookup"><span data-stu-id="4b306-112">Returns the number of bytes actually written to the file.</span></span> <span data-ttu-id="4b306-113">Se si verifica un errore, il valore restituito è 1.</span><span class="sxs-lookup"><span data-stu-id="4b306-113">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b306-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b306-114">Remarks</span></span>

<span data-ttu-id="4b306-115">La procedura di I/O è responsabile dell'aggiornamento del membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) in modo da riflettere la nuova posizione del file dopo l'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="4b306-115">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the write operation.</span></span>

<span data-ttu-id="4b306-116">Questo messaggio è equivalente al messaggio [**di \_ scrittura MMIOM**](mmiom-write.md) con la differenza che richiede che la procedura di i/O scarichi i buffer interni, se presenti.</span><span class="sxs-lookup"><span data-stu-id="4b306-116">This message is equivalent to the [**MMIOM\_WRITE**](mmiom-write.md) message except that it requests that the I/O procedure flush its internal buffers, if any.</span></span> <span data-ttu-id="4b306-117">A meno che una routine di I/O esegua il buffering interno, questo messaggio può essere gestito esattamente come il messaggio di **\_ scrittura MMIOM** .</span><span class="sxs-lookup"><span data-stu-id="4b306-117">Unless an I/O procedure performs internal buffering, this message can be handled exactly like the **MMIOM\_WRITE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b306-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b306-118">Requirements</span></span>



| <span data-ttu-id="4b306-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b306-119">Requirement</span></span> | <span data-ttu-id="4b306-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4b306-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b306-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b306-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4b306-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b306-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4b306-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b306-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4b306-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b306-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4b306-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b306-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b306-126"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b306-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

