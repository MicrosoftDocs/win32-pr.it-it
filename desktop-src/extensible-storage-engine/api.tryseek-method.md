---
description: 'Altre informazioni su: metodo API. TrySeek'
title: API. TrySeek, metodo
TOCTitle: 'TrySeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryseek(v=EXCHG.10)
ms:contentKeyID: 55100941
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46472c59c14bd515e744a7ccfa908752783d27fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878866"
---
# <a name="apitryseek-method"></a><span data-ttu-id="79836-103">API. TrySeek, metodo</span><span class="sxs-lookup"><span data-stu-id="79836-103">Api.TrySeek method</span></span>

<span data-ttu-id="79836-104">Posiziona in modo efficiente un cursore in una voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca in tale cursore e alla disuguaglianza specificata.</span><span class="sxs-lookup"><span data-stu-id="79836-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="79836-105">È necessario che una chiave di ricerca sia stata costruita in precedenza usando JetMakeKey.</span><span class="sxs-lookup"><span data-stu-id="79836-105">A search key must have been previously constructed using JetMakeKey.</span></span>

<span data-ttu-id="79836-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="79836-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="79836-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="79836-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="79836-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79836-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As Boolean

returnValue = Api.TrySeek(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="79836-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="79836-109">Parameters</span></span>

  - <span data-ttu-id="79836-110">sesid</span><span class="sxs-lookup"><span data-stu-id="79836-110">sesid</span></span>  
    <span data-ttu-id="79836-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79836-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="79836-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="79836-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="79836-113">TableID</span><span class="sxs-lookup"><span data-stu-id="79836-113">tableid</span></span>  
    <span data-ttu-id="79836-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79836-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="79836-115">Cursore da posizionare.</span><span class="sxs-lookup"><span data-stu-id="79836-115">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="79836-116">grbit</span><span class="sxs-lookup"><span data-stu-id="79836-116">grbit</span></span>  
    <span data-ttu-id="79836-117">Tipo: [Microsoft. ISAM. esent. Interop. SeekGrbit](./seekgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="79836-117">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="79836-118">Opzione Seek.</span><span class="sxs-lookup"><span data-stu-id="79836-118">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="79836-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79836-119">Return value</span></span>

<span data-ttu-id="79836-120">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="79836-120">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="79836-121">True se è stato trovato un record corrispondente ai criteri.</span><span class="sxs-lookup"><span data-stu-id="79836-121">True if a record matching the criteria was found.</span></span>  

## <a name="see-also"></a><span data-ttu-id="79836-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79836-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="79836-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="79836-123">Reference</span></span>

[<span data-ttu-id="79836-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="79836-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="79836-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="79836-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="79836-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="79836-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
