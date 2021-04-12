---
description: 'Altre informazioni su: struttura JET_SETSYSPARAM'
title: Struttura JET_SETSYSPARAM
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342991"
---
# <a name="jet_setsysparam-structure"></a><span data-ttu-id="0fa5a-103">Struttura JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="0fa5a-103">JET_SETSYSPARAM Structure</span></span>


<span data-ttu-id="0fa5a-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0fa5a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setsysparam-structure"></a><span data-ttu-id="0fa5a-105">Struttura JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="0fa5a-105">JET_SETSYSPARAM Structure</span></span>

<span data-ttu-id="0fa5a-106">Una matrice di strutture di **JET_SETSYSPARAM** indica un set specifico di parametri di sistema globale impostati come argomento quando si utilizza la funzione [JetEnableMultiInstance](./jetenablemultiinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0fa5a-106">An array of **JET_SETSYSPARAM** structures indicate a specific set of global system parameters that are set as an argument when using the [JetEnableMultiInstance](./jetenablemultiinstance-function.md) function.</span></span>

<span data-ttu-id="0fa5a-107">**Windows XP:** Questa struttura è stata introdotta in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0fa5a-107">**Windows XP:** This structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a><span data-ttu-id="0fa5a-108">Membri</span><span class="sxs-lookup"><span data-stu-id="0fa5a-108">Members</span></span>

<span data-ttu-id="0fa5a-109">**paramid**</span><span class="sxs-lookup"><span data-stu-id="0fa5a-109">**paramid**</span></span>

<span data-ttu-id="0fa5a-110">ID del parametro di sistema che verrà impostato.</span><span class="sxs-lookup"><span data-stu-id="0fa5a-110">The ID of the system parameter that will be set.</span></span>

<span data-ttu-id="0fa5a-111">Vedere [parametri di sistema Extensible Storage Engine](./extensible-storage-engine-system-parameters.md) per un elenco completo dei parametri di sistema e delle rispettive proprietà.</span><span class="sxs-lookup"><span data-stu-id="0fa5a-111">See [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="0fa5a-112">**lParam**</span><span class="sxs-lookup"><span data-stu-id="0fa5a-112">**lParam**</span></span>

<span data-ttu-id="0fa5a-113">Valore facoltativo da impostare per il parametro di sistema selezionato se il parametro di sistema è di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="0fa5a-113">The optional value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="0fa5a-114">**SZ**</span><span class="sxs-lookup"><span data-stu-id="0fa5a-114">**sz**</span></span>

<span data-ttu-id="0fa5a-115">Valore facoltativo da impostare per il parametro di sistema selezionato se tale parametro di sistema è di tipo String.</span><span class="sxs-lookup"><span data-stu-id="0fa5a-115">The optional value to be set for the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="0fa5a-116">**Err**</span><span class="sxs-lookup"><span data-stu-id="0fa5a-116">**err**</span></span>

<span data-ttu-id="0fa5a-117">Errore risultante dalla chiamata a [JetSetSystemParameter](./jetsetsystemparameter-function.md) con i parametri specificati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0fa5a-117">The error resulting from the call to [JetSetSystemParameter](./jetsetsystemparameter-function.md) with the previously specified parameters.</span></span>

### <a name="requirements"></a><span data-ttu-id="0fa5a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fa5a-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fa5a-119"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0fa5a-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa5a-120">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0fa5a-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa5a-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0fa5a-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa5a-122">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0fa5a-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fa5a-123"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="0fa5a-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa5a-124">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="0fa5a-124">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fa5a-125"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0fa5a-125"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0fa5a-126">Implementato come <strong>JET_ SETSYSPARAM_W</strong> (Unicode) e <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0fa5a-126">Implemented as <strong>JET_ SETSYSPARAM_W</strong> (Unicode) and <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0fa5a-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0fa5a-127">See Also</span></span>

[<span data-ttu-id="0fa5a-128">Parametri di sistema Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="0fa5a-128">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)  
[<span data-ttu-id="0fa5a-129">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="0fa5a-129">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="0fa5a-130">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0fa5a-130">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0fa5a-131">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="0fa5a-131">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="0fa5a-132">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="0fa5a-132">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
