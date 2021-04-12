---
description: 'Altre informazioni su: metodo API. JetOpenDatabase'
title: API. JetOpenDatabase, metodo
TOCTitle: 'JetOpenDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopendatabase(v=EXCHG.10)
ms:contentKeyID: 55100768
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: faaff0eec2b5bc8a2c2f2a72a61f9f6a23f7d972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233789"
---
# <a name="apijetopendatabase-method"></a><span data-ttu-id="aa5ab-103">API. JetOpenDatabase, metodo</span><span class="sxs-lookup"><span data-stu-id="aa5ab-103">Api.JetOpenDatabase method</span></span>

<span data-ttu-id="aa5ab-104">Apre un database precedentemente associato a [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md)per l'utilizzo con una sessione di database.</span><span class="sxs-lookup"><span data-stu-id="aa5ab-104">Opens a database previously attached with [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md), for use with a database session.</span></span> <span data-ttu-id="aa5ab-105">Questa funzione può essere chiamata più volte per lo stesso database.</span><span class="sxs-lookup"><span data-stu-id="aa5ab-105">This function can be called multiple times for the same database.</span></span>

<span data-ttu-id="aa5ab-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aa5ab-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aa5ab-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aa5ab-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aa5ab-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa5ab-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetOpenDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As OpenDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As OpenDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetOpenDatabase(sesid, _
    database, connect, dbid, grbit)
```

``` csharp
public static JET_wrn JetOpenDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    OpenDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="aa5ab-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa5ab-109">Parameters</span></span>

  - <span data-ttu-id="aa5ab-110">sesid</span><span class="sxs-lookup"><span data-stu-id="aa5ab-110">sesid</span></span>  
    <span data-ttu-id="aa5ab-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aa5ab-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="aa5ab-112">Sessione in cui è in corso l'apertura del database.</span><span class="sxs-lookup"><span data-stu-id="aa5ab-112">The session that is opening the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="aa5ab-113">database</span><span class="sxs-lookup"><span data-stu-id="aa5ab-113">database</span></span>  
    <span data-ttu-id="aa5ab-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="aa5ab-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="aa5ab-115">Database da aprire.</span><span class="sxs-lookup"><span data-stu-id="aa5ab-115">The database to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="aa5ab-116">connessione</span><span class="sxs-lookup"><span data-stu-id="aa5ab-116">connect</span></span>  
    <span data-ttu-id="aa5ab-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="aa5ab-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="aa5ab-118">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="aa5ab-118">Reserved for future use.</span></span>

<!-- end list -->

  - <span data-ttu-id="aa5ab-119">dbid</span><span class="sxs-lookup"><span data-stu-id="aa5ab-119">dbid</span></span>  
    <span data-ttu-id="aa5ab-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aa5ab-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="aa5ab-121">Restituisce l'dbid del database collegato.</span><span class="sxs-lookup"><span data-stu-id="aa5ab-121">Returns the dbid of the attached database.</span></span>

<!-- end list -->

  - <span data-ttu-id="aa5ab-122">grbit</span><span class="sxs-lookup"><span data-stu-id="aa5ab-122">grbit</span></span>  
    <span data-ttu-id="aa5ab-123">Tipo: [Microsoft. ISAM. esent. Interop. OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="aa5ab-123">Type: [Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="aa5ab-124">Opzioni di database aperte.</span><span class="sxs-lookup"><span data-stu-id="aa5ab-124">Open database options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="aa5ab-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa5ab-125">Return value</span></span>

<span data-ttu-id="aa5ab-126">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="aa5ab-126">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="aa5ab-127">Codice di avviso ESENT.</span><span class="sxs-lookup"><span data-stu-id="aa5ab-127">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aa5ab-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa5ab-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aa5ab-129">Riferimento</span><span class="sxs-lookup"><span data-stu-id="aa5ab-129">Reference</span></span>

[<span data-ttu-id="aa5ab-130">Classe API</span><span class="sxs-lookup"><span data-stu-id="aa5ab-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="aa5ab-131">Membri API</span><span class="sxs-lookup"><span data-stu-id="aa5ab-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="aa5ab-132">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="aa5ab-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
