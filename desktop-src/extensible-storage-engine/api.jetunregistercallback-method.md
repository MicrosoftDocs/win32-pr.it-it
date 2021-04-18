---
description: 'Altre informazioni su: metodo API. JetUnregisterCallback'
title: API. JetUnregisterCallback, metodo
TOCTitle: 'JetUnregisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUnregisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetunregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100812
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetUnregisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUnregisterCallback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: db3f4a26803242f4ac9d3cb1de09805f9dd57012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308587"
---
# <a name="apijetunregistercallback-method"></a><span data-ttu-id="f9485-103">API. JetUnregisterCallback, metodo</span><span class="sxs-lookup"><span data-stu-id="f9485-103">Api.JetUnregisterCallback method</span></span>

<span data-ttu-id="f9485-104">Configura il motore di database per arrestare l'invio di notifiche all'applicazione come richiesto in precedenza tramite [JetRegisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)](./api.jetregistercallback-method.md).</span><span class="sxs-lookup"><span data-stu-id="f9485-104">Configures the database engine to stop issuing notifications to the application as previously requested through [JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)](./api.jetregistercallback-method.md).</span></span>

<span data-ttu-id="f9485-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f9485-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f9485-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f9485-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f9485-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9485-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUnregisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callbackId As JET_HANDLEApi.JetUnregisterCallback(sesid, _
    tableid, cbtyp, callbackId)
```

``` csharp
public static void JetUnregisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_HANDLE callbackId
)
```

#### <a name="parameters"></a><span data-ttu-id="f9485-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9485-108">Parameters</span></span>

  - <span data-ttu-id="f9485-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f9485-109">sesid</span></span>  
    <span data-ttu-id="f9485-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f9485-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f9485-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f9485-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f9485-112">TableID</span><span class="sxs-lookup"><span data-stu-id="f9485-112">tableid</span></span>  
    <span data-ttu-id="f9485-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f9485-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f9485-114">Cursore aperto nella tabella in cui deve essere registrata la richiamata.</span><span class="sxs-lookup"><span data-stu-id="f9485-114">A cursor opened on the table that the callback should be registered on.</span></span>

<!-- end list -->

  - <span data-ttu-id="f9485-115">cbtyp</span><span class="sxs-lookup"><span data-stu-id="f9485-115">cbtyp</span></span>  
    <span data-ttu-id="f9485-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f9485-116">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="f9485-117">I motivi di callback per i quali l'applicazione non desidera più ricevere le notifiche.</span><span class="sxs-lookup"><span data-stu-id="f9485-117">The callback reasons for which the application no longer wishes to receive notifications.</span></span>

<!-- end list -->

  - <span data-ttu-id="f9485-118">callbackId</span><span class="sxs-lookup"><span data-stu-id="f9485-118">callbackId</span></span>  
    <span data-ttu-id="f9485-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f9485-119">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="f9485-120">Handle del callback registrato restituito da [JetRegisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)](./api.jetregistercallback-method.md).</span><span class="sxs-lookup"><span data-stu-id="f9485-120">The handle of the registered callback that was returned by [JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)](./api.jetregistercallback-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f9485-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9485-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f9485-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f9485-122">Reference</span></span>

[<span data-ttu-id="f9485-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="f9485-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f9485-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="f9485-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f9485-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f9485-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
