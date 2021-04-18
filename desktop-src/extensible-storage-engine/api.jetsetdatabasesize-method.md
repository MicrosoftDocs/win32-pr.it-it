---
description: 'Altre informazioni su: metodo API. JetSetDatabaseSize'
title: API. JetSetDatabaseSize, metodo
TOCTitle: 'JetSetDatabaseSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetdatabasesize(v=EXCHG.10)
ms:contentKeyID: 55100807
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetDatabaseSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c90ba5ef2ebc96cbe6d50fa6c0888db9a09a0a99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315718"
---
# <a name="apijetsetdatabasesize-method"></a><span data-ttu-id="21221-103">API. JetSetDatabaseSize, metodo</span><span class="sxs-lookup"><span data-stu-id="21221-103">Api.JetSetDatabaseSize method</span></span>

<span data-ttu-id="21221-104">Imposta la dimensione di un file di database non aperto.</span><span class="sxs-lookup"><span data-stu-id="21221-104">Sets the size of an unopened database file.</span></span>

<span data-ttu-id="21221-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="21221-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="21221-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="21221-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="21221-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21221-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetDatabaseSize ( _
    sesid As JET_SESID, _
    database As String, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim desiredPages As Integer
Dim actualPages As IntegerApi.JetSetDatabaseSize(sesid, database, _
    desiredPages, actualPages)
```

``` csharp
public static void JetSetDatabaseSize(
    JET_SESID sesid,
    string database,
    int desiredPages,
    out int actualPages
)
```

#### <a name="parameters"></a><span data-ttu-id="21221-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="21221-108">Parameters</span></span>

  - <span data-ttu-id="21221-109">sesid</span><span class="sxs-lookup"><span data-stu-id="21221-109">sesid</span></span>  
    <span data-ttu-id="21221-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="21221-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="21221-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="21221-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="21221-112">database</span><span class="sxs-lookup"><span data-stu-id="21221-112">database</span></span>  
    <span data-ttu-id="21221-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="21221-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="21221-114">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="21221-114">The name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="21221-115">desiredPages</span><span class="sxs-lookup"><span data-stu-id="21221-115">desiredPages</span></span>  
    <span data-ttu-id="21221-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="21221-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="21221-117">Dimensioni desiderate del database, in pagine.</span><span class="sxs-lookup"><span data-stu-id="21221-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="21221-118">actualPages</span><span class="sxs-lookup"><span data-stu-id="21221-118">actualPages</span></span>  
    <span data-ttu-id="21221-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="21221-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="21221-120">Dimensioni del database, in pagine, dopo la chiamata a.</span><span class="sxs-lookup"><span data-stu-id="21221-120">The size of the database, in pages, after the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="21221-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21221-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="21221-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="21221-122">Reference</span></span>

[<span data-ttu-id="21221-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="21221-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="21221-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="21221-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="21221-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="21221-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
