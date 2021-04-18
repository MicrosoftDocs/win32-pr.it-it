---
description: 'Altre informazioni su: struttura JET_BKLOGTIME'
title: Struttura JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: 0b3ebfd1c0b807a491695ba18d6735e0230a16fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316498"
---
# <a name="jet_bklogtime-structure"></a><span data-ttu-id="ee944-103">Struttura JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="ee944-103">JET_BKLOGTIME Structure</span></span>


<span data-ttu-id="ee944-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ee944-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bklogtime-structure"></a><span data-ttu-id="ee944-105">Struttura JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="ee944-105">JET_BKLOGTIME Structure</span></span>

<span data-ttu-id="ee944-106">La struttura **JET_BKLOGTIME** include gli elementi di data e ora di un evento.</span><span class="sxs-lookup"><span data-stu-id="ee944-106">The **JET_BKLOGTIME** structure holds the date and time elements of an event.</span></span> <span data-ttu-id="ee944-107">Si tratta di un'estensione di [JET_LOGTIME](./jet-logtime-structure.md).</span><span class="sxs-lookup"><span data-stu-id="ee944-107">It is an extension of [JET_LOGTIME](./jet-logtime-structure.md).</span></span>

<span data-ttu-id="ee944-108">**Windows Vista: JET_BKLOGTIME** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ee944-108">**Windows Vista:  JET_BKLOGTIME** is introduced in Windows Vista.</span></span>

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a><span data-ttu-id="ee944-109">Membri</span><span class="sxs-lookup"><span data-stu-id="ee944-109">Members</span></span>

<span data-ttu-id="ee944-110">**bSeconds**</span><span class="sxs-lookup"><span data-stu-id="ee944-110">**bSeconds**</span></span>

<span data-ttu-id="ee944-111">Ora dell'evento in secondi.</span><span class="sxs-lookup"><span data-stu-id="ee944-111">The time of the event in seconds.</span></span> <span data-ttu-id="ee944-112">Il valore può essere 0 (zero) e 60.</span><span class="sxs-lookup"><span data-stu-id="ee944-112">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="ee944-113">0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".</span><span class="sxs-lookup"><span data-stu-id="ee944-113">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="ee944-114">**bMinutes**</span><span class="sxs-lookup"><span data-stu-id="ee944-114">**bMinutes**</span></span>

<span data-ttu-id="ee944-115">Ora dell'evento in minuti.</span><span class="sxs-lookup"><span data-stu-id="ee944-115">The time of the event in minutes.</span></span> <span data-ttu-id="ee944-116">Il valore può essere 0 (zero) e 60.</span><span class="sxs-lookup"><span data-stu-id="ee944-116">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="ee944-117">0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".</span><span class="sxs-lookup"><span data-stu-id="ee944-117">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="ee944-118">**Gabriele**</span><span class="sxs-lookup"><span data-stu-id="ee944-118">**bHours**</span></span>

<span data-ttu-id="ee944-119">Ora dell'evento in ore.</span><span class="sxs-lookup"><span data-stu-id="ee944-119">The time of the event in hours.</span></span> <span data-ttu-id="ee944-120">Può essere 0 (zero) a 24.</span><span class="sxs-lookup"><span data-stu-id="ee944-120">This can be 0 (zero) to 24.</span></span> <span data-ttu-id="ee944-121">0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".</span><span class="sxs-lookup"><span data-stu-id="ee944-121">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="ee944-122">**bDay**</span><span class="sxs-lookup"><span data-stu-id="ee944-122">**bDay**</span></span>

<span data-ttu-id="ee944-123">Giorno del mese dell'evento.</span><span class="sxs-lookup"><span data-stu-id="ee944-123">The day of the month of the event.</span></span> <span data-ttu-id="ee944-124">Può essere 0 (zero) a 31.</span><span class="sxs-lookup"><span data-stu-id="ee944-124">This can be 0 (zero) to 31.</span></span> <span data-ttu-id="ee944-125">0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".</span><span class="sxs-lookup"><span data-stu-id="ee944-125">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="ee944-126">**bMonth**</span><span class="sxs-lookup"><span data-stu-id="ee944-126">**bMonth**</span></span>

