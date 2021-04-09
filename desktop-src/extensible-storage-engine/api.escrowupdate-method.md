---
description: 'Altre informazioni su: metodo API. EscrowUpdate'
title: API. EscrowUpdate, metodo
TOCTitle: 'EscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.EscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.escrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100668
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dde632f01bd7ac9cbdf8bc4dc09e1337f32014b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749506"
---
# <a name="apiescrowupdate-method"></a><span data-ttu-id="7c351-103">API. EscrowUpdate, metodo</span><span class="sxs-lookup"><span data-stu-id="7c351-103">Api.EscrowUpdate method</span></span>

<span data-ttu-id="7c351-104">Eseguire l'aggiunta atomica in una colonna.</span><span class="sxs-lookup"><span data-stu-id="7c351-104">Perform atomic addition on one column.</span></span> <span data-ttu-id="7c351-105">La colonna deve essere di tipo [Long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="7c351-105">The column must be of type [Long](./jet-coltyp-enumeration.md).</span></span> <span data-ttu-id="7c351-106">Questa funzione consente a più sessioni di aggiornare simultaneamente lo stesso record senza conflitti.</span><span class="sxs-lookup"><span data-stu-id="7c351-106">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

<span data-ttu-id="7c351-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7c351-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7c351-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7c351-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7c351-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c351-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function EscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Integer _
) As Integer
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Integer
Dim returnValue As Integer

returnValue = Api.EscrowUpdate(sesid, _
    tableid, columnid, delta)
```

``` csharp
public static int EscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int delta
)
```

#### <a name="parameters"></a><span data-ttu-id="7c351-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c351-110">Parameters</span></span>

  - <span data-ttu-id="7c351-111">sesid</span><span class="sxs-lookup"><span data-stu-id="7c351-111">sesid</span></span>  
    <span data-ttu-id="7c351-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7c351-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7c351-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7c351-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7c351-114">TableID</span><span class="sxs-lookup"><span data-stu-id="7c351-114">tableid</span></span>  
    <span data-ttu-id="7c351-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7c351-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7c351-116">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7c351-116">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="7c351-117">columnid</span><span class="sxs-lookup"><span data-stu-id="7c351-117">columnid</span></span>  
    <span data-ttu-id="7c351-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7c351-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="7c351-119">Colonna da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7c351-119">The column to update.</span></span> <span data-ttu-id="7c351-120">Deve essere una colonna aggiornabile con deposito.</span><span class="sxs-lookup"><span data-stu-id="7c351-120">This must be an escrow-updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="7c351-121">delta</span><span class="sxs-lookup"><span data-stu-id="7c351-121">delta</span></span>  
    <span data-ttu-id="7c351-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7c351-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7c351-123">Delta da applicare alla colonna.</span><span class="sxs-lookup"><span data-stu-id="7c351-123">The delta to apply to the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7c351-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c351-124">Return value</span></span>

<span data-ttu-id="7c351-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7c351-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="7c351-126">Il valore corrente della colonna archiviato nel database (il controllo delle versioni viene ignorato).</span><span class="sxs-lookup"><span data-stu-id="7c351-126">The current value of the column as stored in the database (versioning is ignored).</span></span>  

## <a name="remarks"></a><span data-ttu-id="7c351-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c351-127">Remarks</span></span>

<span data-ttu-id="7c351-128">Questo metodo esegue il wrapping di [JetEscrowUpdate (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, \[ \] , Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="7c351-128">This method wraps [JetEscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, \[\], Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7c351-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c351-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7c351-130">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7c351-130">Reference</span></span>

[<span data-ttu-id="7c351-131">Classe API</span><span class="sxs-lookup"><span data-stu-id="7c351-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7c351-132">Membri API</span><span class="sxs-lookup"><span data-stu-id="7c351-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7c351-133">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7c351-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
