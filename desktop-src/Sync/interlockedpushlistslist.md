---
UID: ''
title: Funzione InterlockedPushListSList
description: Inserisce un elenco collegato singolarmente davanti a un altro elenco collegato singolarmente.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/29/2020
ms.locfileid: "104398779"
---
# <a name="interlockedpushlistslist-function"></a><span data-ttu-id="12aae-103">Funzione InterlockedPushListSList</span><span class="sxs-lookup"><span data-stu-id="12aae-103">InterlockedPushListSList function</span></span>

## <a name="description"></a><span data-ttu-id="12aae-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12aae-104">Description</span></span>

<span data-ttu-id="12aae-105">Inserisce un elenco collegato singolarmente davanti a un altro elenco collegato singolarmente.</span><span class="sxs-lookup"><span data-stu-id="12aae-105">Inserts a singly-linked list at the front of another singly linked list.</span></span>
<span data-ttu-id="12aae-106">L'accesso agli elenchi è sincronizzato in un sistema multiprocessore.</span><span class="sxs-lookup"><span data-stu-id="12aae-106">Access to the lists is synchronized on a multiprocessor system.</span></span>

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a><span data-ttu-id="12aae-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="12aae-107">Parameters</span></span>

### <a name="listhead-in-out"></a><span data-ttu-id="12aae-108">ListHead [in, out]</span><span class="sxs-lookup"><span data-stu-id="12aae-108">ListHead [in, out]</span></span>

<span data-ttu-id="12aae-109">Puntatore a una struttura **SLIST_HEADER** che rappresenta l'intestazione di un elenco collegato singolarmente.</span><span class="sxs-lookup"><span data-stu-id="12aae-109">Pointer to an **SLIST_HEADER** structure that represents the head of a singly linked list.</span></span>
<span data-ttu-id="12aae-110">L'elenco specificato dall'elenco *e dai* parametri di *ascolto* viene inserito all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="12aae-110">The list specified by the *List* and *ListEnd* parameters is inserted at the front of this list.</span></span>

### <a name="list-in-out"></a><span data-ttu-id="12aae-111">Elenco [in, out]</span><span class="sxs-lookup"><span data-stu-id="12aae-111">List [in, out]</span></span>

<span data-ttu-id="12aae-112">Puntatore a una struttura [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) che rappresenta il primo elemento dell'elenco da inserire.</span><span class="sxs-lookup"><span data-stu-id="12aae-112">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the first item in the list to be inserted.</span></span>

### <a name="listend-in-out"></a><span data-ttu-id="12aae-113">In ascolto [in, out]</span><span class="sxs-lookup"><span data-stu-id="12aae-113">ListEnd [in, out]</span></span>

<span data-ttu-id="12aae-114">Puntatore a una struttura [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) che rappresenta l'ultimo elemento dell'elenco da inserire.</span><span class="sxs-lookup"><span data-stu-id="12aae-114">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the last item in the list to be inserted.</span></span>

### <a name="count-in"></a><span data-ttu-id="12aae-115">Count [in]</span><span class="sxs-lookup"><span data-stu-id="12aae-115">Count [in]</span></span>

<span data-ttu-id="12aae-116">Numero di elementi nell'elenco da inserire.</span><span class="sxs-lookup"><span data-stu-id="12aae-116">The number of items in the list to be inserted.</span></span>

## <a name="returns"></a><span data-ttu-id="12aae-117">Restituisce</span><span class="sxs-lookup"><span data-stu-id="12aae-117">Returns</span></span>

<span data-ttu-id="12aae-118">Il valore restituito è il primo elemento precedente nell'elenco specificato dal parametro *listhead* .</span><span class="sxs-lookup"><span data-stu-id="12aae-118">The return value is the previous first item in the list specified by the *ListHead* parameter.</span></span>
<span data-ttu-id="12aae-119">Se l'elenco è stato precedentemente vuoto, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="12aae-119">If the list was previously empty, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="12aae-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="12aae-120">Remarks</span></span>

<span data-ttu-id="12aae-121">Tutti gli elementi dell'elenco devono essere allineati su un limite di **MEMORY_ALLOCATION_ALIGNMENT** ; in caso contrario, questa funzione si comporterà in modo imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="12aae-121">All list items must be aligned on a **MEMORY_ALLOCATION_ALIGNMENT** boundary; otherwise, this function will behave unpredictably.</span></span>
<span data-ttu-id="12aae-122">Vedere **_aligned_malloc**.</span><span class="sxs-lookup"><span data-stu-id="12aae-122">See **_aligned_malloc**.</span></span>

<span data-ttu-id="12aae-123">**Windows 8 e Windows Server 2012:**  Questa funzione è stata sostituita da [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span><span class="sxs-lookup"><span data-stu-id="12aae-123">**Windows 8 and Windows Server 2012:**  This function has been superceded by [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span></span>
<span data-ttu-id="12aae-124">Quando si esegue la compilazione con **NTDDI_VERSION** impostato su **NTDDI_WIN8** o versione successiva, le chiamate a **InterlockedPushListSList** andranno invece a **InterlockedPushListSListEx** .</span><span class="sxs-lookup"><span data-stu-id="12aae-124">When compiling with **NTDDI_VERSION** set to **NTDDI_WIN8** or greater, calls to **InterlockedPushListSList** will go to **InterlockedPushListSListEx** instead.</span></span>

## <a name="see-also"></a><span data-ttu-id="12aae-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12aae-125">See also</span></span>

[<span data-ttu-id="12aae-126">Elenchi collegati singolarmente con Interlocking</span><span class="sxs-lookup"><span data-stu-id="12aae-126">Interlocked Singly Linked Lists</span></span>](/windows/desktop/Sync/interlocked-singly-linked-lists)

[<span data-ttu-id="12aae-127">InterlockedPopEntrySList</span><span class="sxs-lookup"><span data-stu-id="12aae-127">InterlockedPopEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[<span data-ttu-id="12aae-128">InterlockedPushEntrySList</span><span class="sxs-lookup"><span data-stu-id="12aae-128">InterlockedPushEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[<span data-ttu-id="12aae-129">InterlockedPushListSListEx</span><span class="sxs-lookup"><span data-stu-id="12aae-129">InterlockedPushListSListEx</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[<span data-ttu-id="12aae-130">InterlockedFlushSList</span><span class="sxs-lookup"><span data-stu-id="12aae-130">InterlockedFlushSList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[<span data-ttu-id="12aae-131">SLIST_ENTRY</span><span class="sxs-lookup"><span data-stu-id="12aae-131">SLIST_ENTRY</span></span>](/windows/win32/api/winnt/ns-winnt-slist_entry)

[<span data-ttu-id="12aae-132">Uso di elenchi collegati singolarmente</span><span class="sxs-lookup"><span data-stu-id="12aae-132">Using Singly Linked Lists</span></span>](/windows/desktop/Sync/using-singly-linked-lists)
