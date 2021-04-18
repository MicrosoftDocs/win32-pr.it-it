---
description: 'Altre informazioni su: struttura JET_RECPOS'
title: Struttura JET_RECPOS
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315096"
---
# <a name="jet_recpos-structure"></a><span data-ttu-id="e87a9-103">Struttura JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="e87a9-103">JET_RECPOS Structure</span></span>


<span data-ttu-id="e87a9-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e87a9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recpos-structure"></a><span data-ttu-id="e87a9-105">Struttura JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="e87a9-105">JET_RECPOS Structure</span></span>

<span data-ttu-id="e87a9-106">La struttura **JET_RECPOS** contiene una raccolta di numeri interi che rappresentano una posizione frazionaria all'interno di un indice.</span><span class="sxs-lookup"><span data-stu-id="e87a9-106">The **JET_RECPOS** structure contains a collection of integers that represent a fractional position within an index.</span></span> <span data-ttu-id="e87a9-107">**centriesLT** è il numero di voci di indice minori della chiave di indice corrente.</span><span class="sxs-lookup"><span data-stu-id="e87a9-107">**centriesLT** is the number of index entries less than the current index key.</span></span> <span data-ttu-id="e87a9-108">**centriesInRange** è il numero di voci di indice uguali alla chiave corrente.</span><span class="sxs-lookup"><span data-stu-id="e87a9-108">**centriesInRange** is the number of index entries equal to the current key.</span></span> <span data-ttu-id="e87a9-109">**centriesInRange** non è supportato e viene sempre restituito come 1.</span><span class="sxs-lookup"><span data-stu-id="e87a9-109">**centriesInRange** is not supported and is always returned as 1.</span></span> <span data-ttu-id="e87a9-110">**centriesTotal** è il numero di voci di indice nell'indice.</span><span class="sxs-lookup"><span data-stu-id="e87a9-110">**centriesTotal** is the number of index entries in the index.</span></span> <span data-ttu-id="e87a9-111">Tutti i valori sono approssimazioni senza alcuna garanzia di accuratezza.</span><span class="sxs-lookup"><span data-stu-id="e87a9-111">All values are approximations with no guarantee of accuracy.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a><span data-ttu-id="e87a9-112">Membri</span><span class="sxs-lookup"><span data-stu-id="e87a9-112">Members</span></span>

<span data-ttu-id="e87a9-113">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="e87a9-113">**cbStruct**</span></span>

<span data-ttu-id="e87a9-114">Dimensioni in byte della struttura [JET_RETINFO](./jet-retinfo-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="e87a9-114">The size of the [JET_RETINFO](./jet-retinfo-structure.md) structure, in bytes.</span></span> <span data-ttu-id="e87a9-115">Questo valore conferma la presenza dei campi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e87a9-115">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="e87a9-116">**centriesLT**</span><span class="sxs-lookup"><span data-stu-id="e87a9-116">**centriesLT**</span></span>

<span data-ttu-id="e87a9-117">Numero approssimativo di voci di indice minori della chiave corrente.</span><span class="sxs-lookup"><span data-stu-id="e87a9-117">The approximate number of index entries less than the current key.</span></span>

<span data-ttu-id="e87a9-118">**centriesInRange**</span><span class="sxs-lookup"><span data-stu-id="e87a9-118">**centriesInRange**</span></span>

<span data-ttu-id="e87a9-119">Numero approssimativo di voci di indice uguali alla chiave corrente.</span><span class="sxs-lookup"><span data-stu-id="e87a9-119">The approximate number of index entries equal to the current key.</span></span> <span data-ttu-id="e87a9-120">Questo campo è sempre impostato su 1, indipendentemente dal numero di voci di indice effettivamente uguali alla chiave corrente.</span><span class="sxs-lookup"><span data-stu-id="e87a9-120">This field is always set to 1, regardless of the number of index entries that are actually equal to the current key.</span></span>

<span data-ttu-id="e87a9-121">**centriesTotal**</span><span class="sxs-lookup"><span data-stu-id="e87a9-121">**centriesTotal**</span></span>

<span data-ttu-id="e87a9-122">Numero approssimativo di voci nell'indice.</span><span class="sxs-lookup"><span data-stu-id="e87a9-122">The approximate number of entries in the index.</span></span>

### <a name="requirements"></a><span data-ttu-id="e87a9-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e87a9-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e87a9-124"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e87a9-124"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e87a9-125">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e87a9-125">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e87a9-126"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e87a9-126"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e87a9-127">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e87a9-127">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e87a9-128"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="e87a9-128"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e87a9-129">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e87a9-129">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e87a9-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e87a9-130">See Also</span></span>

[<span data-ttu-id="e87a9-131">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="e87a9-131">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="e87a9-132">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="e87a9-132">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)
