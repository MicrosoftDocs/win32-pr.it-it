---
description: 'Altre informazioni su: metodo API. JetBeginSession'
title: API. JetBeginSession, metodo
TOCTitle: 'JetBeginSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginSession(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID@,System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbeginsession(v=EXCHG.10)
ms:contentKeyID: 55107223
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39174c27043f62de4c1a78685876e79de513b804
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128055"
---
# <a name="apijetbeginsession-method"></a><span data-ttu-id="b9727-103">API. JetBeginSession, metodo</span><span class="sxs-lookup"><span data-stu-id="b9727-103">Api.JetBeginSession method</span></span>

<span data-ttu-id="b9727-104">Inizializzare una nuova sessione ESENT.</span><span class="sxs-lookup"><span data-stu-id="b9727-104">Initialize a new ESENT session.</span></span>

<span data-ttu-id="b9727-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b9727-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b9727-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b9727-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b9727-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9727-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginSession ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef sesid As JET_SESID, _
    username As String, _
    password As String _
)
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim username As String
Dim password As StringApi.JetBeginSession(instance, sesid, _
    username, password)
```

``` csharp
public static void JetBeginSession(
    JET_INSTANCE instance,
    out JET_SESID sesid,
    string username,
    string password
)
```

#### <a name="parameters"></a><span data-ttu-id="b9727-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9727-108">Parameters</span></span>

  - <span data-ttu-id="b9727-109">instance</span><span class="sxs-lookup"><span data-stu-id="b9727-109">instance</span></span>  
    <span data-ttu-id="b9727-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b9727-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="b9727-111">Istanza inizializzata in cui creare la sessione.</span><span class="sxs-lookup"><span data-stu-id="b9727-111">The initialized instance to create the session in.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9727-112">sesid</span><span class="sxs-lookup"><span data-stu-id="b9727-112">sesid</span></span>  
    <span data-ttu-id="b9727-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b9727-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b9727-114">Restituisce la sessione creata.</span><span class="sxs-lookup"><span data-stu-id="b9727-114">Returns the created session.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9727-115">username</span><span class="sxs-lookup"><span data-stu-id="b9727-115">username</span></span>  
    <span data-ttu-id="b9727-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b9727-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b9727-117">Il parametro non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b9727-117">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9727-118">password</span><span class="sxs-lookup"><span data-stu-id="b9727-118">password</span></span>  
    <span data-ttu-id="b9727-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b9727-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b9727-120">Il parametro non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b9727-120">The parameter is not used.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9727-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9727-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b9727-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b9727-122">Reference</span></span>

[<span data-ttu-id="b9727-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="b9727-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b9727-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="b9727-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b9727-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b9727-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
