---
description: 'Altre informazioni su: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: fe3a8ccd813ececcb42388c7d577f78e9055d5b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751375"
---
# <a name="jet_dbid"></a><span data-ttu-id="df011-103">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="df011-103">JET_DBID</span></span>


<span data-ttu-id="df011-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="df011-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbid"></a><span data-ttu-id="df011-105">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="df011-105">JET_DBID</span></span>

<span data-ttu-id="df011-106">Il tipo di dati **JET_DBID** contiene l'handle per il database.</span><span class="sxs-lookup"><span data-stu-id="df011-106">The **JET_DBID** data type contains the handle to the database.</span></span> <span data-ttu-id="df011-107">Per gestire lo schema di un database viene utilizzato un handle di database.</span><span class="sxs-lookup"><span data-stu-id="df011-107">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="df011-108">Può inoltre essere utilizzato per gestire le tabelle all'interno di tale database.</span><span class="sxs-lookup"><span data-stu-id="df011-108">It can also be used to manage the tables inside of that database.</span></span>

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a><span data-ttu-id="df011-109">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="df011-109">Data Types</span></span>

<span data-ttu-id="df011-110">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="df011-110">JET_DBID</span></span>

<span data-ttu-id="df011-111">Handle per il database.</span><span class="sxs-lookup"><span data-stu-id="df011-111">Handle to the database.</span></span>

<span data-ttu-id="df011-112">Il valore JET_dbidNil indica che l'handle non è valido.</span><span class="sxs-lookup"><span data-stu-id="df011-112">A value of JET_dbidNil indicates that the handle is invalid.</span></span>

### <a name="remarks"></a><span data-ttu-id="df011-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="df011-113">Remarks</span></span>

<span data-ttu-id="df011-114">Un handle di database viene creato tramite una chiamata a [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="df011-114">A database handle is created by means of a call to [JetCreateDatabase](./jetcreatedatabase-function.md) or [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

<span data-ttu-id="df011-115">Un handle di database può essere chiuso in modo esplicito da [JetCloseDatabase](./jetclosedatabase-function.md) o chiuso in modo implicito da [JetEndSession](./jetendsession-function.md) o [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="df011-115">A database handle can be explicitly closed by [JetCloseDatabase](./jetclosedatabase-function.md) or implicitly closed by [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="df011-116">Un handle di database può essere utilizzato solo all'interno della sessione in cui è stato creato.</span><span class="sxs-lookup"><span data-stu-id="df011-116">A database handle can be used only within the session in which it was created.</span></span> <span data-ttu-id="df011-117">L'esistenza di un handle di database corrisponde all'apertura logica di un database.</span><span class="sxs-lookup"><span data-stu-id="df011-117">The existence of a database handle corresponds to the logical open of a database.</span></span> <span data-ttu-id="df011-118">Una apertura logica è diversa dall'apertura fisica di un database, che si verifica quando un database viene collegato al sistema.</span><span class="sxs-lookup"><span data-stu-id="df011-118">A logical open is different from the physical open of a database, which happens when a database is attached to the system.</span></span>

### <a name="requirements"></a><span data-ttu-id="df011-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df011-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df011-120"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="df011-120"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="df011-121">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="df011-121">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df011-122"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="df011-122"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="df011-123">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="df011-123">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df011-124"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="df011-124"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="df011-125">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="df011-125">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="df011-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="df011-126">See Also</span></span>

[<span data-ttu-id="df011-127">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="df011-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="df011-128">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="df011-128">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="df011-129">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="df011-129">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="df011-130">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="df011-130">JetEndSession</span></span>](./jetendsession-function.md)
