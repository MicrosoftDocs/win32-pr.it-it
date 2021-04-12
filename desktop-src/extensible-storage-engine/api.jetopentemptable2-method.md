---
description: 'Altre informazioni su: metodo API. JetOpenTempTable2'
title: API. JetOpenTempTable2, metodo
TOCTitle: 'JetOpenTempTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable2(v=EXCHG.10)
ms:contentKeyID: 55100777
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fd3f0e04db6519fbcaa1c2d2fa9060d2d993d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233784"
---
# <a name="apijetopentemptable2-method"></a><span data-ttu-id="01597-103">API. JetOpenTempTable2, metodo</span><span class="sxs-lookup"><span data-stu-id="01597-103">Api.JetOpenTempTable2 method</span></span>

<span data-ttu-id="01597-104">Crea una tabella temporanea con un solo indice.</span><span class="sxs-lookup"><span data-stu-id="01597-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="01597-105">Una tabella temporanea archivia e recupera i record esattamente come una tabella ordinaria creata con JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="01597-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="01597-106">Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile.</span><span class="sxs-lookup"><span data-stu-id="01597-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="01597-107">Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale.</span><span class="sxs-lookup"><span data-stu-id="01597-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="01597-108">Vedere anche [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="01597-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="01597-109">[JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="01597-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="01597-110">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="01597-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="01597-111">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="01597-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="01597-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01597-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable2 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    lcid As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim lcid As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable2(sesid, columns, _
    numColumns, lcid, grbit, tableid, _
    columnids)
```

``` csharp
public static void JetOpenTempTable2(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    int lcid,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="01597-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="01597-113">Parameters</span></span>

  - <span data-ttu-id="01597-114">sesid</span><span class="sxs-lookup"><span data-stu-id="01597-114">sesid</span></span>  
    <span data-ttu-id="01597-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="01597-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="01597-116">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="01597-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="01597-117">colonne</span><span class="sxs-lookup"><span data-stu-id="01597-117">columns</span></span>  
    <span data-ttu-id="01597-118">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="01597-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="01597-119">Definizioni di colonna per le colonne create nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="01597-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="01597-120">numColumns</span><span class="sxs-lookup"><span data-stu-id="01597-120">numColumns</span></span>  
    <span data-ttu-id="01597-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="01597-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="01597-122">Numero di definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="01597-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="01597-123">lcid</span><span class="sxs-lookup"><span data-stu-id="01597-123">lcid</span></span>  
    <span data-ttu-id="01597-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="01597-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="01597-125">ID delle impostazioni locali da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="01597-125">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="01597-126">Le impostazioni locali possono essere usate purché nel computer sia installato il Language Pack appropriato.</span><span class="sxs-lookup"><span data-stu-id="01597-126">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span>

<!-- end list -->

  - <span data-ttu-id="01597-127">grbit</span><span class="sxs-lookup"><span data-stu-id="01597-127">grbit</span></span>  
    <span data-ttu-id="01597-128">Tipo: [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="01597-128">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="01597-129">Opzioni per la creazione di tabelle.</span><span class="sxs-lookup"><span data-stu-id="01597-129">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="01597-130">TableID</span><span class="sxs-lookup"><span data-stu-id="01597-130">tableid</span></span>  
    <span data-ttu-id="01597-131">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="01597-131">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="01597-132">Restituisce il TableID della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="01597-132">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="01597-133">La chiusura di questo TableID con [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libera le risorse associate alla tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="01597-133">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="01597-134">columnIDs</span><span class="sxs-lookup"><span data-stu-id="01597-134">columnids</span></span>  
    <span data-ttu-id="01597-135">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="01597-135">Type: \[\]</span></span>  
    
    <span data-ttu-id="01597-136">Buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="01597-136">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="01597-137">Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="01597-137">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="01597-138">Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione della matrice di input.</span><span class="sxs-lookup"><span data-stu-id="01597-138">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="01597-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01597-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="01597-140">Riferimento</span><span class="sxs-lookup"><span data-stu-id="01597-140">Reference</span></span>

[<span data-ttu-id="01597-141">Classe API</span><span class="sxs-lookup"><span data-stu-id="01597-141">Api class</span></span>](./api-class.md)

[<span data-ttu-id="01597-142">Membri API</span><span class="sxs-lookup"><span data-stu-id="01597-142">Api members</span></span>](./api-members.md)

[<span data-ttu-id="01597-143">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="01597-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
