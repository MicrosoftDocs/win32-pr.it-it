---
description: 'Altre informazioni su: metodo API. JetGetLock'
title: API. JetGetLock, metodo
TOCTitle: 'JetGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetlock(v=EXCHG.10)
ms:contentKeyID: 55100732
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8480b6ac2eab84a0299e0bb3d480908e4f646fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878878"
---
# <a name="apijetgetlock-method"></a><span data-ttu-id="b77f7-103">API. JetGetLock, metodo</span><span class="sxs-lookup"><span data-stu-id="b77f7-103">Api.JetGetLock method</span></span>

<span data-ttu-id="b77f7-104">Riservare in modo esplicito la possibilità di aggiornare una riga, un blocco di scrittura o di impedire in modo esplicito l'aggiornamento di una riga da parte di qualsiasi altra sessione, blocco Read.</span><span class="sxs-lookup"><span data-stu-id="b77f7-104">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="b77f7-105">In genere, i blocchi di scrittura di riga vengono acquisiti in modo implicito in seguito all'aggiornamento delle righe.</span><span class="sxs-lookup"><span data-stu-id="b77f7-105">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="b77f7-106">I blocchi di lettura non sono in genere necessari a causa del controllo delle versioni dei record.</span><span class="sxs-lookup"><span data-stu-id="b77f7-106">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="b77f7-107">Tuttavia, in alcuni casi è possibile che una transazione desideri bloccare in modo esplicito una riga per applicare la serializzazione o per assicurarsi che un'operazione successiva venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="b77f7-107">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span>

<span data-ttu-id="b77f7-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b77f7-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b77f7-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b77f7-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b77f7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b77f7-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbitApi.JetGetLock(sesid, tableid, grbit)
```

``` csharp
public static void JetGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b77f7-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b77f7-111">Parameters</span></span>

  - <span data-ttu-id="b77f7-112">sesid</span><span class="sxs-lookup"><span data-stu-id="b77f7-112">sesid</span></span>  
    <span data-ttu-id="b77f7-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b77f7-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b77f7-114">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b77f7-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b77f7-115">TableID</span><span class="sxs-lookup"><span data-stu-id="b77f7-115">tableid</span></span>  
    <span data-ttu-id="b77f7-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b77f7-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b77f7-117">Cursore da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b77f7-117">The cursor to use.</span></span> <span data-ttu-id="b77f7-118">Verrà acquisito un blocco sul record corrente.</span><span class="sxs-lookup"><span data-stu-id="b77f7-118">A lock will be acquired on the current record.</span></span>

<!-- end list -->

  - <span data-ttu-id="b77f7-119">grbit</span><span class="sxs-lookup"><span data-stu-id="b77f7-119">grbit</span></span>  
    <span data-ttu-id="b77f7-120">Tipo: [Microsoft. ISAM. esent. Interop. GetLockGrbit](./getlockgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b77f7-120">Type: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b77f7-121">Opzioni di blocco, utilizzare questa opzione per specificare il tipo di blocco da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b77f7-121">Lock options, use this to specify which type of lock to obtain.</span></span>

## <a name="see-also"></a><span data-ttu-id="b77f7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b77f7-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b77f7-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b77f7-123">Reference</span></span>

[<span data-ttu-id="b77f7-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="b77f7-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b77f7-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="b77f7-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b77f7-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b77f7-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
