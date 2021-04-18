---
description: 'Altre informazioni su: Enumerazione JET_TblInfo'
title: Enumerazione JET_TblInfo
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad43dcecf65fdc9fb8dd53bdf686a077e6bdfa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313107"
---
# <a name="jet_tblinfo-enumeration"></a><span data-ttu-id="d9ff8-103">Enumerazione JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="d9ff8-103">JET_TblInfo enumeration</span></span>

<span data-ttu-id="d9ff8-104">Livelli di informazioni per il recupero delle informazioni sulla tabella con JetGetTableInfo.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-104">Info levels for retrieving table info with JetGetTableInfo.</span></span>

<span data-ttu-id="d9ff8-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d9ff8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d9ff8-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d9ff8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d9ff8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9ff8-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
```

## <a name="members"></a><span data-ttu-id="d9ff8-108">Members</span><span class="sxs-lookup"><span data-stu-id="d9ff8-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d9ff8-109">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="d9ff8-109">Member name</span></span></th>
<th><span data-ttu-id="d9ff8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9ff8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d9ff8-111">Predefinito</span><span class="sxs-lookup"><span data-stu-id="d9ff8-111">Default</span></span></td>
<td><span data-ttu-id="d9ff8-112">Opzione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-112">Default option.</span></span> <span data-ttu-id="d9ff8-113">Recupera un <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> contenente le informazioni sulla tabella.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-113">Retrieves a <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> containing information about the table.</span></span> <span data-ttu-id="d9ff8-114">Usare questa opzione con <a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-114">Use this option with <a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d9ff8-115">Nome</span><span class="sxs-lookup"><span data-stu-id="d9ff8-115">Name</span></span></td>
<td><span data-ttu-id="d9ff8-116">Recupera il nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-116">Retrieves the name of the table.</span></span> <span data-ttu-id="d9ff8-117">Usare questa opzione con <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-117">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d9ff8-118">Dbid</span><span class="sxs-lookup"><span data-stu-id="d9ff8-118">Dbid</span></span></td>
<td><span data-ttu-id="d9ff8-119">Recupera la <a href="hh596176(v=exchg.10).md">JET_DBID</a> del database che contiene la tabella.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-119">Retrieves the <a href="hh596176(v=exchg.10).md">JET_DBID</a> of the database containing the table.</span></span> <span data-ttu-id="d9ff8-120">Usare questa opzione con <a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-120">Use this option with <a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d9ff8-121">SpaceUsage</span><span class="sxs-lookup"><span data-stu-id="d9ff8-121">SpaceUsage</span></span></td>
<td><span data-ttu-id="d9ff8-122">Il comportamento del metodo dipende dalla dimensione della matrice passata al metodo.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-122">The behavior of the method depends on how large the array that is passed to the method is.</span></span> <span data-ttu-id="d9ff8-123">La matrice deve contenere almeno due voci.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-123">The array must have at least two entries.</span></span> <span data-ttu-id="d9ff8-124">La prima voce conterrà il numero di extent di proprietà nella tabella.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-124">The first entry will contain the number of Owned Extents in the table.</span></span> <span data-ttu-id="d9ff8-125">La seconda voce conterrà il numero di extent disponibili nella tabella.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-125">The second entry will contain the number of Available Extents in the table.</span></span> <span data-ttu-id="d9ff8-126">Se la matrice contiene più di due voci, i byte rimanenti del buffer sono costituiti da una matrice di strutture che rappresentano un elenco di extent.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-126">If the array has more than two entries then the remaining bytes of the buffer will consist of an array of structures that represent a list of extents.</span></span> <span data-ttu-id="d9ff8-127">Questa struttura contiene due membri: l'ultimo numero di pagina nell'extent e il numero di pagine nell'extent.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-127">This structure contains two members: the last page number in the extent and the number of pages in the extent.</span></span> <span data-ttu-id="d9ff8-128">Usare questa opzione con <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [] JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-128">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d9ff8-129">SpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="d9ff8-129">SpaceAlloc</span></span></td>
<td><span data-ttu-id="d9ff8-130">La matrice passata a JetGetTableInfo deve avere due voci.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-130">The array passed to JetGetTableInfo must have two entries.</span></span> <span data-ttu-id="d9ff8-131">La prima voce verrà impostata sul numero di pagine della tabella.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-131">The first entry will be set to the number of pages in the table.</span></span> <span data-ttu-id="d9ff8-132">La seconda voce verrà impostata sulla densità di destinazione delle pagine per la tabella.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-132">The second entry will be set to the target density of pages for the table.</span></span> <span data-ttu-id="d9ff8-133">Usare questa opzione con <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [] JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-133">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d9ff8-134">SpaceOwned</span><span class="sxs-lookup"><span data-stu-id="d9ff8-134">SpaceOwned</span></span></td>
<td><span data-ttu-id="d9ff8-135">Ottiene il numero di pagine di proprietà nella tabella.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-135">Gets the number of owned pages in the table.</span></span> <span data-ttu-id="d9ff8-136">Usare questa opzione con <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-136">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d9ff8-137">SpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="d9ff8-137">SpaceAvailable</span></span></td>
<td><span data-ttu-id="d9ff8-138">Ottiene il numero di pagine disponibili nella tabella.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-138">Gets the number of available pages in the table.</span></span> <span data-ttu-id="d9ff8-139">Usare questa opzione con <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-139">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d9ff8-140">TemplateTableName</span><span class="sxs-lookup"><span data-stu-id="d9ff8-140">TemplateTableName</span></span></td>
<td><span data-ttu-id="d9ff8-141">Se la tabella è una tabella derivata, il risultato verrà compilato con il nome della tabella da cui la tabella derivata eredita la DDL.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-141">If the table is a derived table, the result will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="d9ff8-142">Se la tabella non è una tabella derivata, il buffer sarà una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-142">If the table is not a derived table, the buffer will an empty string.</span></span> <span data-ttu-id="d9ff8-143">Usare questa opzione con <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="d9ff8-143">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d9ff8-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9ff8-144">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d9ff8-145">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d9ff8-145">Reference</span></span>

[<span data-ttu-id="d9ff8-146">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d9ff8-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
