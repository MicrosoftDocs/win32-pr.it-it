---
title: Messaggio MMIOM_READ (mmsystem. h)
description: Il \_ messaggio di lettura MMIOM viene inviato a una routine di i/O dalla funzione mmioRead per richiedere che un numero specificato di byte venga letto da un file aperto.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- MMIOM_READ messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479373"
---
# <a name="mmiom_read-message"></a><span data-ttu-id="bb01c-104">MMIOM \_ leggere il messaggio</span><span class="sxs-lookup"><span data-stu-id="bb01c-104">MMIOM\_READ message</span></span>

<span data-ttu-id="bb01c-105">Il messaggio di **\_ lettura MMIOM** viene inviato a una routine di i/O dalla funzione [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) per richiedere che un numero specificato di byte venga letto da un file aperto.</span><span class="sxs-lookup"><span data-stu-id="bb01c-105">The **MMIOM\_READ** message is sent to an I/O procedure by the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) function to request that a specified number of bytes be read from an open file.</span></span>


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a><span data-ttu-id="bb01c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb01c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb01c-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span><span class="sxs-lookup"><span data-stu-id="bb01c-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="bb01c-108">Puntatore al buffer da riempire con i dati letti dal file.</span><span class="sxs-lookup"><span data-stu-id="bb01c-108">Pointer to the buffer to be filled with data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="bb01c-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span><span class="sxs-lookup"><span data-stu-id="bb01c-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span></span>
</dt> <dd>

<span data-ttu-id="bb01c-110">Numero di byte da leggere dal file.</span><span class="sxs-lookup"><span data-stu-id="bb01c-110">Number of bytes to read from file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb01c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb01c-111">Return Value</span></span>

<span data-ttu-id="bb01c-112">Restituisce il numero di byte effettivamente letti dal file.</span><span class="sxs-lookup"><span data-stu-id="bb01c-112">Returns the number of bytes actually read from the file.</span></span> <span data-ttu-id="bb01c-113">Se non è possibile leggere altri byte, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="bb01c-113">If no more bytes can be read, the return value is 0.</span></span> <span data-ttu-id="bb01c-114">Se si verifica un errore, il valore restituito è 1.</span><span class="sxs-lookup"><span data-stu-id="bb01c-114">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb01c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb01c-115">Remarks</span></span>

<span data-ttu-id="bb01c-116">La procedura di I/O è responsabile dell'aggiornamento del membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) in modo da riflettere la nuova posizione del file dopo l'operazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="bb01c-116">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the read operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb01c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb01c-117">Requirements</span></span>



| <span data-ttu-id="bb01c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb01c-118">Requirement</span></span> | <span data-ttu-id="bb01c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bb01c-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb01c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb01c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb01c-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb01c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bb01c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb01c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb01c-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb01c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bb01c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb01c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb01c-125"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb01c-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

