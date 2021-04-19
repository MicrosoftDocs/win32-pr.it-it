---
description: 'Altre informazioni su: struttura JET_LOGINFO'
title: Struttura JET_LOGINFO
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
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
ms.openlocfilehash: b7e643d775d1fb8e0c19286bfb7a50d887644e99
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323795"
---
# <a name="jet_loginfo-structure"></a><span data-ttu-id="ed527-103">Struttura JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="ed527-103">JET_LOGINFO Structure</span></span>


<span data-ttu-id="ed527-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ed527-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_loginfo-structure"></a><span data-ttu-id="ed527-105">Struttura JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="ed527-105">JET_LOGINFO Structure</span></span>

<span data-ttu-id="ed527-106">La struttura **JET_LOGINFO** restituisce informazioni strutturate sul set di file di log delle transazioni che devono far parte di un set di file di backup.</span><span class="sxs-lookup"><span data-stu-id="ed527-106">The **JET_LOGINFO** structure returns structured information about the set of transaction log files that should be a part of a backup file set.</span></span> <span data-ttu-id="ed527-107">La struttura di **JET_LOGINFO** è il set minimo di informazioni necessarie per rappresentare un intervallo di log recuperato con [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) o specificato per un ripristino hardware con [JetExternalRestore2](./jetexternalrestore2-function.md).</span><span class="sxs-lookup"><span data-stu-id="ed527-107">The **JET_LOGINFO** structure is the minimal set of information needed to represent a range of logs that is retrieved with [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) or specified for a hard recovery with [JetExternalRestore2](./jetexternalrestore2-function.md).</span></span>

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a><span data-ttu-id="ed527-108">Membri</span><span class="sxs-lookup"><span data-stu-id="ed527-108">Members</span></span>

<span data-ttu-id="ed527-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="ed527-109">**cbSize**</span></span>

<span data-ttu-id="ed527-110">Dimensioni, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="ed527-110">The size of the structure, in bytes.</span></span>

<span data-ttu-id="ed527-111">Questo membro consente l'espansione futura di questa struttura abilitando la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="ed527-111">This member enables future expansion of this structure while enabling backwards compatibility.</span></span> <span data-ttu-id="ed527-112">Deve sempre essere impostata su sizeof (JET_LOGINFO).</span><span class="sxs-lookup"><span data-stu-id="ed527-112">It should always be set to sizeof( JET_LOGINFO ).</span></span>

<span data-ttu-id="ed527-113">**ulGenLow**</span><span class="sxs-lookup"><span data-stu-id="ed527-113">**ulGenLow**</span></span>

<span data-ttu-id="ed527-114">Numero di file di log più basso o meno recente ripristinato.</span><span class="sxs-lookup"><span data-stu-id="ed527-114">The lowest (or oldest) log file number that is restored.</span></span> <span data-ttu-id="ed527-115">È necessario mantenere la fedeltà completa di un long senza segno, ma nelle versioni correnti del motore questo numero è un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="ed527-115">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="ed527-116">Questo potrebbe cambiare nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="ed527-116">This might change in future versions.</span></span>

<span data-ttu-id="ed527-117">**ulGenHigh**</span><span class="sxs-lookup"><span data-stu-id="ed527-117">**ulGenHigh**</span></span>

<span data-ttu-id="ed527-118">Il numero di file di log massimo o più recente ripristinato.</span><span class="sxs-lookup"><span data-stu-id="ed527-118">The highest (or most recent) log file number that is restored.</span></span> <span data-ttu-id="ed527-119">È necessario mantenere la fedeltà completa di un long senza segno, ma nelle versioni correnti del motore questo numero è un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="ed527-119">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="ed527-120">Questo potrebbe cambiare nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="ed527-120">This might change in future versions.</span></span>

<span data-ttu-id="ed527-121">**szBaseName**</span><span class="sxs-lookup"><span data-stu-id="ed527-121">**szBaseName**</span></span>

<span data-ttu-id="ed527-122">Prefisso utilizzato per assegnare un nome ai file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="ed527-122">The prefix used to name the transaction log files.</span></span>

