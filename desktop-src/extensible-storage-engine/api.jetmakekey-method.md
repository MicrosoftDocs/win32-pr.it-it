---
description: 'Altre informazioni su: metodo API. JetMakeKey'
title: API. JetMakeKey, metodo
TOCTitle: 'JetMakeKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmakekey(v=EXCHG.10)
ms:contentKeyID: 55100764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13db6e7106f5312e03ffa5acfbd86c72d38c6edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968361"
---
# <a name="apijetmakekey-method"></a><span data-ttu-id="4edc7-103">API. JetMakeKey, metodo</span><span class="sxs-lookup"><span data-stu-id="4edc7-103">Api.JetMakeKey method</span></span>

<span data-ttu-id="4edc7-104">Costruisce chiavi di ricerca che possono essere usate da [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) e [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="4edc7-104">Constructs search keys that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="4edc7-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4edc7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4edc7-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4edc7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4edc7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4edc7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As MakeKeyGrbitApi.JetMakeKey(sesid, tableid, data, _
    dataSize, grbit)
```

``` csharp
public static void JetMakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="4edc7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4edc7-108">Parameters</span></span>

  - <span data-ttu-id="4edc7-109">sesid</span><span class="sxs-lookup"><span data-stu-id="4edc7-109">sesid</span></span>  
    <span data-ttu-id="4edc7-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4edc7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4edc7-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="4edc7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4edc7-112">TableID</span><span class="sxs-lookup"><span data-stu-id="4edc7-112">tableid</span></span>  
    <span data-ttu-id="4edc7-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4edc7-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4edc7-114">Cursore su cui creare la chiave.</span><span class="sxs-lookup"><span data-stu-id="4edc7-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="4edc7-115">data</span><span class="sxs-lookup"><span data-stu-id="4edc7-115">data</span></span>  
    <span data-ttu-id="4edc7-116">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="4edc7-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="4edc7-117">Dati della colonna chiave corrente dell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="4edc7-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="4edc7-118">dataSize</span><span class="sxs-lookup"><span data-stu-id="4edc7-118">dataSize</span></span>  
    <span data-ttu-id="4edc7-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4edc7-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4edc7-120">Dimensione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4edc7-120">Size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="4edc7-121">grbit</span><span class="sxs-lookup"><span data-stu-id="4edc7-121">grbit</span></span>  
    <span data-ttu-id="4edc7-122">Tipo: [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4edc7-122">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4edc7-123">Opzioni chiave.</span><span class="sxs-lookup"><span data-stu-id="4edc7-123">Key options.</span></span>

## <a name="remarks"></a><span data-ttu-id="4edc7-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="4edc7-124">Remarks</span></span>

<span data-ttu-id="4edc7-125">Le funzioni MakeKey forniscono funzionalità chiave specifiche per il tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="4edc7-125">The MakeKey functions provide datatype-specific make key functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="4edc7-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4edc7-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4edc7-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4edc7-127">Reference</span></span>

[<span data-ttu-id="4edc7-128">Classe API</span><span class="sxs-lookup"><span data-stu-id="4edc7-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4edc7-129">Membri API</span><span class="sxs-lookup"><span data-stu-id="4edc7-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4edc7-130">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4edc7-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
