---
description: 'Altre informazioni su: metodo API. JetRenameTable'
title: API. JetRenameTable, metodo
TOCTitle: 'JetRenameTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRenameTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrenametable(v=EXCHG.10)
ms:contentKeyID: 55100788
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRenameTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRenameTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bb108498501df50a43964f5b069860d10c39258
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049410"
---
# <a name="apijetrenametable-method"></a><span data-ttu-id="2c087-103">API. JetRenameTable, metodo</span><span class="sxs-lookup"><span data-stu-id="2c087-103">Api.JetRenameTable method</span></span>

<span data-ttu-id="2c087-104">Modifica il nome di una tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="2c087-104">Changes the name of an existing table.</span></span>

<span data-ttu-id="2c087-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2c087-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2c087-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2c087-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2c087-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c087-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRenameTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    newTableName As String _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim newTableName As StringApi.JetRenameTable(sesid, dbid, _
    tableName, newTableName)
```

``` csharp
public static void JetRenameTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string newTableName
)
```

#### <a name="parameters"></a><span data-ttu-id="2c087-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c087-108">Parameters</span></span>

  - <span data-ttu-id="2c087-109">sesid</span><span class="sxs-lookup"><span data-stu-id="2c087-109">sesid</span></span>  
    <span data-ttu-id="2c087-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2c087-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2c087-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="2c087-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2c087-112">dbid</span><span class="sxs-lookup"><span data-stu-id="2c087-112">dbid</span></span>  
    <span data-ttu-id="2c087-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2c087-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="2c087-114">Database contenente la tabella.</span><span class="sxs-lookup"><span data-stu-id="2c087-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="2c087-115">tableName</span><span class="sxs-lookup"><span data-stu-id="2c087-115">tableName</span></span>  
    <span data-ttu-id="2c087-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2c087-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2c087-117">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="2c087-117">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="2c087-118">newTableName</span><span class="sxs-lookup"><span data-stu-id="2c087-118">newTableName</span></span>  
    <span data-ttu-id="2c087-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2c087-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2c087-120">Nuovo nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="2c087-120">The new name of the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c087-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c087-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2c087-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2c087-122">Reference</span></span>

[<span data-ttu-id="2c087-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="2c087-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2c087-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="2c087-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2c087-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2c087-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
