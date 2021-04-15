---
description: 'Altre informazioni su: metodo API. GetTableColumnid'
title: API. GetTableColumnid, metodo
TOCTitle: 'GetTableColumnid method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumnid(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumnid(v=EXCHG.10)
ms:contentKeyID: 55107215
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec91b014401709b6312b3363d8dae9e7da3d200e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524792"
---
# <a name="apigettablecolumnid-method"></a><span data-ttu-id="a15f0-103">API. GetTableColumnid, metodo</span><span class="sxs-lookup"><span data-stu-id="a15f0-103">Api.GetTableColumnid method</span></span>

<span data-ttu-id="a15f0-104">Ottiene il ColumnID della colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="a15f0-104">Get the columnid of the specified column.</span></span>

<span data-ttu-id="a15f0-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a15f0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a15f0-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a15f0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a15f0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a15f0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumnid ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String _
) As JET_COLUMNID
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim returnValue As JET_COLUMNID

returnValue = Api.GetTableColumnid(sesid, _
    tableid, columnName)
```

``` csharp
public static JET_COLUMNID GetTableColumnid(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName
)
```

#### <a name="parameters"></a><span data-ttu-id="a15f0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a15f0-108">Parameters</span></span>

  - <span data-ttu-id="a15f0-109">sesid</span><span class="sxs-lookup"><span data-stu-id="a15f0-109">sesid</span></span>  
    <span data-ttu-id="a15f0-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a15f0-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a15f0-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="a15f0-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a15f0-112">TableID</span><span class="sxs-lookup"><span data-stu-id="a15f0-112">tableid</span></span>  
    <span data-ttu-id="a15f0-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a15f0-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a15f0-114">Tabella contenente la colonna.</span><span class="sxs-lookup"><span data-stu-id="a15f0-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="a15f0-115">columnName</span><span class="sxs-lookup"><span data-stu-id="a15f0-115">columnName</span></span>  
    <span data-ttu-id="a15f0-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a15f0-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a15f0-117">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="a15f0-117">The name of the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a15f0-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a15f0-118">Return value</span></span>

<span data-ttu-id="a15f0-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a15f0-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
<span data-ttu-id="a15f0-120">ID della colonna.</span><span class="sxs-lookup"><span data-stu-id="a15f0-120">The id of the column.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a15f0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a15f0-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a15f0-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a15f0-122">Reference</span></span>

[<span data-ttu-id="a15f0-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="a15f0-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a15f0-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="a15f0-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a15f0-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a15f0-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
