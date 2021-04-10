---
description: Scrive un evento completo in una sessione.
title: EtwEventWriteFull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 5ea3de0dba842544b0ffacc785fb138bdda571a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966243"
---
# <a name="etweventwritefull-function"></a><span data-ttu-id="774d8-103">EtwEventWriteFull (funzione)</span><span class="sxs-lookup"><span data-stu-id="774d8-103">EtwEventWriteFull function</span></span>

<span data-ttu-id="774d8-104">[La funzione EtwEventWriteFull e le strutture restituite sono interne al sistema operativo e soggette a modifiche da una versione di Windows a un'altra.]</span><span class="sxs-lookup"><span data-stu-id="774d8-104">[The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="774d8-105">Scrive un evento completo in una sessione.</span><span class="sxs-lookup"><span data-stu-id="774d8-105">Writes a full event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="774d8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="774d8-106">Syntax</span></span>

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="774d8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="774d8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="774d8-108">*RegHandle*</span><span class="sxs-lookup"><span data-stu-id="774d8-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="774d8-109">RegHandle per il provider.</span><span class="sxs-lookup"><span data-stu-id="774d8-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="774d8-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="774d8-110">*EventDescriptor*</span></span> 
</dt> <dd>

<span data-ttu-id="774d8-111">Descrittore dell'evento da registrare.</span><span class="sxs-lookup"><span data-stu-id="774d8-111">Event Descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="774d8-112">*EventProperty*</span><span class="sxs-lookup"><span data-stu-id="774d8-112">*EventProperty*</span></span>
</dt> <dd>

<span data-ttu-id="774d8-113">Flag fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="774d8-113">Flag given by the user.</span></span>

</dd> <dt>

<span data-ttu-id="774d8-114">*ActivityId*</span><span class="sxs-lookup"><span data-stu-id="774d8-114">*ActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="774d8-115">ID attività.</span><span class="sxs-lookup"><span data-stu-id="774d8-115">Activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="774d8-116">*RelatedActivityId*</span><span class="sxs-lookup"><span data-stu-id="774d8-116">*RelatedActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="774d8-117">ID attività correlata.</span><span class="sxs-lookup"><span data-stu-id="774d8-117">Related activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="774d8-118">*UserDataCount*</span><span class="sxs-lookup"><span data-stu-id="774d8-118">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="774d8-119">Numero di elementi di dati utente.</span><span class="sxs-lookup"><span data-stu-id="774d8-119">The number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="774d8-120">*UserData*</span><span class="sxs-lookup"><span data-stu-id="774d8-120">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="774d8-121">Puntatore a una matrice di elementi di dati utente.</span><span class="sxs-lookup"><span data-stu-id="774d8-121">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="774d8-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="774d8-122">Return value</span></span>

<span data-ttu-id="774d8-123">Codice di errore Win32.</span><span class="sxs-lookup"><span data-stu-id="774d8-123">A Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="774d8-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="774d8-124">Remarks</span></span>

<span data-ttu-id="774d8-125">La funzione EtwEventWriteFull e le strutture restituite sono interne al sistema operativo e sono soggette a modifiche da una versione di Windows a un'altra.</span><span class="sxs-lookup"><span data-stu-id="774d8-125">The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="774d8-126">Per mantenere la compatibilità dell'applicazione, è preferibile usare invece le funzioni pubbliche.</span><span class="sxs-lookup"><span data-stu-id="774d8-126">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>


## <a name="requirements"></a><span data-ttu-id="774d8-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="774d8-127">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="774d8-128">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="774d8-128">**Target Platform**</span></span> | <span data-ttu-id="774d8-129">Windows</span><span class="sxs-lookup"><span data-stu-id="774d8-129">Windows</span></span> |
| <span data-ttu-id="774d8-130">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="774d8-130">**Header**</span></span> | <span data-ttu-id="774d8-131">ntetw. h</span><span class="sxs-lookup"><span data-stu-id="774d8-131">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="774d8-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="774d8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774d8-133">EventWrite</span><span class="sxs-lookup"><span data-stu-id="774d8-133">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="774d8-134">EventWriteEx</span><span class="sxs-lookup"><span data-stu-id="774d8-134">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
