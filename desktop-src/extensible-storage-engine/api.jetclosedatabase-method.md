---
description: 'Altre informazioni su: metodo API. JetCloseDatabase'
title: API. JetCloseDatabase, metodo
TOCTitle: 'JetCloseDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.CloseDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosedatabase(v=EXCHG.10)
ms:contentKeyID: 55100662
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b39d830c34f2d772730d7ea1c65ec4adf3c3d4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525644"
---
# <a name="apijetclosedatabase-method"></a><span data-ttu-id="62174-103">API. JetCloseDatabase, metodo</span><span class="sxs-lookup"><span data-stu-id="62174-103">Api.JetCloseDatabase method</span></span>

<span data-ttu-id="62174-104">Chiude un file di database precedentemente aperto con [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md) o creato con [JetCreateDatabase (JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="62174-104">Closes a database file that was previously opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md) or created with [JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span></span>

<span data-ttu-id="62174-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="62174-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="62174-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="62174-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="62174-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62174-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    grbit As CloseDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim grbit As CloseDatabaseGrbitApi.JetCloseDatabase(sesid, dbid, _
    grbit)
```

``` csharp
public static void JetCloseDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    CloseDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="62174-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="62174-108">Parameters</span></span>

  - <span data-ttu-id="62174-109">sesid</span><span class="sxs-lookup"><span data-stu-id="62174-109">sesid</span></span>  
    <span data-ttu-id="62174-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="62174-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="62174-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="62174-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="62174-112">dbid</span><span class="sxs-lookup"><span data-stu-id="62174-112">dbid</span></span>  
    <span data-ttu-id="62174-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="62174-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="62174-114">Database da chiudere.</span><span class="sxs-lookup"><span data-stu-id="62174-114">The database to close.</span></span>

<!-- end list -->

  - <span data-ttu-id="62174-115">grbit</span><span class="sxs-lookup"><span data-stu-id="62174-115">grbit</span></span>  
    <span data-ttu-id="62174-116">Tipo: [Microsoft. ISAM. esent. Interop. CloseDatabaseGrbit](./closedatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="62174-116">Type: [Microsoft.Isam.Esent.Interop.CloseDatabaseGrbit](./closedatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="62174-117">Opzioni di chiusura.</span><span class="sxs-lookup"><span data-stu-id="62174-117">Close options.</span></span>

## <a name="see-also"></a><span data-ttu-id="62174-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62174-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="62174-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="62174-119">Reference</span></span>

[<span data-ttu-id="62174-120">Classe API</span><span class="sxs-lookup"><span data-stu-id="62174-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="62174-121">Membri API</span><span class="sxs-lookup"><span data-stu-id="62174-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="62174-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="62174-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
