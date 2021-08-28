---
description: 'Altre informazioni su: Funzione JetDeleteColumn2'
title: Funzione JetDeleteColumn2
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2e74c507483791f3090b43e436e01ce7b5173e0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984964"
---
# <a name="jetdeletecolumn2-function"></a>Funzione JetDeleteColumn2


_**Si applica a:** Windows | Windows Server_

## <a name="jetdeletecolumn2-function"></a>Funzione JetDeleteColumn2

La **funzione JetDeleteColumn2** elimina una colonna da una tabella di database ESE e abilita l'impostazione di un'opzione *grbit.*

**Windows XP: JetDeleteColumn2** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*tableid*

Tabella contenente la colonna da eliminare.

*szColumnName*

Nome della colonna da eliminare.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitDeleteColumnIgnoreTemplateColumns</p> | <p>Impostando JET_bitDeleteColumIgnoreTemplateColumns, l'API tenterà di eliminare solo le colonne nella tabella derivata. Se nella tabella di base esiste una colonna con tale nome, questa verrà ignorata.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errColumnInUse</p> | <p>La colonna è attualmente in uso. Può essere attualmente utilizzato da un indice.</p> | 
| <p>JET_errFixedDDL</p> | <p>Si è tentato di modificare il DDL fisso.</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>La colonna denominata in <em>szColumnName</em> esiste nella tabella modello e non è possibile modificare il DDL di una tabella modello.</p> | 
| <p>JET_errInvalidName</p> | <p>Può essere restituito se è stato specificato un nome non valido <em>per szColumnName.</em></p> | 
| <p>JET_errPermissionDenied</p> | <p>La tabella non è scrivibile. Può essere restituito se il database è stato aperto in modalità di sola lettura.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La transazione è di sola lettura.</p> | 



#### <a name="remarks"></a>Commenti

La [chiamata a JetDeleteColumn](./jetdeletecolumn-function.md) è identica alla chiamata **di JetDeleteColumn2** con *grbit* impostato su zero (0).

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetDeleteColumn2W</strong> (Unicode) e <strong>JetDeleteColumn2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)
