---
description: 'Altre informazioni su: metodo API. JetSetCurrentIndex4'
title: API. JetSetCurrentIndex4, metodo
TOCTitle: 'JetSetCurrentIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex4(v=EXCHG.10)
ms:contentKeyID: 55100806
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2b9319554b998175b3f533c6cd5f4c2d05ba02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306266"
---
# <a name="apijetsetcurrentindex4-method"></a><span data-ttu-id="b34ab-103">API. JetSetCurrentIndex4, metodo</span><span class="sxs-lookup"><span data-stu-id="b34ab-103">Api.JetSetCurrentIndex4 method</span></span>

<span data-ttu-id="b34ab-104">Imposta l'indice corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="b34ab-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="b34ab-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b34ab-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b34ab-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b34ab-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b34ab-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b34ab-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    indexid As JET_INDEXID, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim indexid As JET_INDEXID
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex4(sesid, _
    tableid, index, indexid, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    JET_INDEXID indexid,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="b34ab-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b34ab-108">Parameters</span></span>

  - <span data-ttu-id="b34ab-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b34ab-109">sesid</span></span>  
    <span data-ttu-id="b34ab-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b34ab-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b34ab-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b34ab-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b34ab-112">TableID</span><span class="sxs-lookup"><span data-stu-id="b34ab-112">tableid</span></span>  
    <span data-ttu-id="b34ab-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b34ab-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b34ab-114">Cursore su cui impostare l'indice.</span><span class="sxs-lookup"><span data-stu-id="b34ab-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="b34ab-115">indice</span><span class="sxs-lookup"><span data-stu-id="b34ab-115">index</span></span>  
    <span data-ttu-id="b34ab-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b34ab-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b34ab-117">Nome dell'indice da selezionare.</span><span class="sxs-lookup"><span data-stu-id="b34ab-117">The name of the index to be selected.</span></span> <span data-ttu-id="b34ab-118">Se è null o vuoto, verrà selezionato l'indice primario.</span><span class="sxs-lookup"><span data-stu-id="b34ab-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="b34ab-119">indexid</span><span class="sxs-lookup"><span data-stu-id="b34ab-119">indexid</span></span>  
    <span data-ttu-id="b34ab-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b34ab-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="b34ab-121">ID dell'indice da selezionare.</span><span class="sxs-lookup"><span data-stu-id="b34ab-121">The id of the index to select.</span></span> <span data-ttu-id="b34ab-122">Questo ID può essere ottenuto tramite JetGetIndexInfo o JetGetTableIndexInfo con l'opzione [indexid](./jet-idxinfo-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="b34ab-122">This id can be obtained using JetGetIndexInfo or JetGetTableIndexInfo with the [IndexId](./jet-idxinfo-enumeration.md) option.</span></span>

<!-- end list -->

  - <span data-ttu-id="b34ab-123">grbit</span><span class="sxs-lookup"><span data-stu-id="b34ab-123">grbit</span></span>  
    <span data-ttu-id="b34ab-124">Tipo: [Microsoft. ISAM. esent. Interop. SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b34ab-124">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b34ab-125">Impostare le opzioni relative agli indici.</span><span class="sxs-lookup"><span data-stu-id="b34ab-125">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="b34ab-126">itagSequence</span><span class="sxs-lookup"><span data-stu-id="b34ab-126">itagSequence</span></span>  
    <span data-ttu-id="b34ab-127">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b34ab-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b34ab-128">Numero di sequenza del valore della colonna multivalore che verrà utilizzato per posizionare il cursore sul nuovo indice.</span><span class="sxs-lookup"><span data-stu-id="b34ab-128">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="b34ab-129">Questo parametro viene usato solo in combinazione con [nomove](./setcurrentindexgrbit-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="b34ab-129">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="b34ab-130">Se questo parametro non è presente o è impostato su zero, il relativo valore si presume essere 1.</span><span class="sxs-lookup"><span data-stu-id="b34ab-130">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="b34ab-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b34ab-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b34ab-132">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b34ab-132">Reference</span></span>

[<span data-ttu-id="b34ab-133">Classe API</span><span class="sxs-lookup"><span data-stu-id="b34ab-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b34ab-134">Membri API</span><span class="sxs-lookup"><span data-stu-id="b34ab-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b34ab-135">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b34ab-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
