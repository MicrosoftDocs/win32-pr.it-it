---
description: 'Altre informazioni su: Costruttore tabella'
title: Costruttore di tabella
TOCTitle: 'Table constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.table(v=EXCHG.10)
ms:contentKeyID: 55104142
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8987e643253791e5315dd07b7b20a40dee66cf9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307802"
---
# <a name="table-constructor"></a><span data-ttu-id="0bf7e-103">Costruttore di tabella</span><span class="sxs-lookup"><span data-stu-id="0bf7e-103">Table constructor</span></span>

<span data-ttu-id="0bf7e-104">Inizializza una nuova istanza della classe Table.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-104">Initializes a new instance of the Table class.</span></span> <span data-ttu-id="0bf7e-105">La tabella viene aperta dal database specificato.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-105">The table is opened from the given database.</span></span>

<span data-ttu-id="0bf7e-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0bf7e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0bf7e-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0bf7e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0bf7e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bf7e-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    name As String, _
    grbit As OpenTableGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim name As String
Dim grbit As OpenTableGrbit

Dim instance As New Table(sesid, dbid, _
    name, grbit)
```

``` csharp
public Table(
    JET_SESID sesid,
    JET_DBID dbid,
    string name,
    OpenTableGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0bf7e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0bf7e-109">Parameters</span></span>

  - <span data-ttu-id="0bf7e-110">sesid</span><span class="sxs-lookup"><span data-stu-id="0bf7e-110">sesid</span></span>  
    <span data-ttu-id="0bf7e-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0bf7e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0bf7e-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0bf7e-113">dbid</span><span class="sxs-lookup"><span data-stu-id="0bf7e-113">dbid</span></span>  
    <span data-ttu-id="0bf7e-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0bf7e-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="0bf7e-115">Database in cui aprire la tabella.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-115">The database to open the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="0bf7e-116">name</span><span class="sxs-lookup"><span data-stu-id="0bf7e-116">name</span></span>  
    <span data-ttu-id="0bf7e-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0bf7e-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0bf7e-118">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-118">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="0bf7e-119">grbit</span><span class="sxs-lookup"><span data-stu-id="0bf7e-119">grbit</span></span>  
    <span data-ttu-id="0bf7e-120">Tipo: [Microsoft. ISAM. esent. Interop. OpenTableGrbit](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0bf7e-120">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0bf7e-121">Opzioni di JetOpenTable.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-121">JetOpenTable options.</span></span>

## <a name="see-also"></a><span data-ttu-id="0bf7e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0bf7e-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0bf7e-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0bf7e-123">Reference</span></span>

[<span data-ttu-id="0bf7e-124">Classe Table</span><span class="sxs-lookup"><span data-stu-id="0bf7e-124">Table class</span></span>](./table-class.md)

[<span data-ttu-id="0bf7e-125">Membri della tabella</span><span class="sxs-lookup"><span data-stu-id="0bf7e-125">Table members</span></span>](./table-members.md)

[<span data-ttu-id="0bf7e-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0bf7e-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
