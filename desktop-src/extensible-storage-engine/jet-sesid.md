---
description: 'Altre informazioni su: JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 542802c806bbea55aafb4fc1a0241a92b2842878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878853"
---
# <a name="jet_sesid"></a><span data-ttu-id="6a280-103">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6a280-103">JET_SESID</span></span>


<span data-ttu-id="6a280-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6a280-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_sesid"></a><span data-ttu-id="6a280-105">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6a280-105">JET_SESID</span></span>

<span data-ttu-id="6a280-106">Il tipo di dati **JET_SESID** contiene un handle per la sessione da usare per una chiamata all'API Jet.</span><span class="sxs-lookup"><span data-stu-id="6a280-106">The **JET_SESID** data type contains a handle to the session to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a><span data-ttu-id="6a280-107">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="6a280-107">Data Types</span></span>

<span data-ttu-id="6a280-108">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6a280-108">JET_SESID</span></span>

<span data-ttu-id="6a280-109">È possibile utilizzare **null** o [JET_sesidNil](./invalid-handle-constants.md) per indicare un handle di sessione non valido.</span><span class="sxs-lookup"><span data-stu-id="6a280-109">Either **NULL** or [JET_sesidNil](./invalid-handle-constants.md) can be used to indicate an invalid session handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="6a280-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a280-110">Remarks</span></span>

<span data-ttu-id="6a280-111">Una sessione è il contesto di transazione del motore di database.</span><span class="sxs-lookup"><span data-stu-id="6a280-111">A session is the transaction context of the database engine.</span></span> <span data-ttu-id="6a280-112">Può essere usato per avviare, eseguire il commit o interrompere le transazioni che influiscono sulla visibilità e sulla durabilità delle modifiche apportate da questa o da altre sessioni.</span><span class="sxs-lookup"><span data-stu-id="6a280-112">It can be used to begin, commit, or abort transactions that affect the visibility and durability of changes that are made by this or other sessions.</span></span>

<span data-ttu-id="6a280-113">È possibile avviare una transazione utilizzando [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="6a280-113">A transaction can be started using [JetBeginTransaction](./jetbegintransaction-function.md).</span></span> <span data-ttu-id="6a280-114">È possibile creare una sessione usando [JetBeginSession](./jetbeginsession-function.md).</span><span class="sxs-lookup"><span data-stu-id="6a280-114">A session may be created using [JetBeginSession](./jetbeginsession-function.md).</span></span> <span data-ttu-id="6a280-115">Il numero massimo di sessioni che è possibile creare in qualsiasi momento è controllato da [JET_paramMaxSessions](./resource-parameters.md), che può essere configurato tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="6a280-115">The maximum number of sessions that can be created at any one time is controlled by [JET_paramMaxSessions](./resource-parameters.md), which can be configured by means of [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="6a280-116">Una sessione viene terminata in modo esplicito da una chiamata a [JetEndSession](./jetendsession-function.md) o terminata in modo implicito da una chiamata a [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="6a280-116">A session is explicitly ended by a call to [JetEndSession](./jetendsession-function.md) or implicitly ended by a call to [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="6a280-117">Ogni sessione può essere utilizzata da un solo thread alla volta.</span><span class="sxs-lookup"><span data-stu-id="6a280-117">Each session can only be used by one thread at a time.</span></span> <span data-ttu-id="6a280-118">Inoltre, il comportamento predefinito del motore consiste nel limitare l'uso di una sessione allo stesso thread dal momento in cui la prima chiamata a [JetBeginTransaction](./jetbegintransaction-function.md) viene effettuata fino al momento in cui viene effettuata la chiamata corrispondente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="6a280-118">In addition, the default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to [JetBeginTransaction](./jetbegintransaction-function.md) is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="6a280-119">Questo comportamento può essere modificato per rimuovere la seconda restrizione impostando un contesto di sessione personalizzato usando [JetSetSessionContext](./jetsetsessioncontext-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="6a280-119">This behavior can be changed to remove this second restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="6a280-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a280-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a280-121"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6a280-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6a280-122">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6a280-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a280-123"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6a280-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6a280-124">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6a280-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a280-125"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="6a280-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6a280-126">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="6a280-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="6a280-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6a280-127">See Also</span></span>

[<span data-ttu-id="6a280-128">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="6a280-128">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="6a280-129">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="6a280-129">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="6a280-130">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="6a280-130">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="6a280-131">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="6a280-131">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="6a280-132">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="6a280-132">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="6a280-133">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="6a280-133">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="6a280-134">JetRollback</span><span class="sxs-lookup"><span data-stu-id="6a280-134">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="6a280-135">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="6a280-135">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="6a280-136">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="6a280-136">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="6a280-137">JetTerm</span><span class="sxs-lookup"><span data-stu-id="6a280-137">JetTerm</span></span>](./jetterm-function.md)
