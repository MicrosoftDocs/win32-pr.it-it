---
description: 'Altre informazioni su: JET_RSTINFO Structure'
title: JET_RSTINFO struttura
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
ms.openlocfilehash: d8491b84a164ff591ce3d4a97e1e1128d8bba4f8b2e61e2b60824c501cbe4a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967841"
---
# <a name="jet_rstinfo-structure"></a>JET_RSTINFO struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_rstinfo-structure"></a>JET_RSTINFO struttura

La **JET_RSTINFO** contiene informazioni di controllo per il processo di ripristino, ad esempio le informazioni sulla rilocazione del database e la possibilità di controllare l'arresto del ripristino.

**Windows Vista:** La **JET_RSTINFO** struttura è stata introdotta in Windows Vista.

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

### <a name="members"></a>Membri

**cbStruct**

Dimensione della struttura .

**rgrstmap**

Struttura che descrive il percorso precedente e nuovo di un database ripristinato.

**crstmap**

Numero di voci di matrice in rgrstmap.

**lgposStop**

Posizione del log in cui arrestare il ripristino. Non verrà eseguita alcuna operazione di annullamento.

**logtimeStop**

Riservato per utilizzi futuri.

**pfnStatus**

Funzione di stato per la segnalazione dello stato del ripristino.

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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JET_RSTINFO_W</strong> (Unicode) <strong>e JET_RSTINFO_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetInit3](./jetinit3-function.md)
