---
description: Altre informazioni sulla funzione JetDeleteColumn
title: Funzione JetDeleteColumn
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd20ba923157d50b3130250f4784ea9bfb19b9b1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476447"
---
# <a name="jetdeletecolumn-function"></a>Funzione JetDeleteColumn


_**Si applica a:** Windows | Windows Server_

## <a name="jetdeletecolumn-function"></a>Funzione JetDeleteColumn

La **funzione JetDeleteColumn** elimina una colonna da una tabella di database ESE.

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*tableid*

Tabella da cui eliminare la colonna.

*szColumnName*

Nome della colonna da eliminare.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errColumnInUse</p> | <p>La colonna è attualmente in uso. Può essere attualmente usato da un indice.</p> | 
| <p>JET_errFixedDDL</p> | <p>È stato effettuato un tentativo di modificare il DDL fisso.</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>La colonna denominata in <em>szColumnName</em> esiste nella tabella modello e il DDL di una tabella modello non può essere modificato.</p> | 
| <p>JET_errInvalidName</p> | <p>Può essere restituito se è stato specificato un nome non valido per <em>szColumnName.</em></p> | 
| <p>JET_errPermissionDenied</p> | <p>La tabella non è scrivibile. Può essere restituito se il database è stato aperto in modalità di sola lettura.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La transazione è di sola lettura.</p> | 



#### <a name="remarks"></a>Commenti

La **chiamata a JetDeleteColumn** è identica alla chiamata [di JetDeleteColumn2](./jetdeletecolumn2-function.md) con *grbit* impostato su zero (0).

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetDeleteColumnW</strong> (Unicode) e <strong>JetDeleteColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
