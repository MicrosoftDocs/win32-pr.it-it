---
title: Messaggio MMIOM_SEEK (mmsystem. h)
description: Il \_ messaggio MMIOM Seek viene inviato a una routine di i/O dalla funzione mmioSeek per richiedere che la posizione corrente del file venga spostata.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- MMIOM_SEEK messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302504"
---
# <a name="mmiom_seek-message"></a><span data-ttu-id="aa72c-104">\_Messaggio MMIOM seek</span><span class="sxs-lookup"><span data-stu-id="aa72c-104">MMIOM\_SEEK message</span></span>

<span data-ttu-id="aa72c-105">Il messaggio **MMIOM \_ Seek** viene inviato a una routine di i/O dalla funzione [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) per richiedere che la posizione corrente del file venga spostata.</span><span class="sxs-lookup"><span data-stu-id="aa72c-105">The **MMIOM\_SEEK** message is sent to an I/O procedure by the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function to request that the current file position be moved.</span></span>


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a><span data-ttu-id="aa72c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa72c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa72c-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span><span class="sxs-lookup"><span data-stu-id="aa72c-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="aa72c-108">Nuova posizione del file.</span><span class="sxs-lookup"><span data-stu-id="aa72c-108">New file position.</span></span> <span data-ttu-id="aa72c-109">Il significato di questo valore dipende dal flag specificato in **lChangeFlag**.</span><span class="sxs-lookup"><span data-stu-id="aa72c-109">The meaning of this value is dependent on the flag specified in **lChangeFlag**.</span></span>

</dd> <dt>

<span data-ttu-id="aa72c-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span><span class="sxs-lookup"><span data-stu-id="aa72c-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span></span>
</dt> <dd>

<span data-ttu-id="aa72c-111">Flag che specifica la modalità di modifica della posizione del file.</span><span class="sxs-lookup"><span data-stu-id="aa72c-111">Flag specifying how the file position is changed.</span></span> <span data-ttu-id="aa72c-112">Vengono definiti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa72c-112">The following values are defined:</span></span>



| <span data-ttu-id="aa72c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa72c-113">Requirement</span></span> | <span data-ttu-id="aa72c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="aa72c-114">Value</span></span> |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa72c-115">Cerca \_ cur</span><span class="sxs-lookup"><span data-stu-id="aa72c-115">SEEK\_CUR</span></span> | <span data-ttu-id="aa72c-116">Spostare la posizione del file in *lNewFilePos* byte dalla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="aa72c-116">Move the file position to be *lNewFilePos* bytes from the current position.</span></span> <span data-ttu-id="aa72c-117">*lNewFilePos* può essere positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="aa72c-117">*lNewFilePos* can be positive or negative.</span></span> |
| <span data-ttu-id="aa72c-118">\_fine ricerca</span><span class="sxs-lookup"><span data-stu-id="aa72c-118">SEEK\_END</span></span> | <span data-ttu-id="aa72c-119">Spostare la posizione del file in *lNewFilePos* byte dalla fine del file.</span><span class="sxs-lookup"><span data-stu-id="aa72c-119">Move the file position to be *lNewFilePos* bytes from the end of the file.</span></span>                                             |
| <span data-ttu-id="aa72c-120">SET di ricerca \_</span><span class="sxs-lookup"><span data-stu-id="aa72c-120">SEEK\_SET</span></span> | <span data-ttu-id="aa72c-121">Spostare la posizione del file in *lNewFilePos* i byte dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="aa72c-121">Move the file position to be *lNewFilePos* bytes from the beginning of the file.</span></span>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa72c-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa72c-122">Return Value</span></span>

<span data-ttu-id="aa72c-123">Restituisce la nuova posizione del file.</span><span class="sxs-lookup"><span data-stu-id="aa72c-123">Returns the new file position.</span></span> <span data-ttu-id="aa72c-124">Se si verifica un errore, il valore restituito è 1.</span><span class="sxs-lookup"><span data-stu-id="aa72c-124">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa72c-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa72c-125">Remarks</span></span>

<span data-ttu-id="aa72c-126">La procedura di I/O è responsabile della gestione della posizione corrente del file nel membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="aa72c-126">The I/O procedure is responsible for maintaining the current file position in the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa72c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa72c-127">Requirements</span></span>



| <span data-ttu-id="aa72c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa72c-128">Requirement</span></span> | <span data-ttu-id="aa72c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="aa72c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa72c-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa72c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aa72c-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa72c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aa72c-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa72c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aa72c-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa72c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aa72c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa72c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa72c-135"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa72c-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

