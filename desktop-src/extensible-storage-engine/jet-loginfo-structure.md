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
# <a name="jet_loginfo-structure"></a>Struttura JET_LOGINFO


_**Si applica a:** Windows | Windows Server_

## <a name="jet_loginfo-structure"></a>Struttura JET_LOGINFO

La struttura **JET_LOGINFO** restituisce informazioni strutturate sul set di file di log delle transazioni che devono far parte di un set di file di backup. La struttura di **JET_LOGINFO** è il set minimo di informazioni necessarie per rappresentare un intervallo di log recuperato con [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) o specificato per un ripristino hardware con [JetExternalRestore2](./jetexternalrestore2-function.md).

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a>Membri

**cbSize**

Dimensioni, in byte, della struttura.

Questo membro consente l'espansione futura di questa struttura abilitando la compatibilità con le versioni precedenti. Deve sempre essere impostata su sizeof (JET_LOGINFO).

**ulGenLow**

Numero di file di log più basso o meno recente ripristinato. È necessario mantenere la fedeltà completa di un long senza segno, ma nelle versioni correnti del motore questo numero è un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF. Questo potrebbe cambiare nelle versioni future.

**ulGenHigh**

Il numero di file di log massimo o più recente ripristinato. È necessario mantenere la fedeltà completa di un long senza segno, ma nelle versioni correnti del motore questo numero è un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF. Questo potrebbe cambiare nelle versioni future.

**szBaseName**

Prefisso utilizzato per assegnare un nome ai file di log delle transazioni.

Il valore restituito in questo membro è sempre uguale all'impostazione per [JET_paramBaseName](./transaction-log-parameters.md) per l'istanza che ha generato queste informazioni.

### <a name="remarks"></a>Commenti

I file di log delle transazioni vengono denominati in base al nome di base dell'istanza e al numero di generazione del file di log. Il nome è nel formato BBBXXXXX. LOG. BBB corrisponde al nome di base per il file di log e ha sempre una lunghezza di tre caratteri. XXXXX corrisponde al numero di generazione del file di log in formato esadecimale con riempimento zero e ha sempre una lunghezza di cinque caratteri. LOG è l'estensione di file che viene sempre assegnata ai file di log delle transazioni da parte del motore di.

L'utilizzo di queste informazioni strutturate è sconsigliato perché comporta una conoscenza approfondita di questo schema di denominazione per i file di log delle transazioni da parte dell'applicazione. Se lo schema di denominazione viene modificato in futuro, tale applicazione non funzionerà più correttamente. È possibile che il formato di log venga modificato per incorporare 8 cifre esadecimali in futuro. Le applicazioni devono invece usare l'elenco esplicito dei nomi file restituiti da [JetGetLogInfo](./jetgetloginfo-function.md) .

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JET_LOGINFO_W</strong> (Unicode) e <strong>JET_LOGINFO_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetExternalRestore2](./jetexternalrestore2-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
