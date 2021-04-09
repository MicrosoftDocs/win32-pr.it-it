---
description: 'Altre informazioni su: metodo API. JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)'
title: Metodo API. JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int64@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100700
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc036a1c1eceedd39fd265bcf85a2dbaf779a432
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128699"
---
# <a name="apijetgetdatabasefileinfo-method-string-int64-jet_dbinfo"></a><span data-ttu-id="4dd7c-103">Metodo API. JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="4dd7c-103">Api.JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)</span></span>

<span data-ttu-id="4dd7c-104">Recupera determinate informazioni sul database specificato.</span><span class="sxs-lookup"><span data-stu-id="4dd7c-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="4dd7c-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4dd7c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4dd7c-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4dd7c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd7c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4dd7c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Long, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Long
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out long value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="4dd7c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4dd7c-108">Parameters</span></span>

  - <span data-ttu-id="4dd7c-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="4dd7c-109">databaseName</span></span>  
    <span data-ttu-id="4dd7c-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4dd7c-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4dd7c-111">Nome file del database.</span><span class="sxs-lookup"><span data-stu-id="4dd7c-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="4dd7c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd7c-112">value</span></span>  
    <span data-ttu-id="4dd7c-113">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="4dd7c-113">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="4dd7c-114">Valore da recuperare.</span><span class="sxs-lookup"><span data-stu-id="4dd7c-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="4dd7c-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="4dd7c-115">infoLevel</span></span>  
    <span data-ttu-id="4dd7c-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4dd7c-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="4dd7c-117">Dati specifici da recuperare.</span><span class="sxs-lookup"><span data-stu-id="4dd7c-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="4dd7c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4dd7c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4dd7c-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4dd7c-119">Reference</span></span>

[<span data-ttu-id="4dd7c-120">Classe API</span><span class="sxs-lookup"><span data-stu-id="4dd7c-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4dd7c-121">Membri API</span><span class="sxs-lookup"><span data-stu-id="4dd7c-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4dd7c-122">Overload JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="4dd7c-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="4dd7c-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4dd7c-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
