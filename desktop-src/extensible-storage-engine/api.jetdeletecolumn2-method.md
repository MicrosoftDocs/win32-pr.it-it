---
description: 'Altre informazioni su: metodo API. JetDeleteColumn2'
title: API. JetDeleteColumn2, metodo
TOCTitle: 'JetDeleteColumn2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.DeleteColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn2(v=EXCHG.10)
ms:contentKeyID: 55100680
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0426ca2557dac11c565211162438db6d5c77a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306307"
---
# <a name="apijetdeletecolumn2-method"></a><span data-ttu-id="f8c75-103">API. JetDeleteColumn2, metodo</span><span class="sxs-lookup"><span data-stu-id="f8c75-103">Api.JetDeleteColumn2 method</span></span>

<span data-ttu-id="f8c75-104">Elimina una colonna da una tabella di database.</span><span class="sxs-lookup"><span data-stu-id="f8c75-104">Deletes a column from a database table.</span></span>

<span data-ttu-id="f8c75-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8c75-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8c75-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8c75-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c75-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8c75-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteColumn2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    grbit As DeleteColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim grbit As DeleteColumnGrbitApi.JetDeleteColumn2(sesid, tableid, _
    column, grbit)
```

``` csharp
public static void JetDeleteColumn2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    DeleteColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f8c75-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8c75-108">Parameters</span></span>

  - <span data-ttu-id="f8c75-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f8c75-109">sesid</span></span>  
    <span data-ttu-id="f8c75-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8c75-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f8c75-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f8c75-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8c75-112">TableID</span><span class="sxs-lookup"><span data-stu-id="f8c75-112">tableid</span></span>  
    <span data-ttu-id="f8c75-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8c75-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f8c75-114">Cursore della tabella da cui eliminare la colonna.</span><span class="sxs-lookup"><span data-stu-id="f8c75-114">A cursor on the table to delete the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8c75-115">colonna</span><span class="sxs-lookup"><span data-stu-id="f8c75-115">column</span></span>  
    <span data-ttu-id="f8c75-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f8c75-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f8c75-117">Nome della colonna da eliminare.</span><span class="sxs-lookup"><span data-stu-id="f8c75-117">The name of the column to be deleted.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8c75-118">grbit</span><span class="sxs-lookup"><span data-stu-id="f8c75-118">grbit</span></span>  
    <span data-ttu-id="f8c75-119">Tipo: [Microsoft. ISAM. esent. Interop. DeleteColumnGrbit](./deletecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f8c75-119">Type: [Microsoft.Isam.Esent.Interop.DeleteColumnGrbit](./deletecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f8c75-120">Opzioni di eliminazione della colonna.</span><span class="sxs-lookup"><span data-stu-id="f8c75-120">Column deletion options.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8c75-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8c75-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8c75-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f8c75-122">Reference</span></span>

[<span data-ttu-id="f8c75-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="f8c75-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f8c75-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="f8c75-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f8c75-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f8c75-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
