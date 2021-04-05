---
description: 'Altre informazioni su: struttura JET_LOGTIME'
title: Struttura JET_LOGTIME
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762425"
---
# <a name="jet_logtime-structure"></a><span data-ttu-id="41228-103">Struttura JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="41228-103">JET_LOGTIME Structure</span></span>


<span data-ttu-id="41228-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="41228-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_logtime-structure"></a><span data-ttu-id="41228-105">Struttura JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="41228-105">JET_LOGTIME Structure</span></span>

<span data-ttu-id="41228-106">La struttura **JET_LOGTIME** include gli elementi della data e dell'ora di un evento.</span><span class="sxs-lookup"><span data-stu-id="41228-106">The **JET_LOGTIME** structure holds elements of the date and time of an event.</span></span>

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a><span data-ttu-id="41228-107">Membri</span><span class="sxs-lookup"><span data-stu-id="41228-107">Members</span></span>

<span data-ttu-id="41228-108">**bSeconds**</span><span class="sxs-lookup"><span data-stu-id="41228-108">**bSeconds**</span></span>

<span data-ttu-id="41228-109">Ora dell'evento in secondi.</span><span class="sxs-lookup"><span data-stu-id="41228-109">The time of the event in seconds.</span></span> <span data-ttu-id="41228-110">Questo valore può essere compreso tra 0 e 59.</span><span class="sxs-lookup"><span data-stu-id="41228-110">This value can be 0 to 59.</span></span> <span data-ttu-id="41228-111">0 viene utilizzato quando la struttura è null.</span><span class="sxs-lookup"><span data-stu-id="41228-111">0 is used when the structure is null.</span></span>

<span data-ttu-id="41228-112">**bMinutes**</span><span class="sxs-lookup"><span data-stu-id="41228-112">**bMinutes**</span></span>

<span data-ttu-id="41228-113">Ora dell'evento in minuti.</span><span class="sxs-lookup"><span data-stu-id="41228-113">The time of the event in minutes.</span></span> <span data-ttu-id="41228-114">Questo valore può essere compreso tra 0 e 59.</span><span class="sxs-lookup"><span data-stu-id="41228-114">This value can be 0 to 59.</span></span> <span data-ttu-id="41228-115">0 viene utilizzato quando la struttura è null.</span><span class="sxs-lookup"><span data-stu-id="41228-115">0 is used when the structure is null.</span></span>

<span data-ttu-id="41228-116">**Gabriele**</span><span class="sxs-lookup"><span data-stu-id="41228-116">**bHours**</span></span>

<span data-ttu-id="41228-117">Ora dell'evento in ore.</span><span class="sxs-lookup"><span data-stu-id="41228-117">The time of the event in hours.</span></span> <span data-ttu-id="41228-118">Questo valore può essere compreso tra 0 e 23.</span><span class="sxs-lookup"><span data-stu-id="41228-118">This value can be 0 to 23.</span></span> <span data-ttu-id="41228-119">0 viene utilizzato quando la struttura è null.</span><span class="sxs-lookup"><span data-stu-id="41228-119">0 is used when the structure is null.</span></span>

<span data-ttu-id="41228-120">**bDay**</span><span class="sxs-lookup"><span data-stu-id="41228-120">**bDay**</span></span>

<span data-ttu-id="41228-121">Giorno del mese dell'evento.</span><span class="sxs-lookup"><span data-stu-id="41228-121">The day of the month of the event.</span></span> <span data-ttu-id="41228-122">Questo valore può essere compreso tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="41228-122">This value can be 0 to 31.</span></span> <span data-ttu-id="41228-123">0 viene utilizzato quando la struttura è null.</span><span class="sxs-lookup"><span data-stu-id="41228-123">0 is used when the structure is null.</span></span>

<span data-ttu-id="41228-124">**bMonth**</span><span class="sxs-lookup"><span data-stu-id="41228-124">**bMonth**</span></span>

<span data-ttu-id="41228-125">Mese dell'anno dell'evento.</span><span class="sxs-lookup"><span data-stu-id="41228-125">The month of the year of the event.</span></span> <span data-ttu-id="41228-126">Questo valore può essere compreso tra 0 e 12.</span><span class="sxs-lookup"><span data-stu-id="41228-126">This value can be 0 to 12.</span></span> <span data-ttu-id="41228-127">0 viene utilizzato quando la struttura è null.</span><span class="sxs-lookup"><span data-stu-id="41228-127">0 is used when the structure is null.</span></span>

<span data-ttu-id="41228-128">**bYear**</span><span class="sxs-lookup"><span data-stu-id="41228-128">**bYear**</span></span>

<span data-ttu-id="41228-129">Anno dell'evento (offset di 1900).</span><span class="sxs-lookup"><span data-stu-id="41228-129">The year of the event (offset by 1900).</span></span> <span data-ttu-id="41228-130">Per ottenere l'anno effettivo, aggiungere 1900 a questo valore.</span><span class="sxs-lookup"><span data-stu-id="41228-130">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="41228-131">0 viene utilizzato quando la struttura è null.</span><span class="sxs-lookup"><span data-stu-id="41228-131">0 is used when the structure is null.</span></span>

<span data-ttu-id="41228-132">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="41228-132">**bFiller1**</span></span>

<span data-ttu-id="41228-133">Questo campo deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="41228-133">This field should be ignored.</span></span>

<span data-ttu-id="41228-134">**fTimeIsUTC**</span><span class="sxs-lookup"><span data-stu-id="41228-134">**fTimeIsUTC**</span></span>

<span data-ttu-id="41228-135">L'ora è in formato UTC.</span><span class="sxs-lookup"><span data-stu-id="41228-135">The time is in UTC format.</span></span>

<span data-ttu-id="41228-136">**fUnused**</span><span class="sxs-lookup"><span data-stu-id="41228-136">**fUnused**</span></span>

<span data-ttu-id="41228-137">Questo campo deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="41228-137">This field should be ignored.</span></span>

<span data-ttu-id="41228-138">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="41228-138">**bFiller2**</span></span>

<span data-ttu-id="41228-139">Questo campo deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="41228-139">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="41228-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="41228-140">Remarks</span></span>

<span data-ttu-id="41228-141">Questa struttura è destinata principalmente all'uso nel debug.</span><span class="sxs-lookup"><span data-stu-id="41228-141">This structure is meant primarily for usage in debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="41228-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41228-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41228-143"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="41228-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="41228-144">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="41228-144">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41228-145"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="41228-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="41228-146">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="41228-146">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41228-147"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="41228-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="41228-148">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="41228-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="41228-149">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="41228-149">See Also</span></span>

[<span data-ttu-id="41228-150">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="41228-150">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
