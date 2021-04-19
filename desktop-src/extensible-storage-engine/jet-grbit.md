---
description: 'Altre informazioni su: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323779"
---
# <a name="jet_grbit"></a><span data-ttu-id="ec68b-103">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ec68b-103">JET_GRBIT</span></span>


<span data-ttu-id="ec68b-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ec68b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_grbit"></a><span data-ttu-id="ec68b-105">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ec68b-105">JET_GRBIT</span></span>

<span data-ttu-id="ec68b-106">Il tipo di dati **JET_GRBIT** è costituito da un gruppo di bit che contengono costanti specifiche per le funzioni e le strutture in cui vengono utilizzate.</span><span class="sxs-lookup"><span data-stu-id="ec68b-106">The **JET_GRBIT** data type is a group of bits that contain constants that are specific to the functions and structures in which it is used.</span></span>

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a><span data-ttu-id="ec68b-107">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="ec68b-107">Data Types</span></span>

<span data-ttu-id="ec68b-108">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ec68b-108">JET_GRBIT</span></span>

<span data-ttu-id="ec68b-109">In generale, le costanti utilizzate come valori per questo tipo di dati riflettono il nome dell'elemento API in cui vengono utilizzate.</span><span class="sxs-lookup"><span data-stu-id="ec68b-109">In general, the constants that are used as values for this data type reflect the name of the API element in which they are used.</span></span> <span data-ttu-id="ec68b-110">Ad esempio, tutte le costanti passate a [JetRetrieveColumn](./jetretrievecolumn-function.md) iniziano con "JET_bitRetrieve".</span><span class="sxs-lookup"><span data-stu-id="ec68b-110">For example, all constants passed to [JetRetrieveColumn](./jetretrievecolumn-function.md) begin with "JET_bitRetrieve".</span></span> <span data-ttu-id="ec68b-111">Analogamente, tutte le costanti passate a [JetSetColumn](./jetsetcolumn-function.md) iniziano con "JET_bitSet".</span><span class="sxs-lookup"><span data-stu-id="ec68b-111">Similarly, all constants passed to [JetSetColumn](./jetsetcolumn-function.md) begin with "JET_bitSet".</span></span>

<span data-ttu-id="ec68b-112">Se il valore è zero, il parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ec68b-112">A value of zero causes the parameter to be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="ec68b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec68b-113">Remarks</span></span>

<span data-ttu-id="ec68b-114">Per ulteriori informazioni, vedere la funzione o la struttura specifica.</span><span class="sxs-lookup"><span data-stu-id="ec68b-114">For more information, see the specific function or structure.</span></span> <span data-ttu-id="ec68b-115">Le opzioni vengono in genere passate come un set di flag che possono essere combinati.</span><span class="sxs-lookup"><span data-stu-id="ec68b-115">The options are usually passed as a set of flags that can be combined.</span></span>

### <a name="requirements"></a><span data-ttu-id="ec68b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec68b-116">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec68b-117"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ec68b-117"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ec68b-118">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ec68b-118">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec68b-119"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ec68b-119"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ec68b-120">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ec68b-120">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec68b-121"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ec68b-121"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ec68b-122">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ec68b-122">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ec68b-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ec68b-123">See Also</span></span>

[<span data-ttu-id="ec68b-124">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="ec68b-124">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="ec68b-125">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="ec68b-125">JetSetColumn</span></span>](./jetsetcolumn-function.md)
