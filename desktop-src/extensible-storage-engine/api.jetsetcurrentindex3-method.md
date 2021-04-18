---
description: 'Altre informazioni su: metodo API. JetSetCurrentIndex3'
title: API. JetSetCurrentIndex3, metodo
TOCTitle: 'JetSetCurrentIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex3(v=EXCHG.10)
ms:contentKeyID: 55100805
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c56f259a35026bb47a5e58b7b364b52d9bedbc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314093"
---
# <a name="apijetsetcurrentindex3-method"></a><span data-ttu-id="a146f-103">API. JetSetCurrentIndex3, metodo</span><span class="sxs-lookup"><span data-stu-id="a146f-103">Api.JetSetCurrentIndex3 method</span></span>

<span data-ttu-id="a146f-104">Imposta l'indice corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="a146f-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="a146f-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a146f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a146f-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a146f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a146f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a146f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex3 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex3(sesid, _
    tableid, index, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex3(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="a146f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a146f-108">Parameters</span></span>

  - <span data-ttu-id="a146f-109">sesid</span><span class="sxs-lookup"><span data-stu-id="a146f-109">sesid</span></span>  
    <span data-ttu-id="a146f-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a146f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a146f-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="a146f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a146f-112">TableID</span><span class="sxs-lookup"><span data-stu-id="a146f-112">tableid</span></span>  
    <span data-ttu-id="a146f-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a146f-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a146f-114">Cursore su cui impostare l'indice.</span><span class="sxs-lookup"><span data-stu-id="a146f-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="a146f-115">indice</span><span class="sxs-lookup"><span data-stu-id="a146f-115">index</span></span>  
    <span data-ttu-id="a146f-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a146f-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a146f-117">Nome dell'indice da selezionare.</span><span class="sxs-lookup"><span data-stu-id="a146f-117">The name of the index to be selected.</span></span> <span data-ttu-id="a146f-118">Se è null o vuoto, verrà selezionato l'indice primario.</span><span class="sxs-lookup"><span data-stu-id="a146f-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="a146f-119">grbit</span><span class="sxs-lookup"><span data-stu-id="a146f-119">grbit</span></span>  
    <span data-ttu-id="a146f-120">Tipo: [Microsoft. ISAM. esent. Interop. SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a146f-120">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a146f-121">Impostare le opzioni relative agli indici.</span><span class="sxs-lookup"><span data-stu-id="a146f-121">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="a146f-122">itagSequence</span><span class="sxs-lookup"><span data-stu-id="a146f-122">itagSequence</span></span>  
    <span data-ttu-id="a146f-123">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a146f-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a146f-124">Numero di sequenza del valore della colonna multivalore che verrà utilizzato per posizionare il cursore sul nuovo indice.</span><span class="sxs-lookup"><span data-stu-id="a146f-124">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="a146f-125">Questo parametro viene usato solo in combinazione con [nomove](./setcurrentindexgrbit-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="a146f-125">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="a146f-126">Se questo parametro non è presente o è impostato su zero, il relativo valore si presume essere 1.</span><span class="sxs-lookup"><span data-stu-id="a146f-126">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="a146f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a146f-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a146f-128">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a146f-128">Reference</span></span>

[<span data-ttu-id="a146f-129">Classe API</span><span class="sxs-lookup"><span data-stu-id="a146f-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a146f-130">Membri API</span><span class="sxs-lookup"><span data-stu-id="a146f-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a146f-131">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a146f-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
