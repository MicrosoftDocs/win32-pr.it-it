---
description: 'Altre informazioni su: metodo API. JetDefragment'
title: API. JetDefragment, metodo
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69428d785bf9d607199cb62bfe02d2e373e7dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306310"
---
# <a name="apijetdefragment-method"></a><span data-ttu-id="621b8-103">API. JetDefragment, metodo</span><span class="sxs-lookup"><span data-stu-id="621b8-103">Api.JetDefragment method</span></span>

<span data-ttu-id="621b8-104">Avvia e arresta le attività di deframmentazione del database che migliorano l'organizzazione dei dati all'interno di un database.</span><span class="sxs-lookup"><span data-stu-id="621b8-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="621b8-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="621b8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="621b8-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="621b8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="621b8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="621b8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="621b8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="621b8-108">Parameters</span></span>

  - <span data-ttu-id="621b8-109">sesid</span><span class="sxs-lookup"><span data-stu-id="621b8-109">sesid</span></span>  
    <span data-ttu-id="621b8-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="621b8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="621b8-111">Sessione da utilizzare per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="621b8-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="621b8-112">dbid</span><span class="sxs-lookup"><span data-stu-id="621b8-112">dbid</span></span>  
    <span data-ttu-id="621b8-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="621b8-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="621b8-114">Database da deframmentare.</span><span class="sxs-lookup"><span data-stu-id="621b8-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="621b8-115">tableName</span><span class="sxs-lookup"><span data-stu-id="621b8-115">tableName</span></span>  
    <span data-ttu-id="621b8-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="621b8-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="621b8-117">Parametro non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="621b8-117">Unused parameter.</span></span> <span data-ttu-id="621b8-118">La deframmentazione viene eseguita per l'intero database descritto dall'ID del database specificato.</span><span class="sxs-lookup"><span data-stu-id="621b8-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="621b8-119">passa</span><span class="sxs-lookup"><span data-stu-id="621b8-119">passes</span></span>  
    <span data-ttu-id="621b8-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="621b8-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="621b8-121">Quando si avvia un'attività di deframmentazione in linea, questo parametro imposta il numero massimo di passaggi di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="621b8-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="621b8-122">Quando si arresta un'attività di deframmentazione in linea, questo parametro viene impostato sul numero di passaggi eseguiti.</span><span class="sxs-lookup"><span data-stu-id="621b8-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="621b8-123">secondi</span><span class="sxs-lookup"><span data-stu-id="621b8-123">seconds</span></span>  
    <span data-ttu-id="621b8-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="621b8-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="621b8-125">Quando si avvia un'attività di deframmentazione in linea, questo parametro imposta il tempo massimo per la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="621b8-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="621b8-126">Quando si arresta un'attività di deframmentazione in linea, questo buffer di output viene impostato sul periodo di tempo utilizzato per la deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="621b8-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="621b8-127">grbit</span><span class="sxs-lookup"><span data-stu-id="621b8-127">grbit</span></span>  
    <span data-ttu-id="621b8-128">Tipo: [Microsoft. ISAM. esent. Interop. DefragGrbit](./defraggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="621b8-128">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="621b8-129">Opzioni di deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="621b8-129">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="621b8-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="621b8-130">Return value</span></span>

<span data-ttu-id="621b8-131">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="621b8-131">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="621b8-132">Codice di avviso.</span><span class="sxs-lookup"><span data-stu-id="621b8-132">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="621b8-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="621b8-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="621b8-134">Riferimento</span><span class="sxs-lookup"><span data-stu-id="621b8-134">Reference</span></span>

[<span data-ttu-id="621b8-135">Classe API</span><span class="sxs-lookup"><span data-stu-id="621b8-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="621b8-136">Membri API</span><span class="sxs-lookup"><span data-stu-id="621b8-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="621b8-137">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="621b8-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
