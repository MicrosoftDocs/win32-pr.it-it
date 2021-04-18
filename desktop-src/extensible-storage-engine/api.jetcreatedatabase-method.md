---
description: 'Altre informazioni su: metodo API. JetCreateDatabase'
title: API. JetCreateDatabase, metodo
TOCTitle: 'JetCreateDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase(v=EXCHG.10)
ms:contentKeyID: 55100748
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe427c270baf8a6d05e5d0ae99e1dc393208da01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306317"
---
# <a name="apijetcreatedatabase-method"></a><span data-ttu-id="5d7c1-103">API. JetCreateDatabase, metodo</span><span class="sxs-lookup"><span data-stu-id="5d7c1-103">Api.JetCreateDatabase method</span></span>

<span data-ttu-id="5d7c1-104">Crea e connette un file di database.</span><span class="sxs-lookup"><span data-stu-id="5d7c1-104">Creates and attaches a database file.</span></span>

<span data-ttu-id="5d7c1-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5d7c1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5d7c1-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5d7c1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7c1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d7c1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase(sesid, database, _
    connect, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5d7c1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d7c1-108">Parameters</span></span>

  - <span data-ttu-id="5d7c1-109">sesid</span><span class="sxs-lookup"><span data-stu-id="5d7c1-109">sesid</span></span>  
    <span data-ttu-id="5d7c1-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5d7c1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5d7c1-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="5d7c1-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d7c1-112">database</span><span class="sxs-lookup"><span data-stu-id="5d7c1-112">database</span></span>  
    <span data-ttu-id="5d7c1-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5d7c1-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5d7c1-114">Percorso del file di database da creare.</span><span class="sxs-lookup"><span data-stu-id="5d7c1-114">The path to the database file to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d7c1-115">connessione</span><span class="sxs-lookup"><span data-stu-id="5d7c1-115">connect</span></span>  
    <span data-ttu-id="5d7c1-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5d7c1-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5d7c1-117">Il parametro non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="5d7c1-117">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d7c1-118">dbid</span><span class="sxs-lookup"><span data-stu-id="5d7c1-118">dbid</span></span>  
    <span data-ttu-id="5d7c1-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5d7c1-119">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="5d7c1-120">Restituisce l'dbid del nuovo database.</span><span class="sxs-lookup"><span data-stu-id="5d7c1-120">Returns the dbid of the new database.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d7c1-121">grbit</span><span class="sxs-lookup"><span data-stu-id="5d7c1-121">grbit</span></span>  
    <span data-ttu-id="5d7c1-122">Tipo: [Microsoft. ISAM. esent. Interop. CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5d7c1-122">Type: [Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5d7c1-123">Opzioni di creazione del database.</span><span class="sxs-lookup"><span data-stu-id="5d7c1-123">Database creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d7c1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d7c1-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5d7c1-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="5d7c1-125">Reference</span></span>

[<span data-ttu-id="5d7c1-126">Classe API</span><span class="sxs-lookup"><span data-stu-id="5d7c1-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5d7c1-127">Membri API</span><span class="sxs-lookup"><span data-stu-id="5d7c1-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5d7c1-128">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5d7c1-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
