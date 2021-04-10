---
description: 'Altre informazioni su: Costruttore ColumnStream'
title: Costruttore ColumnStream
TOCTitle: 'ColumnStream constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 498fed2daf2cad5903d9597689a80eadca7bd569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966908"
---
# <a name="columnstream-constructor"></a><span data-ttu-id="c9818-103">Costruttore ColumnStream</span><span class="sxs-lookup"><span data-stu-id="c9818-103">ColumnStream constructor</span></span>

<span data-ttu-id="c9818-104">Inizializza una nuova istanza della classe ColumnStream.</span><span class="sxs-lookup"><span data-stu-id="c9818-104">Initializes a new instance of the ColumnStream class.</span></span>

<span data-ttu-id="c9818-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c9818-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c9818-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c9818-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c9818-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9818-107">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID

Dim instance As New ColumnStream(sesid, tableid, _
    columnid)
```

``` csharp
public ColumnStream(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="c9818-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9818-108">Parameters</span></span>

  - <span data-ttu-id="c9818-109">sesid</span><span class="sxs-lookup"><span data-stu-id="c9818-109">sesid</span></span>  
    <span data-ttu-id="c9818-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c9818-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c9818-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c9818-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9818-112">TableID</span><span class="sxs-lookup"><span data-stu-id="c9818-112">tableid</span></span>  
    <span data-ttu-id="c9818-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c9818-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c9818-114">Cursore da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c9818-114">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9818-115">columnid</span><span class="sxs-lookup"><span data-stu-id="c9818-115">columnid</span></span>  
    <span data-ttu-id="c9818-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c9818-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="c9818-117">ColumnID della colonna da cui impostare o recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="c9818-117">The columnid of the column to set/retrieve data from.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9818-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9818-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c9818-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c9818-119">Reference</span></span>

[<span data-ttu-id="c9818-120">Classe ColumnStream</span><span class="sxs-lookup"><span data-stu-id="c9818-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="c9818-121">Membri di ColumnStream</span><span class="sxs-lookup"><span data-stu-id="c9818-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="c9818-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c9818-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
