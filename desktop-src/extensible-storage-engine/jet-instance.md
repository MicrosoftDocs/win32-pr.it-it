---
description: 'Altre informazioni su: JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: 6e1fde3e01c8328d2fdaf6609c6772fda9cd1428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968051"
---
# <a name="jet_instance"></a><span data-ttu-id="31105-103">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="31105-103">JET_INSTANCE</span></span>


<span data-ttu-id="31105-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="31105-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance"></a><span data-ttu-id="31105-105">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="31105-105">JET_INSTANCE</span></span>

<span data-ttu-id="31105-106">Il tipo di dati **JET_INSTANCE** contiene un handle per l'istanza del database da usare per una chiamata all'API Jet.</span><span class="sxs-lookup"><span data-stu-id="31105-106">The **JET_INSTANCE** data type contains a handle to the instance of the database to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a><span data-ttu-id="31105-107">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="31105-107">Data Types</span></span>

<span data-ttu-id="31105-108">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="31105-108">JET_INSTANCE</span></span>

<span data-ttu-id="31105-109">È possibile utilizzare **null** o [JET_instanceNil](./invalid-handle-constants.md) per indicare un handle di istanza non valido.</span><span class="sxs-lookup"><span data-stu-id="31105-109">Either **NULL** or [JET_instanceNil](./invalid-handle-constants.md) can be used to indicate an invalid instance handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="31105-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="31105-110">Remarks</span></span>

<span data-ttu-id="31105-111">Questo handle viene ottenuto quando si crea un'istanza del database chiamando le funzioni [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)o [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="31105-111">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="31105-112">**Windows XP:**  L'utilizzo esplicito di istanze è supportato solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="31105-112">**Windows XP:**  The explicit use of instances is only supported on Windows XP and later releases.</span></span>

<span data-ttu-id="31105-113">**Windows 2000:**  Per ogni processo è supportata una sola istanza globale.</span><span class="sxs-lookup"><span data-stu-id="31105-113">**Windows 2000:**  Only one global instance is supported per process.</span></span>

### <a name="requirements"></a><span data-ttu-id="31105-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31105-114">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31105-115"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="31105-115"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="31105-116">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="31105-116">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31105-117"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="31105-117"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="31105-118">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="31105-118">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31105-119"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="31105-119"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="31105-120">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="31105-120">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="31105-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="31105-121">See Also</span></span>

[<span data-ttu-id="31105-122">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="31105-122">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="31105-123">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="31105-123">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="31105-124">JetInit</span><span class="sxs-lookup"><span data-stu-id="31105-124">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="31105-125">JetInit2</span><span class="sxs-lookup"><span data-stu-id="31105-125">JetInit2</span></span>](./jetinit2-function.md)
