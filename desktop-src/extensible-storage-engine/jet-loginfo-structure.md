---
description: 'Altre informazioni su: JET_LOGINFO Structure'
title: JET_LOGINFO struttura
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
ms.openlocfilehash: 8f5619211a5fc76bb080b81b22c08c9e369abf93
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983164"
---
# <a name="jet_loginfo-structure"></a>JET_LOGINFO struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_loginfo-structure"></a>JET_LOGINFO struttura

La **JET_LOGINFO** struttura restituisce informazioni strutturate sul set di file di log delle transazioni che devono far parte di un set di file di backup. La **JET_LOGINFO** è il set minimo di informazioni necessarie per rappresentare un intervallo di log recuperato con [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) o specificato per un ripristino rigido con [JetExternalRestore2.](./jetexternalrestore2-function.md)

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

Dimensioni della struttura, in byte.

Questo membro consente l'espansione futura di questa struttura, consentendo al tempo stesso la compatibilità con le versioni precedenti. Deve sempre essere impostato su sizeof( JET_LOGINFO ).

**ulGenLow**

Numero di file di log più basso (o meno recente) ripristinato. La fedeltà completa di un valore long senza segno deve essere mantenuta, ma nelle versioni correnti del motore questo numero è un numero esadecimale nell'intervallo compreso tra 0x00000 a 0xFFFFF. Questo potrebbe cambiare nelle versioni future.

**ulGenHigh**

Numero di file di log più alto (o più recente) ripristinato. La fedeltà completa di un valore long senza segno deve essere mantenuta, ma nelle versioni correnti del motore questo numero è un numero esadecimale nell'intervallo tra 0x00000 a 0xFFFFF. Questo potrebbe cambiare nelle versioni future.

**szBaseName**

Prefisso utilizzato per assegnare un nome ai file di log delle transazioni.

Il valore restituito in questo membro è sempre uguale all'impostazione per JET_paramBaseName [per](./transaction-log-parameters.md) l'istanza che ha generato queste informazioni.

### <a name="remarks"></a>Commenti

I file di log delle transazioni vengono denominati in base al nome di base dell'istanza e al numero di generazione del file di log. Il nome è nel formato BBBXXXXX. REGISTRO. BBB corrisponde al nome di base per il file di log e ha sempre una lunghezza di tre caratteri. XXXXX corrisponde al numero di generazione del file di log in zero caratteri esadecimali con riempimento e ha sempre una lunghezza di cinque caratteri. LOG è l'estensione di file che viene sempre specificata ai file di log delle transazioni dal motore.

L'uso di queste informazioni strutturate è sconsigliato perché fa sì che l'applicazione abbia una conoscenza approfondita di questo schema di denominazione per i file di log delle transazioni. Se lo schema di denominazione viene modificato in futuro, tale applicazione non funzionerà più correttamente. È possibile che il formato del log cambi in modo da incorporare 8 cifre esadecimali in futuro. Le applicazioni devono usare invece l'elenco esplicito di nomi di file [restituiti da JetGetLogInfo.](./jetgetloginfo-function.md)

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_LOGINFO_W</strong> (Unicode) <strong>e JET_LOGINFO_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Vedere anche

[JetExternalRestore2](./jetexternalrestore2-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
