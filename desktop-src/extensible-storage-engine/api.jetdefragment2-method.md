---
description: 'Altre informazioni su: metodo API. JetDefragment2'
title: API. JetDefragment2, metodo
TOCTitle: 'JetDefragment2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.JET_CALLBACK,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment2(v=EXCHG.10)
ms:contentKeyID: 55100696
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b22c89b304103954a2088bf05ba98797777489be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306308"
---
# <a name="apijetdefragment2-method"></a><span data-ttu-id="529be-103">API. JetDefragment2, metodo</span><span class="sxs-lookup"><span data-stu-id="529be-103">Api.JetDefragment2 method</span></span>

<span data-ttu-id="529be-104">Avvia e arresta le attività di deframmentazione del database che migliorano l'organizzazione dei dati all'interno di un database.</span><span class="sxs-lookup"><span data-stu-id="529be-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="529be-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="529be-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="529be-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="529be-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="529be-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="529be-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment2 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    callback As JET_CALLBACK, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim callback As JET_CALLBACK
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment2(sesid, _
    dbid, tableName, passes, seconds, _
    callback, grbit)
```

``` csharp
public static JET_wrn JetDefragment2(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    JET_CALLBACK callback,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="529be-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="529be-108">Parameters</span></span>

  - <span data-ttu-id="529be-109">sesid</span><span class="sxs-lookup"><span data-stu-id="529be-109">sesid</span></span>  
    <span data-ttu-id="529be-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="529be-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="529be-111">Sessione da utilizzare per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="529be-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="529be-112">dbid</span><span class="sxs-lookup"><span data-stu-id="529be-112">dbid</span></span>  
    <span data-ttu-id="529be-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="529be-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="529be-114">Database da deframmentare.</span><span class="sxs-lookup"><span data-stu-id="529be-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="529be-115">tableName</span><span class="sxs-lookup"><span data-stu-id="529be-115">tableName</span></span>  
    <span data-ttu-id="529be-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="529be-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="529be-117">Parametro non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="529be-117">Unused parameter.</span></span> <span data-ttu-id="529be-118">La deframmentazione viene eseguita per l'intero database descritto dall'ID del database specificato.</span><span class="sxs-lookup"><span data-stu-id="529be-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="529be-119">passa</span><span class="sxs-lookup"><span data-stu-id="529be-119">passes</span></span>  
    <span data-ttu-id="529be-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="529be-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="529be-121">Quando si avvia un'attività di deframmentazione in linea, questo parametro imposta il numero massimo di passaggi di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="529be-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="529be-122">Quando si arresta un'attività di deframmentazione in linea, questo parametro viene impostato sul numero di passaggi eseguiti.</span><span class="sxs-lookup"><span data-stu-id="529be-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="529be-123">secondi</span><span class="sxs-lookup"><span data-stu-id="529be-123">seconds</span></span>  
    <span data-ttu-id="529be-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="529be-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="529be-125">Quando si avvia un'attività di deframmentazione in linea, questo parametro imposta il tempo massimo per la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="529be-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="529be-126">Quando si arresta un'attività di deframmentazione in linea, questo buffer di output viene impostato sul periodo di tempo utilizzato per la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="529be-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="529be-127">callback</span><span class="sxs-lookup"><span data-stu-id="529be-127">callback</span></span>  
    <span data-ttu-id="529be-128">Tipo: [Microsoft.ISAM.esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="529be-128">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="529be-129">Funzione di callback utilizzata da Defrag per segnalare lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="529be-129">Callback function that defrag uses to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="529be-130">grbit</span><span class="sxs-lookup"><span data-stu-id="529be-130">grbit</span></span>  
    <span data-ttu-id="529be-131">Tipo: [Microsoft. ISAM. esent. Interop. DefragGrbit](./defraggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="529be-131">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="529be-132">Opzioni di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="529be-132">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="529be-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="529be-133">Return value</span></span>

<span data-ttu-id="529be-134">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="529be-134">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="529be-135">Codice di avviso.</span><span class="sxs-lookup"><span data-stu-id="529be-135">A warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="529be-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="529be-136">Remarks</span></span>

<span data-ttu-id="529be-137">Il callback passato a JetDefragment2 può essere eseguito in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="529be-137">The callback passed to JetDefragment2 can be executed asynchronously.</span></span> <span data-ttu-id="529be-138">Il Garbage Collector non sa che il codice non gestito ha un riferimento al callback, quindi è importante assicurarsi che il callback non venga raccolto.</span><span class="sxs-lookup"><span data-stu-id="529be-138">The GC doesn't know that the unmanaged code has a reference to the callback so it is important to make sure the callback isn't collected.</span></span>

## <a name="see-also"></a><span data-ttu-id="529be-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="529be-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="529be-140">Riferimento</span><span class="sxs-lookup"><span data-stu-id="529be-140">Reference</span></span>

[<span data-ttu-id="529be-141">Classe API</span><span class="sxs-lookup"><span data-stu-id="529be-141">Api class</span></span>](./api-class.md)

[<span data-ttu-id="529be-142">Membri API</span><span class="sxs-lookup"><span data-stu-id="529be-142">Api members</span></span>](./api-members.md)

[<span data-ttu-id="529be-143">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="529be-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
