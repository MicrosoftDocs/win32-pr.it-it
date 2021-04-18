---
description: 'Altre informazioni su: JET_API_PTR'
title: JET_API_PTR
TOCTitle: JET_API_PTR
ms:assetid: 27b1eeec-1707-4edb-a4b2-2619190c21e7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269209(v=EXCHG.10)
ms:contentKeyID: 32765512
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
ms.openlocfilehash: 687f28fcba3d20c5b72a3089d3a442dd97e2dfb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317410"
---
# <a name="jet_api_ptr"></a><span data-ttu-id="6ca5c-103">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="6ca5c-103">JET_API_PTR</span></span>


<span data-ttu-id="6ca5c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6ca5c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_api_ptr"></a><span data-ttu-id="6ca5c-105">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="6ca5c-105">JET_API_PTR</span></span>

<span data-ttu-id="6ca5c-106">Il tipo di dati **JET_API_PTR** include un valore integer o un puntatore.</span><span class="sxs-lookup"><span data-stu-id="6ca5c-106">The **JET_API_PTR** data type holds an integer or a pointer value.</span></span>

```cpp
    #if defined(_WIN64)
        typedef unsigned __int64 JET_API_PTR;
    #elif !defined(__midl) && (defined(_X86_) || defined(_M_IX86)) && _MSC_VER >= 1300
        typedef __w64 unsigned long JET_API_PTR;
    #else
        typedef unsigned long JET_API_PTR;
    #endif
```

### <a name="data-types"></a><span data-ttu-id="6ca5c-107">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="6ca5c-107">Data Types</span></span>

<span data-ttu-id="6ca5c-108">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="6ca5c-108">JET_API_PTR</span></span>

<span data-ttu-id="6ca5c-109">Analogamente a un tipo di dati **DWORD_PTR** , il tipo di dati **JET_API_PTR** viene definito come 4 byte in un computer a 32 bit e a 8 byte in un computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="6ca5c-109">Like a **DWORD_PTR** data type, the **JET_API_PTR** data type is defined as 4 bytes on a 32-bit machine and 8 bytes on a 64-bit machine.</span></span>

### <a name="remarks"></a><span data-ttu-id="6ca5c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ca5c-110">Remarks</span></span>

<span data-ttu-id="6ca5c-111">Il tipo di dati **JET_API_PTR** viene utilizzato per definire i tipi di dati seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ca5c-111">The **JET_API_PTR** data type is used to define the following data types:</span></span>

  - [<span data-ttu-id="6ca5c-112">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="6ca5c-112">JET_HANDLE</span></span>](./jet-handle.md)

  - [<span data-ttu-id="6ca5c-113">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6ca5c-113">JET_INSTANCE</span></span>](./jet-instance.md)

  - [<span data-ttu-id="6ca5c-114">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6ca5c-114">JET_SESID</span></span>](./jet-sesid.md)

  - [<span data-ttu-id="6ca5c-115">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="6ca5c-115">JET_TABLEID</span></span>](./jet-tableid.md)

  - [<span data-ttu-id="6ca5c-116">JET_LS</span><span class="sxs-lookup"><span data-stu-id="6ca5c-116">JET_LS</span></span>](./jet-ls.md)

### <a name="requirements"></a><span data-ttu-id="6ca5c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ca5c-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ca5c-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6ca5c-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6ca5c-119">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6ca5c-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ca5c-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6ca5c-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6ca5c-121">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6ca5c-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ca5c-122"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="6ca5c-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6ca5c-123">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="6ca5c-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>
