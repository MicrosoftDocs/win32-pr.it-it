---
description: 'Altre informazioni su: metodo API. JetCreateIndex'
title: API. JetCreateIndex, metodo
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9b3549461324f396408bb7d370531907248e8c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306316"
---
# <a name="apijetcreateindex-method"></a><span data-ttu-id="a901b-103">API. JetCreateIndex, metodo</span><span class="sxs-lookup"><span data-stu-id="a901b-103">Api.JetCreateIndex method</span></span>

<span data-ttu-id="a901b-104">Crea un indice sui dati in un database ESE.</span><span class="sxs-lookup"><span data-stu-id="a901b-104">Creates an index over data in an ESE database.</span></span> <span data-ttu-id="a901b-105">Un indice può essere usato per individuare rapidamente dati specifici.</span><span class="sxs-lookup"><span data-stu-id="a901b-105">An index can be used to locate specific data quickly.</span></span>

<span data-ttu-id="a901b-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a901b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a901b-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a901b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a901b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a901b-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a><span data-ttu-id="a901b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a901b-109">Parameters</span></span>

  - <span data-ttu-id="a901b-110">sesid</span><span class="sxs-lookup"><span data-stu-id="a901b-110">sesid</span></span>  
    <span data-ttu-id="a901b-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a901b-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a901b-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="a901b-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a901b-113">TableID</span><span class="sxs-lookup"><span data-stu-id="a901b-113">tableid</span></span>  
    <span data-ttu-id="a901b-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a901b-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a901b-115">Tabella in cui creare l'indice.</span><span class="sxs-lookup"><span data-stu-id="a901b-115">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="a901b-116">indexName</span><span class="sxs-lookup"><span data-stu-id="a901b-116">indexName</span></span>  
    <span data-ttu-id="a901b-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a901b-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a901b-118">Puntatore a una stringa con terminazione null che specifica il nome dell'indice da creare.</span><span class="sxs-lookup"><span data-stu-id="a901b-118">Pointer to a null-terminated string that specifies the name of the index to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="a901b-119">grbit</span><span class="sxs-lookup"><span data-stu-id="a901b-119">grbit</span></span>  
    <span data-ttu-id="a901b-120">Tipo: [Microsoft. ISAM. esent. Interop. CreateIndexGrbit](./createindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a901b-120">Type: [Microsoft.Isam.Esent.Interop.CreateIndexGrbit](./createindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a901b-121">Opzioni di creazione degli indici.</span><span class="sxs-lookup"><span data-stu-id="a901b-121">Index creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="a901b-122">Descrizione della descrizione</span><span class="sxs-lookup"><span data-stu-id="a901b-122">keyDescription</span></span>  
    <span data-ttu-id="a901b-123">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a901b-123">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a901b-124">Puntatore a una stringa doppia con terminazione null di token delimitati da null.</span><span class="sxs-lookup"><span data-stu-id="a901b-124">Pointer to a double null-terminated string of null-delimited tokens.</span></span>

<!-- end list -->

  - <span data-ttu-id="a901b-125">keyDescriptionLength</span><span class="sxs-lookup"><span data-stu-id="a901b-125">keyDescriptionLength</span></span>  
    <span data-ttu-id="a901b-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a901b-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a901b-127">Lunghezza, in caratteri, di szKey, inclusi i due valori null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="a901b-127">The length, in characters, of szKey including the two terminating nulls.</span></span>

<!-- end list -->

  - <span data-ttu-id="a901b-128">densità</span><span class="sxs-lookup"><span data-stu-id="a901b-128">density</span></span>  
    <span data-ttu-id="a901b-129">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a901b-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a901b-130">Densità iniziale di B + albero.</span><span class="sxs-lookup"><span data-stu-id="a901b-130">Initial B+ tree density.</span></span>

## <a name="see-also"></a><span data-ttu-id="a901b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a901b-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a901b-132">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a901b-132">Reference</span></span>

[<span data-ttu-id="a901b-133">Classe API</span><span class="sxs-lookup"><span data-stu-id="a901b-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a901b-134">Membri API</span><span class="sxs-lookup"><span data-stu-id="a901b-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a901b-135">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a901b-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
