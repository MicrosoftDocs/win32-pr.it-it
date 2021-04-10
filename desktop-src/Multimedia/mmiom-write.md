---
title: Messaggio MMIOM_WRITE (mmsystem. h)
description: Il \_ messaggio di scrittura MMIOM viene inviato a una routine di i/O dalla funzione mmioWrite per richiedere che i dati vengano scritti in un file aperto.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- MMIOM_WRITE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964837"
---
# <a name="mmiom_write-message"></a><span data-ttu-id="d4211-104">MMIOM \_ Scrivi messaggio</span><span class="sxs-lookup"><span data-stu-id="d4211-104">MMIOM\_WRITE message</span></span>

<span data-ttu-id="d4211-105">Il messaggio di **\_ scrittura MMIOM** viene inviato a una routine di i/O dalla funzione [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) per richiedere che i dati vengano scritti in un file aperto.</span><span class="sxs-lookup"><span data-stu-id="d4211-105">The **MMIOM\_WRITE** message is sent to an I/O procedure by the [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) function to request that data be written to an open file.</span></span>


```C++
MMIOM_WRITE 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a><span data-ttu-id="d4211-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4211-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4211-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span><span class="sxs-lookup"><span data-stu-id="d4211-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="d4211-108">Puntatore a un buffer contenente i dati da scrivere nel file.</span><span class="sxs-lookup"><span data-stu-id="d4211-108">Pointer to a buffer containing the data to write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="d4211-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span><span class="sxs-lookup"><span data-stu-id="d4211-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span></span>
</dt> <dd>

<span data-ttu-id="d4211-110">Numero di byte da scrivere nel file.</span><span class="sxs-lookup"><span data-stu-id="d4211-110">Number of bytes to write to file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4211-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4211-111">Return Value</span></span>

<span data-ttu-id="d4211-112">Restituisce il numero di byte effettivamente scritti nel file.</span><span class="sxs-lookup"><span data-stu-id="d4211-112">Returns the number of bytes actually written to the file.</span></span> <span data-ttu-id="d4211-113">Se si verifica un errore, il valore restituito è 1.</span><span class="sxs-lookup"><span data-stu-id="d4211-113">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4211-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4211-114">Remarks</span></span>

<span data-ttu-id="d4211-115">La procedura di I/O è responsabile dell'aggiornamento del membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) in modo da riflettere la nuova posizione del file dopo l'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="d4211-115">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the write operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4211-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4211-116">Requirements</span></span>



| <span data-ttu-id="d4211-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4211-117">Requirement</span></span> | <span data-ttu-id="d4211-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d4211-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4211-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4211-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4211-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d4211-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d4211-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4211-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4211-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d4211-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d4211-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4211-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4211-124"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4211-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

