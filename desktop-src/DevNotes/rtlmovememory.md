---
description: Copia il contenuto di un blocco di memoria di origine in un blocco di memoria di destinazione e supporta i blocchi di memoria di origine e di destinazione sovrapposti.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Funzione RtlMoveMemory (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304655"
---
# <a name="rtlmovememory-function"></a><span data-ttu-id="7be16-103">RtlMoveMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="7be16-103">RtlMoveMemory function</span></span>

<span data-ttu-id="7be16-104">Copia il contenuto di un blocco di memoria di origine in un blocco di memoria di destinazione e supporta i blocchi di memoria di origine e di destinazione sovrapposti.</span><span class="sxs-lookup"><span data-stu-id="7be16-104">Copies the contents of a source memory block to a destination memory block, and supports overlapping source and destination memory blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be16-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7be16-105">Syntax</span></span>


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a><span data-ttu-id="7be16-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7be16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be16-107">*Destinazione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7be16-107">*Destination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7be16-108">Puntatore al blocco di memoria di destinazione in cui copiare i byte.</span><span class="sxs-lookup"><span data-stu-id="7be16-108">A pointer to the destination memory block to copy the bytes to.</span></span>

</dd> <dt>

<span data-ttu-id="7be16-109">*Origine* \[ dati in\]</span><span class="sxs-lookup"><span data-stu-id="7be16-109">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be16-110">Puntatore al blocco di memoria di origine da cui copiare i byte.</span><span class="sxs-lookup"><span data-stu-id="7be16-110">A pointer to the source memory block to copy the bytes from.</span></span>

</dd> <dt>

<span data-ttu-id="7be16-111">*Lunghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7be16-111">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be16-112">Numero di byte da copiare dall'origine alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="7be16-112">The number of bytes to copy from the source to the destination.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be16-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7be16-113">Return value</span></span>

<span data-ttu-id="7be16-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="7be16-114">None</span></span>

## <a name="remarks"></a><span data-ttu-id="7be16-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="7be16-115">Remarks</span></span>

<span data-ttu-id="7be16-116">Il blocco di memoria di origine, definito dall' *origine* e dalla *lunghezza*, può sovrapporsi al blocco di memoria di destinazione, definito in base a *destinazione* e *lunghezza*.</span><span class="sxs-lookup"><span data-stu-id="7be16-116">The source memory block, which is defined by *Source* and *Length*, can overlap the destination memory block, which is defined by *Destination* and *Length*.</span></span>

<span data-ttu-id="7be16-117">La routine [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) viene eseguita più velocemente di **RtlMoveMemory**, ma **RtlCopyMemory** richiede che i blocchi di memoria di origine e di destinazione non si sovrappongano.</span><span class="sxs-lookup"><span data-stu-id="7be16-117">The [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) routine runs faster than **RtlMoveMemory**, but **RtlCopyMemory** requires that the source and destination memory blocks do not overlap.</span></span>

<span data-ttu-id="7be16-118">I chiamanti di **RtlMoveMemory** possono essere in esecuzione in qualsiasi livello IRQL se i blocchi di memoria di origine e di destinazione si trovano in memoria di sistema non di paging.</span><span class="sxs-lookup"><span data-stu-id="7be16-118">Callers of **RtlMoveMemory** can be running at any IRQL if the source and destination memory blocks are in nonpaged system memory.</span></span> <span data-ttu-id="7be16-119">In caso contrario, il chiamante deve essere in esecuzione a livello IRQL <= \_ livello APC.</span><span class="sxs-lookup"><span data-stu-id="7be16-119">Otherwise, the caller must be running at IRQL <= APC\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7be16-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7be16-120">Requirements</span></span>



| <span data-ttu-id="7be16-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7be16-121">Requirement</span></span> | <span data-ttu-id="7be16-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7be16-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be16-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7be16-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7be16-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7be16-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="7be16-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7be16-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7be16-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7be16-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="7be16-127">Piattaforma di destinazione</span><span class="sxs-lookup"><span data-stu-id="7be16-127">Target platform</span></span><br/>          | <dl> <span data-ttu-id="7be16-128"><dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="7be16-128"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="7be16-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7be16-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7be16-130"><dt>WDM. h (include WDM. h, ntddk. h o Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7be16-130"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="7be16-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="7be16-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="7be16-132"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7be16-132"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7be16-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7be16-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7be16-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7be16-134"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="7be16-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7be16-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be16-136">**RtlCopyMemory**</span><span class="sxs-lookup"><span data-stu-id="7be16-136">**RtlCopyMemory**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
