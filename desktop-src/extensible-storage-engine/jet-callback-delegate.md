---
description: 'Altre informazioni su: JET_CALLBACK delegate'
title: Delegato JET_CALLBACK
TOCTitle: JET_CALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_callback(v=EXCHG.10)
ms:contentKeyID: 39515752
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK..ctor
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.Invoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 617cbefba047f822b338627a782be7e016c2a16f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317398"
---
# <a name="jet_callback-delegate"></a><span data-ttu-id="bf4f1-103">Delegato JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="bf4f1-103">JET_CALLBACK delegate</span></span>

<span data-ttu-id="bf4f1-104">Funzione di callback multifunzione utilizzata dal motore di database per informare l'applicazione di un evento che implica la deframmentazione in linea e le notifiche dello stato del cursore.</span><span class="sxs-lookup"><span data-stu-id="bf4f1-104">A multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="bf4f1-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bf4f1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bf4f1-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bf4f1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bf4f1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf4f1-107">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_CALLBACK ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    arg1 As Object, _
    arg2 As Object, _
    context As IntPtr, _
    unused As IntPtr _
) As JET_err
'Usage
Dim instance As New JET_CALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_CALLBACK(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    Object arg1,
    Object arg2,
    IntPtr context,
    IntPtr unused
)
```

#### <a name="parameters"></a><span data-ttu-id="bf4f1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf4f1-108">Parameters</span></span>

  - <span data-ttu-id="bf4f1-109">sesid</span><span class="sxs-lookup"><span data-stu-id="bf4f1-109">sesid</span></span>  
    <span data-ttu-id="bf4f1-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bf4f1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bf4f1-111">Sessione per cui viene eseguito il callback.</span><span class="sxs-lookup"><span data-stu-id="bf4f1-111">The session for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf4f1-112">dbid</span><span class="sxs-lookup"><span data-stu-id="bf4f1-112">dbid</span></span>  
    <span data-ttu-id="bf4f1-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bf4f1-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="bf4f1-114">Database per il quale viene eseguito il callback.</span><span class="sxs-lookup"><span data-stu-id="bf4f1-114">The database for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf4f1-115">TableID</span><span class="sxs-lookup"><span data-stu-id="bf4f1-115">tableid</span></span>  
    <span data-ttu-id="bf4f1-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bf4f1-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bf4f1-117">Cursore per il quale viene eseguito il callback.</span><span class="sxs-lookup"><span data-stu-id="bf4f1-117">The cursor for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf4f1-118">cbtyp</span><span class="sxs-lookup"><span data-stu-id="bf4f1-118">cbtyp</span></span>  
    <span data-ttu-id="bf4f1-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bf4f1-119">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="bf4f1-120">Operazione per la quale viene eseguito il callback.</span><span class="sxs-lookup"><span data-stu-id="bf4f1-120">The operation for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf4f1-121">arg1</span><span class="sxs-lookup"><span data-stu-id="bf4f1-121">arg1</span></span>  
    <span data-ttu-id="bf4f1-122">Tipo: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="bf4f1-122">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="bf4f1-123">Primo argomento specifico della richiamata.</span><span class="sxs-lookup"><span data-stu-id="bf4f1-123">First callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf4f1-124">arg2</span><span class="sxs-lookup"><span data-stu-id="bf4f1-124">arg2</span></span>  
    <span data-ttu-id="bf4f1-125">Tipo: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="bf4f1-125">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="bf4f1-126">Secondo argomento specifico della richiamata.</span><span class="sxs-lookup"><span data-stu-id="bf4f1-126">Second callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf4f1-127">contesto</span><span class="sxs-lookup"><span data-stu-id="bf4f1-127">context</span></span>  
    <span data-ttu-id="bf4f1-128">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="bf4f1-128">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="bf4f1-129">Contesto di callback.</span><span class="sxs-lookup"><span data-stu-id="bf4f1-129">Callback context.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf4f1-130">unused</span><span class="sxs-lookup"><span data-stu-id="bf4f1-130">unused</span></span>  
    <span data-ttu-id="bf4f1-131">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="bf4f1-131">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="bf4f1-132">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="bf4f1-132">This parameter is not used.</span></span>

#### <a name="return-value"></a><span data-ttu-id="bf4f1-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf4f1-133">Return value</span></span>

<span data-ttu-id="bf4f1-134">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bf4f1-134">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="bf4f1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf4f1-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bf4f1-136">Riferimento</span><span class="sxs-lookup"><span data-stu-id="bf4f1-136">Reference</span></span>

[<span data-ttu-id="bf4f1-137">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="bf4f1-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
