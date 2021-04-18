---
description: 'Altre informazioni su: Enumerazione JET_DbInfo'
title: Enumerazione JET_DbInfo
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39c6c3175c08e4f7644ad4f0b41137e12e84f71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306857"
---
# <a name="jet_dbinfo-enumeration"></a><span data-ttu-id="0cbc6-103">Enumerazione JET_DbInfo</span><span class="sxs-lookup"><span data-stu-id="0cbc6-103">JET_DbInfo enumeration</span></span>

<span data-ttu-id="0cbc6-104">Livelli di informazioni per il recupero delle informazioni sul database.</span><span class="sxs-lookup"><span data-stu-id="0cbc6-104">Info levels for retrieving database info.</span></span>

<span data-ttu-id="0cbc6-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0cbc6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0cbc6-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0cbc6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0cbc6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cbc6-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
```

## <a name="members"></a><span data-ttu-id="0cbc6-108">Members</span><span class="sxs-lookup"><span data-stu-id="0cbc6-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0cbc6-109">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="0cbc6-109">Member name</span></span></th>
<th><span data-ttu-id="0cbc6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cbc6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0cbc6-111">Nome file</span><span class="sxs-lookup"><span data-stu-id="0cbc6-111">Filename</span></span></td>
<td><span data-ttu-id="0cbc6-112">Restituisce il percorso del file di database (String).</span><span class="sxs-lookup"><span data-stu-id="0cbc6-112">Returns the path to the database file (string).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0cbc6-113">LCID</span><span class="sxs-lookup"><span data-stu-id="0cbc6-113">LCID</span></span></td>
<td><span data-ttu-id="0cbc6-114">Restituisce l'identificatore delle impostazioni locali (LCID) associato a questo database (Int32).</span><span class="sxs-lookup"><span data-stu-id="0cbc6-114">Returns the locale identifier (LCID) associated with this database (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0cbc6-115">Opzioni</span><span class="sxs-lookup"><span data-stu-id="0cbc6-115">Options</span></span></td>
<td><span data-ttu-id="0cbc6-116">Restituisce un <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="0cbc6-116">Returns a <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>.</span></span> <span data-ttu-id="0cbc6-117">Indica se il database è aperto in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="0cbc6-117">This indicates whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="0cbc6-118">Se il database è in modalità esclusiva, viene restituito <a href="hh579532(v=exchg.10).md">Exclusive</a> ; in caso contrario, viene restituito zero.</span><span class="sxs-lookup"><span data-stu-id="0cbc6-118">If the database is in exclusive mode then <a href="hh579532(v=exchg.10).md">Exclusive</a> will be returned, otherwise zero is returned.</span></span> <span data-ttu-id="0cbc6-119">Non vengono restituite altre opzioni di grbit del database per JetAttachDatabase e JetOpenDatabase.</span><span class="sxs-lookup"><span data-stu-id="0cbc6-119">Other database grbit options for JetAttachDatabase and JetOpenDatabase are not returned.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0cbc6-120">Transazioni</span><span class="sxs-lookup"><span data-stu-id="0cbc6-120">Transactions</span></span></td>
<td><span data-ttu-id="0cbc6-121">Restituisce un numero maggiore del livello massimo a cui è possibile annidare le transazioni.</span><span class="sxs-lookup"><span data-stu-id="0cbc6-121">Returns a number one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="0cbc6-122">Se viene chiamato <a href="dn292105(v=exchg.10).md">JetBeginTransaction (JET_SESID)</a> (in un modo annidato, ovvero nella stessa sessione senza commit o rollback) il numero di volte in cui questo valore viene restituito, nell'ultima chiamata a <a href="hh564840(v=exchg.10).md">TransTooDeep</a> verrà restituito (Int32).</span><span class="sxs-lookup"><span data-stu-id="0cbc6-122">If <a href="dn292105(v=exchg.10).md">JetBeginTransaction(JET_SESID)</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call <a href="hh564840(v=exchg.10).md">TransTooDeep</a> will be returned (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0cbc6-123">Versione</span><span class="sxs-lookup"><span data-stu-id="0cbc6-123">Version</span></span></td>
<td><span data-ttu-id="0cbc6-124">Restituisce la versione principale del motore di database (Int32).</span><span class="sxs-lookup"><span data-stu-id="0cbc6-124">Returns the major version of the database engine (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0cbc6-125">Filesize</span><span class="sxs-lookup"><span data-stu-id="0cbc6-125">Filesize</span></span></td>
<td><span data-ttu-id="0cbc6-126">Restituisce il Filesize del database, in pagine (Int32).</span><span class="sxs-lookup"><span data-stu-id="0cbc6-126">Returns the filesize of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0cbc6-127">SpaceOwned</span><span class="sxs-lookup"><span data-stu-id="0cbc6-127">SpaceOwned</span></span></td>
<td><span data-ttu-id="0cbc6-128">Restituisce lo spazio di proprietà del database, in pagine (Int32).</span><span class="sxs-lookup"><span data-stu-id="0cbc6-128">Returns the owned space of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0cbc6-129">SpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="0cbc6-129">SpaceAvailable</span></span></td>
<td><span data-ttu-id="0cbc6-130">Restituisce lo spazio disponibile nel database, in pagine (Int32).</span><span class="sxs-lookup"><span data-stu-id="0cbc6-130">Returns the available space in the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0cbc6-131">Varie</span><span class="sxs-lookup"><span data-stu-id="0cbc6-131">Misc</span></span></td>
<td><span data-ttu-id="0cbc6-132">Restituisce un oggetto <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> .</span><span class="sxs-lookup"><span data-stu-id="0cbc6-132">Returns a <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> object.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0cbc6-133">DBInUse</span><span class="sxs-lookup"><span data-stu-id="0cbc6-133">DBInUse</span></span></td>
<td><span data-ttu-id="0cbc6-134">Restituisce un valore booleano che indica se il database è collegato (booleano).</span><span class="sxs-lookup"><span data-stu-id="0cbc6-134">Returns a boolean indicating whether the database is attached (boolean).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0cbc6-135">PageSize</span><span class="sxs-lookup"><span data-stu-id="0cbc6-135">PageSize</span></span></td>
<td><span data-ttu-id="0cbc6-136">Restituisce le dimensioni di pagina del database (Int32).</span><span class="sxs-lookup"><span data-stu-id="0cbc6-136">Returns the page size of the database (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0cbc6-137">FileType</span><span class="sxs-lookup"><span data-stu-id="0cbc6-137">FileType</span></span></td>
<td><span data-ttu-id="0cbc6-138">Restituisce il tipo di database (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span><span class="sxs-lookup"><span data-stu-id="0cbc6-138">Returns the type of the database (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0cbc6-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cbc6-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0cbc6-140">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0cbc6-140">Reference</span></span>

[<span data-ttu-id="0cbc6-141">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0cbc6-141">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
