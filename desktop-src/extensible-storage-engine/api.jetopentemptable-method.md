---
description: 'Altre informazioni su: metodo API. JetOpenTempTable'
title: API. JetOpenTempTable, metodo
TOCTitle: 'JetOpenTempTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable(v=EXCHG.10)
ms:contentKeyID: 55100773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa41ce62b8bc2d7f2429acb5de809ad0be44a609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318478"
---
# <a name="apijetopentemptable-method"></a><span data-ttu-id="43f8f-103">API. JetOpenTempTable, metodo</span><span class="sxs-lookup"><span data-stu-id="43f8f-103">Api.JetOpenTempTable method</span></span>

<span data-ttu-id="43f8f-104">Crea una tabella temporanea con un solo indice.</span><span class="sxs-lookup"><span data-stu-id="43f8f-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="43f8f-105">Una tabella temporanea archivia e recupera i record esattamente come una tabella ordinaria creata con JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="43f8f-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="43f8f-106">Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile.</span><span class="sxs-lookup"><span data-stu-id="43f8f-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="43f8f-107">Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale.</span><span class="sxs-lookup"><span data-stu-id="43f8f-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="43f8f-108">Vedere anche [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="43f8f-108">Also see [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="43f8f-109">[JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="43f8f-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="43f8f-110">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43f8f-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43f8f-111">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43f8f-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43f8f-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43f8f-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable(sesid, columns, _
    numColumns, grbit, tableid, columnids)
```

``` csharp
public static void JetOpenTempTable(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="43f8f-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="43f8f-113">Parameters</span></span>

  - <span data-ttu-id="43f8f-114">sesid</span><span class="sxs-lookup"><span data-stu-id="43f8f-114">sesid</span></span>  
    <span data-ttu-id="43f8f-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43f8f-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="43f8f-116">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="43f8f-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="43f8f-117">colonne</span><span class="sxs-lookup"><span data-stu-id="43f8f-117">columns</span></span>  
    <span data-ttu-id="43f8f-118">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="43f8f-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="43f8f-119">Definizioni di colonna per le colonne create nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="43f8f-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="43f8f-120">numColumns</span><span class="sxs-lookup"><span data-stu-id="43f8f-120">numColumns</span></span>  
    <span data-ttu-id="43f8f-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="43f8f-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="43f8f-122">Numero di definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="43f8f-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="43f8f-123">grbit</span><span class="sxs-lookup"><span data-stu-id="43f8f-123">grbit</span></span>  
    <span data-ttu-id="43f8f-124">Tipo: [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="43f8f-124">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="43f8f-125">Opzioni per la creazione di tabelle.</span><span class="sxs-lookup"><span data-stu-id="43f8f-125">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="43f8f-126">TableID</span><span class="sxs-lookup"><span data-stu-id="43f8f-126">tableid</span></span>  
    <span data-ttu-id="43f8f-127">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="43f8f-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="43f8f-128">Restituisce il TableID della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="43f8f-128">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="43f8f-129">La chiusura di questo TableID con [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libera le risorse associate alla tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="43f8f-129">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="43f8f-130">columnIDs</span><span class="sxs-lookup"><span data-stu-id="43f8f-130">columnids</span></span>  
    <span data-ttu-id="43f8f-131">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="43f8f-131">Type: \[\]</span></span>  
    
    <span data-ttu-id="43f8f-132">Buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="43f8f-132">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="43f8f-133">Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="43f8f-133">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="43f8f-134">Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione della matrice di input.</span><span class="sxs-lookup"><span data-stu-id="43f8f-134">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="43f8f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43f8f-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43f8f-136">Riferimento</span><span class="sxs-lookup"><span data-stu-id="43f8f-136">Reference</span></span>

[<span data-ttu-id="43f8f-137">Classe API</span><span class="sxs-lookup"><span data-stu-id="43f8f-137">Api class</span></span>](./api-class.md)

[<span data-ttu-id="43f8f-138">Membri API</span><span class="sxs-lookup"><span data-stu-id="43f8f-138">Api members</span></span>](./api-members.md)

[<span data-ttu-id="43f8f-139">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="43f8f-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
