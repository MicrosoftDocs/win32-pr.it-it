---
description: 'Altre informazioni su: struttura JET_SNPROG'
title: Struttura JET_SNPROG
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484268"
---
# <a name="jet_snprog-structure"></a><span data-ttu-id="8c468-103">Struttura JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="8c468-103">JET_SNPROG Structure</span></span>


<span data-ttu-id="8c468-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8c468-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snprog-structure"></a><span data-ttu-id="8c468-105">Struttura JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="8c468-105">JET_SNPROG Structure</span></span>

<span data-ttu-id="8c468-106">La struttura **JET_SNPROG** contiene informazioni sullo stato di avanzamento di un'operazione a esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="8c468-106">The **JET_SNPROG** structure contains information about the progress of a long-running operation.</span></span> <span data-ttu-id="8c468-107">Quando viene chiamata la funzione di callback per notificare lo stato dell'operazione e l'operazione è ancora in corso, l'ultimo parametro della funzione di callback è un puntatore a una struttura **JET_SNPROG** .</span><span class="sxs-lookup"><span data-stu-id="8c468-107">When the callback function is called to notify the status of the operation and the operation is still in progress, the last parameter of the callback function is a pointer to a **JET_SNPROG** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a><span data-ttu-id="8c468-108">Membri</span><span class="sxs-lookup"><span data-stu-id="8c468-108">Members</span></span>

<span data-ttu-id="8c468-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="8c468-109">**cbStruct**</span></span>

<span data-ttu-id="8c468-110">Dimensioni in byte della struttura **JET_SNPROG** .</span><span class="sxs-lookup"><span data-stu-id="8c468-110">The size of the **JET_SNPROG** structure, in bytes.</span></span> <span data-ttu-id="8c468-111">Questo valore conferma la presenza dei campi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8c468-111">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="8c468-112">**cunitDone**</span><span class="sxs-lookup"><span data-stu-id="8c468-112">**cunitDone**</span></span>

<span data-ttu-id="8c468-113">Numero di unità di lavoro già completate durante la funzione a esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="8c468-113">The number of work units that are already completed during the long running function.</span></span>

<span data-ttu-id="8c468-114">**cunitTotal**</span><span class="sxs-lookup"><span data-stu-id="8c468-114">**cunitTotal**</span></span>

<span data-ttu-id="8c468-115">Numero di unità di lavoro che devono essere completate.</span><span class="sxs-lookup"><span data-stu-id="8c468-115">The number of work units that need to be completed.</span></span> <span data-ttu-id="8c468-116">Questo valore deve essere sempre maggiore o uguale a **cunitDone**.</span><span class="sxs-lookup"><span data-stu-id="8c468-116">This value should always be bigger than or equal to **cunitDone**.</span></span>

### <a name="requirements"></a><span data-ttu-id="8c468-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c468-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c468-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8c468-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8c468-119">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8c468-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c468-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8c468-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8c468-121">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8c468-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c468-122"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="8c468-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8c468-123">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="8c468-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

