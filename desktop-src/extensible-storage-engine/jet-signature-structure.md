---
description: 'Altre informazioni su: struttura JET_SIGNATURE'
title: Struttura JET_SIGNATURE
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: d6210853e22fda5085980c2fb285411ba431bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308023"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="568ec-103">Struttura JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="568ec-103">JET_SIGNATURE Structure</span></span>


<span data-ttu-id="568ec-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="568ec-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_signature-structure"></a><span data-ttu-id="568ec-105">Struttura JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="568ec-105">JET_SIGNATURE Structure</span></span>

<span data-ttu-id="568ec-106">La struttura **JET_SIGNATURE** contiene informazioni che identificano in modo univoco un database.</span><span class="sxs-lookup"><span data-stu-id="568ec-106">The **JET_SIGNATURE** structure contains information that uniquely identifies a database.</span></span>

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a><span data-ttu-id="568ec-107">Membri</span><span class="sxs-lookup"><span data-stu-id="568ec-107">Members</span></span>

<span data-ttu-id="568ec-108">**ulRandom**</span><span class="sxs-lookup"><span data-stu-id="568ec-108">**ulRandom**</span></span>

<span data-ttu-id="568ec-109">Numero assegnato in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="568ec-109">A randomly assigned number.</span></span>

<span data-ttu-id="568ec-110">**logtimeCreate**</span><span class="sxs-lookup"><span data-stu-id="568ec-110">**logtimeCreate**</span></span>

<span data-ttu-id="568ec-111">Il [JET_LOGTIME](./jet-logtime-structure.md) al momento dell'esecuzione di [JetCreateDatabase](./jetcreatedatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="568ec-111">The [JET_LOGTIME](./jet-logtime-structure.md) at the time of [JetCreateDatabase](./jetcreatedatabase-function.md) is executed.</span></span>

<span data-ttu-id="568ec-112">**szComputerName**</span><span class="sxs-lookup"><span data-stu-id="568ec-112">**szComputerName**</span></span>

<span data-ttu-id="568ec-113">Valore stringa facoltativo del nome NetBIOS per il computer.</span><span class="sxs-lookup"><span data-stu-id="568ec-113">The optional string value of the NetBIOS name for the computer.</span></span> <span data-ttu-id="568ec-114">Questo valore non può essere impostato.</span><span class="sxs-lookup"><span data-stu-id="568ec-114">This value may not be set.</span></span>

### <a name="remarks"></a><span data-ttu-id="568ec-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="568ec-115">Remarks</span></span>

<span data-ttu-id="568ec-116">Questo può essere trovato come elemento di [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span><span class="sxs-lookup"><span data-stu-id="568ec-116">This can be found as an element of [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="568ec-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="568ec-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="568ec-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="568ec-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="568ec-119">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="568ec-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="568ec-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="568ec-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="568ec-121">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="568ec-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="568ec-122"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="568ec-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="568ec-123">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="568ec-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="568ec-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="568ec-124">See Also</span></span>

[<span data-ttu-id="568ec-125">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="568ec-125">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="568ec-126">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="568ec-126">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="568ec-127">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="568ec-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)
