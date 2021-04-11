---
description: 'Altre informazioni su: metodo API. JetDeleteColumn'
title: API. JetDeleteColumn, metodo
TOCTitle: 'JetDeleteColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn(v=EXCHG.10)
ms:contentKeyID: 55100684
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0801ffae0429b0c1d16d452d4170bdc6ce74937f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128718"
---
# <a name="apijetdeletecolumn-method"></a><span data-ttu-id="e3ac8-103">API. JetDeleteColumn, metodo</span><span class="sxs-lookup"><span data-stu-id="e3ac8-103">Api.JetDeleteColumn method</span></span>

<span data-ttu-id="e3ac8-104">Elimina una colonna da una tabella di database.</span><span class="sxs-lookup"><span data-stu-id="e3ac8-104">Deletes a column from a database table.</span></span>

<span data-ttu-id="e3ac8-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e3ac8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e3ac8-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e3ac8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ac8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3ac8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As StringApi.JetDeleteColumn(sesid, tableid, _
    column)
```

``` csharp
public static void JetDeleteColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column
)
```

#### <a name="parameters"></a><span data-ttu-id="e3ac8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3ac8-108">Parameters</span></span>

  - <span data-ttu-id="e3ac8-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e3ac8-109">sesid</span></span>  
    <span data-ttu-id="e3ac8-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e3ac8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e3ac8-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="e3ac8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3ac8-112">TableID</span><span class="sxs-lookup"><span data-stu-id="e3ac8-112">tableid</span></span>  
    <span data-ttu-id="e3ac8-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e3ac8-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e3ac8-114">Cursore della tabella da cui eliminare la colonna.</span><span class="sxs-lookup"><span data-stu-id="e3ac8-114">A cursor on the table to delete the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3ac8-115">colonna</span><span class="sxs-lookup"><span data-stu-id="e3ac8-115">column</span></span>  
    <span data-ttu-id="e3ac8-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e3ac8-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e3ac8-117">Nome della colonna da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e3ac8-117">The name of the column to be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3ac8-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3ac8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e3ac8-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e3ac8-119">Reference</span></span>

[<span data-ttu-id="e3ac8-120">Classe API</span><span class="sxs-lookup"><span data-stu-id="e3ac8-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e3ac8-121">Membri API</span><span class="sxs-lookup"><span data-stu-id="e3ac8-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e3ac8-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e3ac8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
