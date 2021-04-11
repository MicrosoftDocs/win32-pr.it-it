---
description: 'Altre informazioni su: struttura JET_RSTINFO'
title: Struttura JET_RSTINFO
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128666"
---
# <a name="jet_rstinfo-structure"></a><span data-ttu-id="b527f-103">Struttura JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="b527f-103">JET_RSTINFO Structure</span></span>


<span data-ttu-id="b527f-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b527f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstinfo-structure"></a><span data-ttu-id="b527f-105">Struttura JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="b527f-105">JET_RSTINFO Structure</span></span>

<span data-ttu-id="b527f-106">La struttura **JET_RSTINFO** contiene informazioni di controllo per il processo di ripristino, ad esempio informazioni sulla rilocazione del database e la possibilità di controllare l'arresto del ripristino.</span><span class="sxs-lookup"><span data-stu-id="b527f-106">The **JET_RSTINFO** structure contains control information for the recovery process like database relocation information and ability to control stopping recovery.</span></span>

<span data-ttu-id="b527f-107">**Windows Vista:** La struttura **JET_RSTINFO** è stata introdotta in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b527f-107">**Windows Vista:** The **JET_RSTINFO** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a><span data-ttu-id="b527f-108">Membri</span><span class="sxs-lookup"><span data-stu-id="b527f-108">Members</span></span>

<span data-ttu-id="b527f-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="b527f-109">**cbStruct**</span></span>

<span data-ttu-id="b527f-110">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="b527f-110">The size of the structure.</span></span>

<span data-ttu-id="b527f-111">**rgrstmap**</span><span class="sxs-lookup"><span data-stu-id="b527f-111">**rgrstmap**</span></span>

<span data-ttu-id="b527f-112">Struttura che descrive il vecchio e il nuovo percorso di un database ripristinato.</span><span class="sxs-lookup"><span data-stu-id="b527f-112">The structure that describes the old and new path of a restored database.</span></span>

<span data-ttu-id="b527f-113">**crstmap**</span><span class="sxs-lookup"><span data-stu-id="b527f-113">**crstmap**</span></span>

<span data-ttu-id="b527f-114">Numero di voci della matrice in rgrstmap.</span><span class="sxs-lookup"><span data-stu-id="b527f-114">Count of array entries in the rgrstmap.</span></span>

<span data-ttu-id="b527f-115">**lgposStop**</span><span class="sxs-lookup"><span data-stu-id="b527f-115">**lgposStop**</span></span>

<span data-ttu-id="b527f-116">Posizione del log in cui arrestare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="b527f-116">The log position to stop recovery at.</span></span> <span data-ttu-id="b527f-117">Non verrà eseguita alcuna operazione di annullamento.</span><span class="sxs-lookup"><span data-stu-id="b527f-117">No undo will be done.</span></span>

<span data-ttu-id="b527f-118">**logtimeStop**</span><span class="sxs-lookup"><span data-stu-id="b527f-118">**logtimeStop**</span></span>

<span data-ttu-id="b527f-119">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="b527f-119">Reserved for future use.</span></span>

<span data-ttu-id="b527f-120">**pfnStatus**</span><span class="sxs-lookup"><span data-stu-id="b527f-120">**pfnStatus**</span></span>

<span data-ttu-id="b527f-121">Funzione di stato per la segnalazione dello stato del ripristino.</span><span class="sxs-lookup"><span data-stu-id="b527f-121">A status function for reporting status of recovery.</span></span>

### <a name="requirements"></a><span data-ttu-id="b527f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b527f-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b527f-123"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b527f-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b527f-124">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b527f-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b527f-125"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b527f-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b527f-126">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b527f-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b527f-127"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b527f-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b527f-128">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b527f-128">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b527f-129"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b527f-129"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b527f-130">Implementato come <strong>JET_RSTINFO_W</strong> (Unicode) e <strong>JET_RSTINFO_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b527f-130">Implemented as <strong>JET_RSTINFO_W</strong> (Unicode) and <strong>JET_RSTINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b527f-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b527f-131">See Also</span></span>

[<span data-ttu-id="b527f-132">JetInit3</span><span class="sxs-lookup"><span data-stu-id="b527f-132">JetInit3</span></span>](./jetinit3-function.md)
