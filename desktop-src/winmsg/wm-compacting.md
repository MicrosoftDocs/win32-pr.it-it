---
description: Inviato a tutte le finestre di primo livello quando il sistema rileva più del 12,5% del tempo di sistema in un intervallo da 30 a 60 secondi viene impiegato per la compattazione della memoria. Indica che la memoria di sistema è insufficiente.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: Messaggio WM_COMPACTING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314872"
---
# <a name="wm_compacting-message"></a><span data-ttu-id="70e15-104">\_Messaggio di compattazione WM</span><span class="sxs-lookup"><span data-stu-id="70e15-104">WM\_COMPACTING message</span></span>

<span data-ttu-id="70e15-105">Inviato a tutte le finestre di primo livello quando il sistema rileva più del 12,5% del tempo di sistema in un intervallo da 30 a 60 secondi viene impiegato per la compattazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="70e15-105">Sent to all top-level windows when the system detects more than 12.5 percent of system time over a 30- to 60-second interval is being spent compacting memory.</span></span> <span data-ttu-id="70e15-106">Indica che la memoria di sistema è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="70e15-106">This indicates that system memory is low.</span></span>

<span data-ttu-id="70e15-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="70e15-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="70e15-108">Questo messaggio viene fornito solo per la compatibilità con le applicazioni basate su Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="70e15-108">This message is provided only for compatibility with 16-bit Windows-based applications.</span></span>

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a><span data-ttu-id="70e15-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="70e15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70e15-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70e15-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70e15-111">Rapporto tra il tempo di unità di elaborazione centrale (CPU) attualmente impiegato dal sistema per la compattazione della memoria e il tempo di CPU attualmente impiegato dal sistema per l'esecuzione di altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="70e15-111">The ratio of central processing unit (CPU) time currently spent by the system compacting memory to CPU time currently spent by the system performing other operations.</span></span> <span data-ttu-id="70e15-112">Ad esempio, 0x8000 rappresenta il 50% del tempo di CPU dedicato alla compattazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="70e15-112">For example, 0x8000 represents 50 percent of CPU time spent compacting memory.</span></span>

</dd> <dt>

<span data-ttu-id="70e15-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70e15-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70e15-114">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="70e15-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70e15-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70e15-115">Return value</span></span>

<span data-ttu-id="70e15-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="70e15-116">Type: **LRESULT**</span></span>

<span data-ttu-id="70e15-117">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="70e15-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="70e15-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="70e15-118">Remarks</span></span>

<span data-ttu-id="70e15-119">Quando un'applicazione riceve questo messaggio, deve liberare il maggior numero di memoria possibile, prendendo in considerazione il livello corrente di attività dell'applicazione e il numero totale di applicazioni in esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="70e15-119">When an application receives this message, it should free as much memory as possible, taking into account the current level of activity of the application and the total number of applications running on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="70e15-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70e15-120">Requirements</span></span>



| <span data-ttu-id="70e15-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="70e15-121">Requirement</span></span> | <span data-ttu-id="70e15-122">Valore</span><span class="sxs-lookup"><span data-stu-id="70e15-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70e15-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70e15-123">Minimum supported client</span></span><br/> | <span data-ttu-id="70e15-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="70e15-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="70e15-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70e15-125">Minimum supported server</span></span><br/> | <span data-ttu-id="70e15-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="70e15-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="70e15-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70e15-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="70e15-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70e15-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70e15-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70e15-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e15-130">Panoramica di Windows</span><span class="sxs-lookup"><span data-stu-id="70e15-130">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
