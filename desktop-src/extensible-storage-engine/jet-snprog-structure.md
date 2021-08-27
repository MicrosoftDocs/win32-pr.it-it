---
description: 'Altre informazioni su: JET_SNPROG Structure'
title: JET_SNPROG struttura
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
ms.openlocfilehash: ab132d203ca2dc81e2ed3c3d8a0ce25c76a2cc71
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987734"
---
# <a name="jet_snprog-structure"></a>JET_SNPROG struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_snprog-structure"></a>JET_SNPROG struttura

La **JET_SNPROG** contiene informazioni sullo stato di avanzamento di un'operazione a esecuzione lunga. Quando la funzione di callback viene chiamata per notificare lo stato dell'operazione e l'operazione è ancora in corso, l'ultimo parametro della funzione di callback è un puntatore **a** una JET_SNPROG struttura.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni della struttura **JET_SNPROG,** in byte. Questo valore conferma la presenza dei campi seguenti.

**cunitDone**

Numero di unità di lavoro già completate durante la funzione a esecuzione lunga.

**cunitTotal**

Numero di unità di lavoro che devono essere completate. Questo valore deve essere sempre maggiore o uguale a **cunitDone**.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 


