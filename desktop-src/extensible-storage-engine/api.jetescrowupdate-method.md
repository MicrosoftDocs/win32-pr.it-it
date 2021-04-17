---
description: 'Altre informazioni su: metodo API. JetEscrowUpdate'
title: API. JetEscrowUpdate, metodo
TOCTitle: 'JetEscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetescrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100740
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 09e74f964fd6018248a3cfc594621bed96f92e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306301"
---
# <a name="apijetescrowupdate-method"></a><span data-ttu-id="860ae-103">API. JetEscrowUpdate, metodo</span><span class="sxs-lookup"><span data-stu-id="860ae-103">Api.JetEscrowUpdate method</span></span>

<span data-ttu-id="860ae-104">Esegue un'operazione di addizione atomica su una colonna.</span><span class="sxs-lookup"><span data-stu-id="860ae-104">Performs an atomic addition operation on one column.</span></span> <span data-ttu-id="860ae-105">Questa funzione consente a più sessioni di aggiornare simultaneamente lo stesso record senza conflitti.</span><span class="sxs-lookup"><span data-stu-id="860ae-105">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span> <span data-ttu-id="860ae-106">Vedere anche [EscrowUpdate (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="860ae-106">Also see [EscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span></span>

<span data-ttu-id="860ae-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="860ae-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="860ae-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="860ae-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="860ae-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="860ae-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Byte(), _
    deltaSize As Integer, _
    previousValue As Byte(), _
    previousValueLength As Integer, _
    <OutAttribute> ByRef actualPreviousValueLength As Integer, _
    grbit As EscrowUpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Byte()
Dim deltaSize As Integer
Dim previousValue As Byte()
Dim previousValueLength As Integer
Dim actualPreviousValueLength As Integer
Dim grbit As EscrowUpdateGrbitApi.JetEscrowUpdate(sesid, tableid, _
    columnid, delta, deltaSize, previousValue, _
    previousValueLength, actualPreviousValueLength, _
    grbit)
```

``` csharp
public static void JetEscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] delta,
    int deltaSize,
    byte[] previousValue,
    int previousValueLength,
    out int actualPreviousValueLength,
    EscrowUpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="860ae-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="860ae-110">Parameters</span></span>

  - <span data-ttu-id="860ae-111">sesid</span><span class="sxs-lookup"><span data-stu-id="860ae-111">sesid</span></span>  
    <span data-ttu-id="860ae-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="860ae-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="860ae-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="860ae-113">The session to use.</span></span> <span data-ttu-id="860ae-114">La sessione deve trovarsi in una transazione.</span><span class="sxs-lookup"><span data-stu-id="860ae-114">The session must be in a transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="860ae-115">TableID</span><span class="sxs-lookup"><span data-stu-id="860ae-115">tableid</span></span>  
    <span data-ttu-id="860ae-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="860ae-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="860ae-117">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="860ae-117">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="860ae-118">columnid</span><span class="sxs-lookup"><span data-stu-id="860ae-118">columnid</span></span>  
    <span data-ttu-id="860ae-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="860ae-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="860ae-120">Colonna da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="860ae-120">The column to update.</span></span> <span data-ttu-id="860ae-121">Deve essere una colonna aggiornabile del deposito.</span><span class="sxs-lookup"><span data-stu-id="860ae-121">This must be an escrow updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="860ae-122">delta</span><span class="sxs-lookup"><span data-stu-id="860ae-122">delta</span></span>  
    <span data-ttu-id="860ae-123">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="860ae-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="860ae-124">Buffer contenente Addend.</span><span class="sxs-lookup"><span data-stu-id="860ae-124">The buffer containing the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="860ae-125">deltaSize</span><span class="sxs-lookup"><span data-stu-id="860ae-125">deltaSize</span></span>  
    <span data-ttu-id="860ae-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="860ae-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="860ae-127">Dimensioni di Addend.</span><span class="sxs-lookup"><span data-stu-id="860ae-127">The size of the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="860ae-128">previousValue</span><span class="sxs-lookup"><span data-stu-id="860ae-128">previousValue</span></span>  
    <span data-ttu-id="860ae-129">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="860ae-129">Type: \[\]</span></span>  
    
    <span data-ttu-id="860ae-130">Buffer di output che riceverà il valore corrente della colonna.</span><span class="sxs-lookup"><span data-stu-id="860ae-130">An output buffer that will recieve the current value of the column.</span></span> <span data-ttu-id="860ae-131">Questo buffer può essere null.</span><span class="sxs-lookup"><span data-stu-id="860ae-131">This buffer can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="860ae-132">previousValueLength</span><span class="sxs-lookup"><span data-stu-id="860ae-132">previousValueLength</span></span>  
    <span data-ttu-id="860ae-133">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="860ae-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="860ae-134">Dimensioni del buffer previousValue.</span><span class="sxs-lookup"><span data-stu-id="860ae-134">The size of the previousValue buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="860ae-135">actualPreviousValueLength</span><span class="sxs-lookup"><span data-stu-id="860ae-135">actualPreviousValueLength</span></span>  
    <span data-ttu-id="860ae-136">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="860ae-136">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="860ae-137">Restituisce le dimensioni effettive di previousValue.</span><span class="sxs-lookup"><span data-stu-id="860ae-137">Returns the actual size of the previousValue.</span></span>

<!-- end list -->

  - <span data-ttu-id="860ae-138">grbit</span><span class="sxs-lookup"><span data-stu-id="860ae-138">grbit</span></span>  
    <span data-ttu-id="860ae-139">Tipo: [Microsoft. ISAM. esent. Interop. EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="860ae-139">Type: [Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="860ae-140">Opzioni di aggiornamento del deposito.</span><span class="sxs-lookup"><span data-stu-id="860ae-140">Escrow update options.</span></span>

## <a name="see-also"></a><span data-ttu-id="860ae-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="860ae-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="860ae-142">Riferimento</span><span class="sxs-lookup"><span data-stu-id="860ae-142">Reference</span></span>

[<span data-ttu-id="860ae-143">Classe API</span><span class="sxs-lookup"><span data-stu-id="860ae-143">Api class</span></span>](./api-class.md)

[<span data-ttu-id="860ae-144">Membri API</span><span class="sxs-lookup"><span data-stu-id="860ae-144">Api members</span></span>](./api-members.md)

[<span data-ttu-id="860ae-145">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="860ae-145">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
