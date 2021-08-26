---
description: Altre informazioni sulla funzione JetSetCursorFilter
title: Funzione JetSetCursorFilter
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5958d288e8b101795d1c8e4b4db789ade4b98418
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477517"
---
# <a name="jetsetcursorfilter-function"></a>Funzione JetSetCursorFilter


_**Si applica a:** Windows | Windows Server_

La **funzione JetSetCursorFilter** imposta una matrice di filtri semplici per la [funzione JetMove.](./jetmove-function.md)

La **funzione JetSetCursorFilter** è stata introdotta nel Windows 8 operativo.

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*tableid*

Cursore da posizionare.

*rgFilters*

Filtri di record semplici.

*cFilters*

Numero di filtri.

*grbit*

Gruppo di bit che specifica zero o più opzioni di spostamento elencate nella tabella seguente.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>nessuno</p> | <p>Opzione predefinita.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti elencati nella tabella seguente. Per altre informazioni sui possibili errori ESE [(Extensible](./extensible-storage-engine-errors.md) Archiviazione Engine), vedere Errori del motore extensible Archiviazione e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 



#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2012.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedi anche

[JetMove](./jetmove-function.md)  
[JET_ERR](./jet-err.md)
