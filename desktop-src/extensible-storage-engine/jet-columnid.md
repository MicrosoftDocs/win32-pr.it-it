---
description: 'Altre informazioni su: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878606"
---
# <a name="jet_columnid"></a><span data-ttu-id="c52a8-103">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="c52a8-103">JET_COLUMNID</span></span>


<span data-ttu-id="c52a8-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c52a8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnid"></a><span data-ttu-id="c52a8-105">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="c52a8-105">JET_COLUMNID</span></span>

<span data-ttu-id="c52a8-106">Il tipo di dati **JET_COLUMNID** identifica una colonna all'interno di una tabella.</span><span class="sxs-lookup"><span data-stu-id="c52a8-106">The **JET_COLUMNID** data type identifies a column within a table.</span></span>

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a><span data-ttu-id="c52a8-107">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="c52a8-107">Data Types</span></span>

<span data-ttu-id="c52a8-108">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="c52a8-108">JET_COLUMNID</span></span>

<span data-ttu-id="c52a8-109">Identifica una colonna all'interno di una tabella.</span><span class="sxs-lookup"><span data-stu-id="c52a8-109">Identifies a column within a table.</span></span>

### <a name="remarks"></a><span data-ttu-id="c52a8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c52a8-110">Remarks</span></span>

<span data-ttu-id="c52a8-111">Gli ID di colonna sono univoci all'interno di una singola tabella.</span><span class="sxs-lookup"><span data-stu-id="c52a8-111">Column IDs are unique within a single table.</span></span> <span data-ttu-id="c52a8-112">Una volta che una colonna dispone di un ID di colonna specifico, avrà sempre l'ID della colonna.</span><span class="sxs-lookup"><span data-stu-id="c52a8-112">Once a column is known to have a certain column ID, it will always have that column ID.</span></span> <span data-ttu-id="c52a8-113">Il ripristino da backup non comporterà la modifica del valore di un ID di colonna.</span><span class="sxs-lookup"><span data-stu-id="c52a8-113">Restore from backup will not change the value of a column ID.</span></span> <span data-ttu-id="c52a8-114">Tuttavia, se una o più colonne della tabella, precedenti a una colonna della tabella specifica, vengono eliminate, un database compatto può modificare il valore di un ID di colonna.</span><span class="sxs-lookup"><span data-stu-id="c52a8-114">However, if one or more table columns, prior to a specific table column, are deleted, a compact database can then change the value of a column ID.</span></span>

<span data-ttu-id="c52a8-115">In alcuni casi, gli ID di colonna costituiscono l'unico mezzo per identificare le colonne.</span><span class="sxs-lookup"><span data-stu-id="c52a8-115">In some cases, column IDs are the only means of identifying columns.</span></span> <span data-ttu-id="c52a8-116">Quando viene creata una tabella temporanea, le relative colonne non hanno nomi, ma una matrice di ID di colonna viene restituita dalla funzione create.</span><span class="sxs-lookup"><span data-stu-id="c52a8-116">When a temporary table is created, its columns do not have names, but an array of column IDs is returned by the create function.</span></span>

<span data-ttu-id="c52a8-117">Le colonne in tabelle diverse possono avere lo stesso ID di colonna.</span><span class="sxs-lookup"><span data-stu-id="c52a8-117">Columns in different tables can have the same column ID.</span></span>

### <a name="requirements"></a><span data-ttu-id="c52a8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c52a8-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c52a8-119"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c52a8-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c52a8-120">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c52a8-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c52a8-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c52a8-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c52a8-122">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c52a8-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c52a8-123"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c52a8-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c52a8-124">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c52a8-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

