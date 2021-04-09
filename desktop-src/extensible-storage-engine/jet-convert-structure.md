---
description: 'Altre informazioni su: struttura JET_CONVERT'
title: Struttura JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879829"
---
# <a name="jet_convert-structure"></a><span data-ttu-id="bb944-103">Struttura JET_CONVERT</span><span class="sxs-lookup"><span data-stu-id="bb944-103">JET_CONVERT Structure</span></span>


<span data-ttu-id="bb944-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bb944-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_convert-structure"></a><span data-ttu-id="bb944-105">Struttura JET_CONVERT</span><span class="sxs-lookup"><span data-stu-id="bb944-105">JET_CONVERT Structure</span></span>

<span data-ttu-id="bb944-106">La struttura **JET_CONVERT** contiene il nome di una dll della versione ESE precedente utilizzata per la lettura di un database creato con la versione precedente.</span><span class="sxs-lookup"><span data-stu-id="bb944-106">The **JET_CONVERT** structure contains the name of an earlier ESE version DLL that is used for reading a databases that are created with that earlier version.</span></span> <span data-ttu-id="bb944-107">Inoltre, vengono forniti altri flag per controllare la natura della conversione.</span><span class="sxs-lookup"><span data-stu-id="bb944-107">In addition, other flags are provided to control the nature of the conversion.</span></span>

<span data-ttu-id="bb944-108">**Windows Server 2003:** La funzionalità di [JetCompact](./jetcompact-function.md) che ha eseguito una conversione è stata rimossa dal prodotto in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb944-108">**Windows Server 2003:** The feature in [JetCompact](./jetcompact-function.md) that performed a conversion was removed from the product in Windows Server 2003.</span></span> <span data-ttu-id="bb944-109">È supportato solo in Windows 2000 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb944-109">It is only supported in Windows 2000 and Windows XP.</span></span>

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a><span data-ttu-id="bb944-110">Membri</span><span class="sxs-lookup"><span data-stu-id="bb944-110">Members</span></span>

<span data-ttu-id="bb944-111">**SzOldDll**</span><span class="sxs-lookup"><span data-stu-id="bb944-111">**SzOldDll**</span></span>

<span data-ttu-id="bb944-112">Nome, incluse le informazioni sul percorso, alla versione precedente della DLL ESE.</span><span class="sxs-lookup"><span data-stu-id="bb944-112">The name, including path information, to the earlier version of the ESE DLL.</span></span>

<span data-ttu-id="bb944-113">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="bb944-113">**fFlags**</span></span>

<span data-ttu-id="bb944-114">Riservato per l'utilizzo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="bb944-114">Reserved for system use.</span></span>

<span data-ttu-id="bb944-115">**fSchemaChangesOnly**</span><span class="sxs-lookup"><span data-stu-id="bb944-115">**fSchemaChangesOnly**</span></span>

<span data-ttu-id="bb944-116">Riservato per l'utilizzo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="bb944-116">Reserved for system use.</span></span>

### <a name="requirements"></a><span data-ttu-id="bb944-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb944-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb944-118"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="bb944-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bb944-119">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bb944-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb944-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bb944-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bb944-121">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bb944-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb944-122"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="bb944-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bb944-123">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="bb944-123">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb944-124"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="bb944-124"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="bb944-125">Implementato come <strong>JET_CONVERT_W</strong> (Unicode) e <strong>JET_CONVERT_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="bb944-125">Implemented as <strong>JET_CONVERT_W</strong> (Unicode) and <strong>JET_CONVERT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="bb944-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bb944-126">See Also</span></span>

[<span data-ttu-id="bb944-127">JetCompact</span><span class="sxs-lookup"><span data-stu-id="bb944-127">JetCompact</span></span>](./jetcompact-function.md)
