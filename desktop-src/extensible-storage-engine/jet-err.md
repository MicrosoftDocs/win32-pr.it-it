---
description: 'Altre informazioni su: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
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
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323780"
---
# <a name="jet_err"></a>JET_ERR


_**Si applica a:** Windows | Windows Server_

## <a name="jet_err"></a>JET_ERR

Il tipo di dati **JET_ERR** contiene un [codice di errore del motore di archiviazione estensibile](./extensible-storage-engine-error-codes.md).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Tipi di dati

JET_ERR

Un valore zero (corrispondente a JET_errSuccess) indica che la chiamata ha avuto esito positivo. Un valore positivo avverte una condizione non irreversibile che si è verificata durante una chiamata altrimenti riuscita. Un valore negativo indica che la chiamata non è riuscita.

### <a name="remarks"></a>Commenti

Per informazioni sulla restituzione di errori come HRESULT, vedere [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md). Per informazioni sui flag per la configurazione del database per la gestione degli errori, vedere la pagina relativa ai [parametri di gestione degli](./error-handling-parameters.md)errori.

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


### <a name="see-also"></a>Vedere anche

[Errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md)  
[Codici di errore di Extensible Storage Engine](./extensible-storage-engine-error-codes.md)  
[Parametri di gestione degli errori](./error-handling-parameters.md)