<span data-ttu-id="ee944-127">Mese dell'anno dell'evento.</span><span class="sxs-lookup"><span data-stu-id="ee944-127">The month of the year of the event.</span></span> <span data-ttu-id="ee944-128">Può essere 0 (zero) a 12.</span><span class="sxs-lookup"><span data-stu-id="ee944-128">This can be 0 (zero) to 12.</span></span> <span data-ttu-id="ee944-129">0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".</span><span class="sxs-lookup"><span data-stu-id="ee944-129">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="ee944-130">**bYear**</span><span class="sxs-lookup"><span data-stu-id="ee944-130">**bYear**</span></span>

<span data-ttu-id="ee944-131">Anno (offset di 1900) dell'evento.</span><span class="sxs-lookup"><span data-stu-id="ee944-131">The year (offset by 1900) of the event.</span></span> <span data-ttu-id="ee944-132">Per ottenere l'anno effettivo, aggiungere 1900 a questo valore.</span><span class="sxs-lookup"><span data-stu-id="ee944-132">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="ee944-133">0 (zero) viene usato quando la struttura del **JET_BKLOGTIME** è "null".</span><span class="sxs-lookup"><span data-stu-id="ee944-133">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="ee944-134">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="ee944-134">**bFiller1**</span></span>

<span data-ttu-id="ee944-135">Questo campo deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ee944-135">This field should be ignored.</span></span>

<span data-ttu-id="ee944-136">**fTimeIsUTC**</span><span class="sxs-lookup"><span data-stu-id="ee944-136">**fTimeIsUTC**</span></span>

<span data-ttu-id="ee944-137">L'ora è in formato UTC.</span><span class="sxs-lookup"><span data-stu-id="ee944-137">The time is in UTC format.</span></span>

<span data-ttu-id="ee944-138">**fUnused**</span><span class="sxs-lookup"><span data-stu-id="ee944-138">**fUnused**</span></span>

<span data-ttu-id="ee944-139">Questo campo deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ee944-139">This field should be ignored.</span></span>

<span data-ttu-id="ee944-140">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="ee944-140">**bFiller2**</span></span>

<span data-ttu-id="ee944-141">Questo campo deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ee944-141">This field should be ignored.</span></span>

<span data-ttu-id="ee944-142">**fOSSnapshot**</span><span class="sxs-lookup"><span data-stu-id="ee944-142">**fOSSnapshot**</span></span>

<span data-ttu-id="ee944-143">Se questo evento è un backup, questo flag contiene uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee944-143">If this event is a backup, this flag contains one of the following possible values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee944-144">Nome</span><span class="sxs-lookup"><span data-stu-id="ee944-144">Name</span></span></p></th>
<th><p><span data-ttu-id="ee944-145">Valore</span><span class="sxs-lookup"><span data-stu-id="ee944-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee944-146">backup di flusso</span><span class="sxs-lookup"><span data-stu-id="ee944-146">streaming backup</span></span></p></td>
<td><p><span data-ttu-id="ee944-147">0 (zero)</span><span class="sxs-lookup"><span data-stu-id="ee944-147">0 (zero)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee944-148">backup di snapshot</span><span class="sxs-lookup"><span data-stu-id="ee944-148">snapshot backup</span></span></p></td>
<td><p><span data-ttu-id="ee944-149">1</span><span class="sxs-lookup"><span data-stu-id="ee944-149">1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee944-150">**fReserved**</span><span class="sxs-lookup"><span data-stu-id="ee944-150">**fReserved**</span></span>

<span data-ttu-id="ee944-151">Questo campo deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="ee944-151">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="ee944-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee944-152">Remarks</span></span>

<span data-ttu-id="ee944-153">Questa struttura viene utilizzata durante il debug.</span><span class="sxs-lookup"><span data-stu-id="ee944-153">This structure is used when debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="ee944-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee944-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee944-155"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ee944-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ee944-156">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ee944-156">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee944-157"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ee944-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ee944-158">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ee944-158">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee944-159"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ee944-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ee944-160">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ee944-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ee944-161">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ee944-161">See Also</span></span>

[<span data-ttu-id="ee944-162">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="ee944-162">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="ee944-163">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="ee944-163">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
