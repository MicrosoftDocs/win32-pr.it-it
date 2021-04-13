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
# <a name="jet_snprog-structure"></a>Struttura JET_SNPROG


_**Si applica a:** Windows | Windows Server_

## <a name="jet_snprog-structure"></a>Struttura JET_SNPROG

La struttura **JET_SNPROG** contiene informazioni sullo stato di avanzamento di un'operazione a esecuzione prolungata. Quando viene chiamata la funzione di callback per notificare lo stato dell'operazione e l'operazione è ancora in corso, l'ultimo parametro della funzione di callback è un puntatore a una struttura **JET_SNPROG** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni in byte della struttura **JET_SNPROG** . Questo valore conferma la presenza dei campi seguenti.

**cunitDone**

Numero di unità di lavoro già completate durante la funzione a esecuzione prolungata.

**cunitTotal**

Numero di unità di lavoro che devono essere completate. Questo valore deve essere sempre maggiore o uguale a **cunitDone**.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>

