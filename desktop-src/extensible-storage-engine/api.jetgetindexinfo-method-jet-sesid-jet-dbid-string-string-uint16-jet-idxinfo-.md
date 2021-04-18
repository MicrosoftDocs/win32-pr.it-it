---
description: 'Altre informazioni su: metodo API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)'
title: Metodo API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.UInt16@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100771
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 762437dba9e502de5c0650e4ae6df53d4629d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306280"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-uint16-jet_idxinfo"></a><span data-ttu-id="06b78-103">Metodo API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="06b78-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</span></span>

<span data-ttu-id="06b78-104">Recupera informazioni sugli indici in una tabella.</span><span class="sxs-lookup"><span data-stu-id="06b78-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="06b78-105">Questa API non è conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="06b78-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="06b78-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="06b78-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="06b78-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="06b78-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="06b78-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06b78-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As UShort, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As UShort
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out ushort result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="06b78-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="06b78-109">Parameters</span></span>

  - <span data-ttu-id="06b78-110">sesid</span><span class="sxs-lookup"><span data-stu-id="06b78-110">sesid</span></span>  
    <span data-ttu-id="06b78-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="06b78-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="06b78-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="06b78-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="06b78-113">dbid</span><span class="sxs-lookup"><span data-stu-id="06b78-113">dbid</span></span>  
    <span data-ttu-id="06b78-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="06b78-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="06b78-115">Database da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="06b78-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="06b78-116">tablename</span><span class="sxs-lookup"><span data-stu-id="06b78-116">tablename</span></span>  
    <span data-ttu-id="06b78-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="06b78-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="06b78-118">Nome della tabella in cui recuperare le informazioni sugli indici.</span><span class="sxs-lookup"><span data-stu-id="06b78-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="06b78-119">IndexName</span><span class="sxs-lookup"><span data-stu-id="06b78-119">indexname</span></span>  
    <span data-ttu-id="06b78-120">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="06b78-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="06b78-121">Nome dell'indice per il quale recuperare informazioni.</span><span class="sxs-lookup"><span data-stu-id="06b78-121">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="06b78-122">result</span><span class="sxs-lookup"><span data-stu-id="06b78-122">result</span></span>  
    <span data-ttu-id="06b78-123">Tipo: [System. UInt16](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="06b78-123">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="06b78-124">Compilato con informazioni sugli indici della tabella.</span><span class="sxs-lookup"><span data-stu-id="06b78-124">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="06b78-125">infoLevel</span><span class="sxs-lookup"><span data-stu-id="06b78-125">infoLevel</span></span>  
    <span data-ttu-id="06b78-126">Tipo: [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="06b78-126">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="06b78-127">Tipo di informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="06b78-127">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="06b78-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06b78-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="06b78-129">Riferimento</span><span class="sxs-lookup"><span data-stu-id="06b78-129">Reference</span></span>

[<span data-ttu-id="06b78-130">Classe API</span><span class="sxs-lookup"><span data-stu-id="06b78-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="06b78-131">Membri API</span><span class="sxs-lookup"><span data-stu-id="06b78-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="06b78-132">Overload JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="06b78-132">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="06b78-133">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="06b78-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
