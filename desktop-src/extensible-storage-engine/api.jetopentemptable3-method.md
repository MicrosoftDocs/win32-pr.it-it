---
description: 'Altre informazioni su: metodo API. JetOpenTempTable3'
title: Metodo Api.JetOpenTempTable3
TOCTitle: 'JetOpenTempTable3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable3(v=EXCHG.10)
ms:contentKeyID: 55100774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e88b5413492c0ae00ed41e569afb49ca6c18e51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318477"
---
# <a name="apijetopentemptable3-method"></a><span data-ttu-id="cef72-103">Metodo Api.JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="cef72-103">Api.JetOpenTempTable3 method</span></span>

<span data-ttu-id="cef72-104">Crea una tabella temporanea con un solo indice.</span><span class="sxs-lookup"><span data-stu-id="cef72-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="cef72-105">Una tabella temporanea archivia e recupera i record esattamente come una tabella ordinaria creata con JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="cef72-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="cef72-106">Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile.</span><span class="sxs-lookup"><span data-stu-id="cef72-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="cef72-107">Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale.</span><span class="sxs-lookup"><span data-stu-id="cef72-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="cef72-108">Vedere anche [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="cef72-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="cef72-109">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cef72-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cef72-110">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cef72-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cef72-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cef72-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable3 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    unicodeindex As JET_UNICODEINDEX, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim unicodeindex As JET_UNICODEINDEX
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable3(sesid, columns, _
    numColumns, unicodeindex, grbit, _
    tableid, columnids)
```

``` csharp
public static void JetOpenTempTable3(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    JET_UNICODEINDEX unicodeindex,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="cef72-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="cef72-112">Parameters</span></span>

  - <span data-ttu-id="cef72-113">sesid</span><span class="sxs-lookup"><span data-stu-id="cef72-113">sesid</span></span>  
    <span data-ttu-id="cef72-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cef72-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cef72-115">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="cef72-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cef72-116">colonne</span><span class="sxs-lookup"><span data-stu-id="cef72-116">columns</span></span>  
    <span data-ttu-id="cef72-117">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="cef72-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="cef72-118">Definizioni di colonna per le colonne create nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="cef72-118">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="cef72-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="cef72-119">numColumns</span></span>  
    <span data-ttu-id="cef72-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="cef72-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="cef72-121">Numero di definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="cef72-121">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="cef72-122">unicodeindex</span><span class="sxs-lookup"><span data-stu-id="cef72-122">unicodeindex</span></span>  
    <span data-ttu-id="cef72-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="cef72-123">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  
    
    <span data-ttu-id="cef72-124">ID delle impostazioni locali e flag di normalizzazione che verranno utilizzati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="cef72-124">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="cef72-125">Quando non è presente, vengono usate le opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="cef72-125">When this is not present then the default options are used.</span></span>

<!-- end list -->

  - <span data-ttu-id="cef72-126">grbit</span><span class="sxs-lookup"><span data-stu-id="cef72-126">grbit</span></span>  
    <span data-ttu-id="cef72-127">Tipo: [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="cef72-127">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="cef72-128">Opzioni per la creazione di tabelle.</span><span class="sxs-lookup"><span data-stu-id="cef72-128">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="cef72-129">TableID</span><span class="sxs-lookup"><span data-stu-id="cef72-129">tableid</span></span>  
    <span data-ttu-id="cef72-130">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cef72-130">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="cef72-131">Restituisce il TableID della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="cef72-131">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="cef72-132">La chiusura di questo TableID con [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libera le risorse associate alla tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="cef72-132">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="cef72-133">columnIDs</span><span class="sxs-lookup"><span data-stu-id="cef72-133">columnids</span></span>  
    <span data-ttu-id="cef72-134">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="cef72-134">Type: \[\]</span></span>  
    
    <span data-ttu-id="cef72-135">Buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="cef72-135">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="cef72-136">Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="cef72-136">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="cef72-137">Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione della matrice di input.</span><span class="sxs-lookup"><span data-stu-id="cef72-137">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="cef72-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cef72-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cef72-139">Riferimento</span><span class="sxs-lookup"><span data-stu-id="cef72-139">Reference</span></span>

[<span data-ttu-id="cef72-140">Classe API</span><span class="sxs-lookup"><span data-stu-id="cef72-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cef72-141">Membri API</span><span class="sxs-lookup"><span data-stu-id="cef72-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cef72-142">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cef72-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