<span data-ttu-id="ed527-123">Il valore restituito in questo membro è sempre uguale all'impostazione per [JET_paramBaseName](./transaction-log-parameters.md) per l'istanza che ha generato queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="ed527-123">The value that is returned in this member is always equal to the setting for [JET_paramBaseName](./transaction-log-parameters.md) for the instance that generated this information.</span></span>

### <a name="remarks"></a><span data-ttu-id="ed527-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed527-124">Remarks</span></span>

<span data-ttu-id="ed527-125">I file di log delle transazioni vengono denominati in base al nome di base dell'istanza e al numero di generazione del file di log.</span><span class="sxs-lookup"><span data-stu-id="ed527-125">Transaction log files are named according to the instance base name and the generation number of the log file.</span></span> <span data-ttu-id="ed527-126">Il nome è nel formato BBBXXXXX. LOG.</span><span class="sxs-lookup"><span data-stu-id="ed527-126">The name is of the format BBBXXXXX.LOG.</span></span> <span data-ttu-id="ed527-127">BBB corrisponde al nome di base per il file di log e ha sempre una lunghezza di tre caratteri.</span><span class="sxs-lookup"><span data-stu-id="ed527-127">BBB corresponds to the base name for the log file and is always three characters in length.</span></span> <span data-ttu-id="ed527-128">XXXXX corrisponde al numero di generazione del file di log in formato esadecimale con riempimento zero e ha sempre una lunghezza di cinque caratteri.</span><span class="sxs-lookup"><span data-stu-id="ed527-128">XXXXX corresponds to the generation number of the log file in zero padded hexadecimal and is always five characters in length.</span></span> <span data-ttu-id="ed527-129">LOG è l'estensione di file che viene sempre assegnata ai file di log delle transazioni da parte del motore di.</span><span class="sxs-lookup"><span data-stu-id="ed527-129">LOG is the file extension that is always given to transaction log files by the engine.</span></span>

<span data-ttu-id="ed527-130">L'utilizzo di queste informazioni strutturate è sconsigliato perché comporta una conoscenza approfondita di questo schema di denominazione per i file di log delle transazioni da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ed527-130">Use of this structured information is discouraged because it causes the application to have intimate knowledge of this naming scheme for transaction log files.</span></span> <span data-ttu-id="ed527-131">Se lo schema di denominazione viene modificato in futuro, tale applicazione non funzionerà più correttamente.</span><span class="sxs-lookup"><span data-stu-id="ed527-131">If the naming scheme ever changes in the future then such an application will no longer function properly.</span></span> <span data-ttu-id="ed527-132">È possibile che il formato di log venga modificato per incorporare 8 cifre esadecimali in futuro.</span><span class="sxs-lookup"><span data-stu-id="ed527-132">It is conceivable that the log format will change to incorporate 8 hex digits in the future.</span></span> <span data-ttu-id="ed527-133">Le applicazioni devono invece usare l'elenco esplicito dei nomi file restituiti da [JetGetLogInfo](./jetgetloginfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ed527-133">Applications should use the explicit list of file names returned by [JetGetLogInfo](./jetgetloginfo-function.md) instead.</span></span>

### <a name="requirements"></a><span data-ttu-id="ed527-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed527-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed527-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ed527-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ed527-136">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed527-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed527-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ed527-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ed527-138">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ed527-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed527-139"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ed527-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ed527-140">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ed527-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed527-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ed527-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ed527-142">Implementato come <strong>JET_LOGINFO_W</strong> (Unicode) e <strong>JET_LOGINFO_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ed527-142">Implemented as <strong>JET_LOGINFO_W</strong> (Unicode) and <strong>JET_LOGINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ed527-143">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ed527-143">See Also</span></span>

[<span data-ttu-id="ed527-144">JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="ed527-144">JetExternalRestore2</span></span>](./jetexternalrestore2-function.md)  
[<span data-ttu-id="ed527-145">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="ed527-145">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="ed527-146">JetGetLogInfoInstance2</span><span class="sxs-lookup"><span data-stu-id="ed527-146">JetGetLogInfoInstance2</span></span>](./jetgetloginfoinstance2-function.md)  
[<span data-ttu-id="ed527-147">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="ed527-147">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
