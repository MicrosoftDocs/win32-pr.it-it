---
description: 'Altre informazioni su: metodo API. JetGrowDatabase'
title: API. JetGrowDatabase, metodo
TOCTitle: 'JetGrowDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgrowdatabase(v=EXCHG.10)
ms:contentKeyID: 55100754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGrowDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a51f0d55187b6f6eac66c0cba2ec7b9daa7d1dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879869"
---
# <a name="apijetgrowdatabase-method"></a><span data-ttu-id="8ed15-103">API. JetGrowDatabase, metodo</span><span class="sxs-lookup"><span data-stu-id="8ed15-103">Api.JetGrowDatabase method</span></span>

<span data-ttu-id="8ed15-104">Estende le dimensioni di un database attualmente aperto.</span><span class="sxs-lookup"><span data-stu-id="8ed15-104">Extends the size of a database that is currently open.</span></span>

<span data-ttu-id="8ed15-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8ed15-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8ed15-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8ed15-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed15-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ed15-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGrowDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetGrowDatabase(sesid, dbid, _
    desiredPages, actualPages)
```

``` csharp
public static void JetGrowDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a><span data-ttu-id="8ed15-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ed15-108">Parameters</span></span>

  - <span data-ttu-id="8ed15-109">sesid</span><span class="sxs-lookup"><span data-stu-id="8ed15-109">sesid</span></span>  
    <span data-ttu-id="8ed15-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8ed15-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8ed15-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="8ed15-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ed15-112">dbid</span><span class="sxs-lookup"><span data-stu-id="8ed15-112">dbid</span></span>  
    <span data-ttu-id="8ed15-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8ed15-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="8ed15-114">Database da incrementare.</span><span class="sxs-lookup"><span data-stu-id="8ed15-114">The database to grow.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ed15-115">desiredPages</span><span class="sxs-lookup"><span data-stu-id="8ed15-115">desiredPages</span></span>  
    <span data-ttu-id="8ed15-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8ed15-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8ed15-117">Dimensioni desiderate del database, in pagine.</span><span class="sxs-lookup"><span data-stu-id="8ed15-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ed15-118">actualPages</span><span class="sxs-lookup"><span data-stu-id="8ed15-118">actualPages</span></span>  
    <span data-ttu-id="8ed15-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8ed15-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8ed15-120">Dimensioni del database, in pagine, dopo la chiamata a.</span><span class="sxs-lookup"><span data-stu-id="8ed15-120">The size of the database, in pages, after the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ed15-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ed15-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8ed15-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8ed15-122">Reference</span></span>

[<span data-ttu-id="8ed15-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="8ed15-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8ed15-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="8ed15-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8ed15-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8ed15-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
