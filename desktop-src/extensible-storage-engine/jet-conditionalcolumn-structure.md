---
description: 'Altre informazioni su: struttura JET_CONDITIONALCOLUMN'
title: Struttura JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308496"
---
# <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="5c02c-103">Struttura JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="5c02c-103">JET_CONDITIONALCOLUMN Structure</span></span>


<span data-ttu-id="5c02c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5c02c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="5c02c-105">Struttura JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="5c02c-105">JET_CONDITIONALCOLUMN Structure</span></span>

<span data-ttu-id="5c02c-106">La struttura **JET_CONDITIONALCOLUMN** definisce il modo in cui viene eseguita l'indicizzazione condizionale per un indice specificato.</span><span class="sxs-lookup"><span data-stu-id="5c02c-106">The **JET_CONDITIONALCOLUMN** structure defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="5c02c-107">Un indice condizionale contiene una voce di indice solo per le righe che corrispondono alla condizione specificata.</span><span class="sxs-lookup"><span data-stu-id="5c02c-107">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="5c02c-108">Tuttavia, la colonna condizionale non fa parte della chiave dell'indice, ma controlla solo la presenza della voce di indice.</span><span class="sxs-lookup"><span data-stu-id="5c02c-108">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a><span data-ttu-id="5c02c-109">Membri</span><span class="sxs-lookup"><span data-stu-id="5c02c-109">Members</span></span>

<span data-ttu-id="5c02c-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="5c02c-110">**cbStruct**</span></span>

<span data-ttu-id="5c02c-111">Questo campo deve essere inizializzato su sizeof (JET_CONDITIONALCOLUMN), in byte.</span><span class="sxs-lookup"><span data-stu-id="5c02c-111">This field must be initialized to sizeof( JET_CONDITIONALCOLUMN ), in bytes.</span></span>

<span data-ttu-id="5c02c-112">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="5c02c-112">**szColumnName**</span></span>

<span data-ttu-id="5c02c-113">Nome della colonna contenente i dati su cui il motore di database sta indicizzando la riga in modo condizionale.</span><span class="sxs-lookup"><span data-stu-id="5c02c-113">The name of the column that contains the data on which the database engine is conditionally indexing the row.</span></span>

<span data-ttu-id="5c02c-114">**grbit** Gruppo di bit che fornisce le opzioni per l'indice condizionale.</span><span class="sxs-lookup"><span data-stu-id="5c02c-114">**grbit** A group of bits that gives the options for the conditional index.</span></span> <span data-ttu-id="5c02c-115">Il passaggio di valori zero o logici **o** ed non è valido per **JET_CONDITIONALCOLUMN**.</span><span class="sxs-lookup"><span data-stu-id="5c02c-115">Passing in zero or logically-**OR** ed values is not valid for **JET_CONDITIONALCOLUMN**.</span></span> <span data-ttu-id="5c02c-116">Il campo di bit deve essere esattamente uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c02c-116">The bit field must be exactly one of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c02c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5c02c-117">Value</span></span></p></th>
<th><p><span data-ttu-id="5c02c-118">Significato</span><span class="sxs-lookup"><span data-stu-id="5c02c-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c02c-119">JET_bitIndexColumnMustBeNull</span><span class="sxs-lookup"><span data-stu-id="5c02c-119">JET_bitIndexColumnMustBeNull</span></span></p></td>
<td><p><span data-ttu-id="5c02c-120">La colonna specificata dal parametro <em>szColumnName</em> deve essere null per visualizzare in questo indice una voce di indice per una determinata riga.</span><span class="sxs-lookup"><span data-stu-id="5c02c-120">The column specified by the <em>szColumnName</em> parameter must be NULL for an index entry for a given row to appear in this index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c02c-121">JET_bitIndexColumnMustBeNonNull</span><span class="sxs-lookup"><span data-stu-id="5c02c-121">JET_bitIndexColumnMustBeNonNull</span></span></p></td>
<td><p><span data-ttu-id="5c02c-122">La colonna specificata dal parametro <em>szColumnName</em> non deve essere null per una voce di indice affinché una determinata riga venga visualizzata in questo indice.</span><span class="sxs-lookup"><span data-stu-id="5c02c-122">The column specified by the <em>szColumnName</em> parameter must be non-NULL for an index entry in order for a given row to appear in this index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="5c02c-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c02c-123">Remarks</span></span>

<span data-ttu-id="5c02c-124">Un indice condizionale contiene una voce di indice solo per le righe che corrispondono alla condizione specificata.</span><span class="sxs-lookup"><span data-stu-id="5c02c-124">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="5c02c-125">Una colonna, ad esempio, può essere denominata "contrassegnato" e, quando una riga è contrassegnata, la colonna viene impostata su un valore non NULL.</span><span class="sxs-lookup"><span data-stu-id="5c02c-125">For example, a column could be named "Marked", and when a row is marked, the column is set to a non-NULL value.</span></span> <span data-ttu-id="5c02c-126">Un JET_bitIndexColumnMustBeNonNull Indice condizionale in questa colonna mostrerà tutte le righe contrassegnate e un indice condizionale JET_bitIndexColumnMustBeNull mostrerà le righe non contrassegnate.</span><span class="sxs-lookup"><span data-stu-id="5c02c-126">A JET_bitIndexColumnMustBeNonNull conditional index on this column will show all rows that are marked, and a JET_bitIndexColumnMustBeNull conditional index will show rows that are not marked.</span></span> <span data-ttu-id="5c02c-127">Questo è anche un modo pratico per eseguire un'eliminazione di flag e un indice di Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="5c02c-127">This is also a convenient way to perform a flag deletion and garbage collecting index.</span></span>

### <a name="requirements"></a><span data-ttu-id="5c02c-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c02c-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c02c-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5c02c-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5c02c-130">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5c02c-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c02c-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5c02c-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5c02c-132">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5c02c-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c02c-133"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="5c02c-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5c02c-134">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="5c02c-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c02c-135"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5c02c-135"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5c02c-136">Implementato come <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) e <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5c02c-136">Implemented as <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) and <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5c02c-137">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5c02c-137">See Also</span></span>

[<span data-ttu-id="5c02c-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5c02c-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5c02c-139">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="5c02c-139">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)
