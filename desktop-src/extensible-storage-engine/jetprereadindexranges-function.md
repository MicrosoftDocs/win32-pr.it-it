---
description: 'Altre informazioni su: Funzione JetPrereadIndexRanges'
title: Funzione JetPrereadIndexRanges
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ff2d9e7c538e8aa8cc862fe9a72c0308e497fd4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986664"
---
# <a name="jetprereadindexranges-function"></a>Funzione JetPrereadIndexRanges


_**Si applica a:** Windows | Windows Server_

La **funzione JetPrereadIndexRanges** prelettura gli indici per migliorare le prestazioni.

La **funzione JetPrereadIndexRanges** è stata introdotta nel Windows 8 operativo.

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*tableid*

Tabella su cui eseguire le prelettura.

*rgIndexRanges*

Intervalli di chiavi da pre-leggere.

*cIndexRanges*

Numero di intervalli di chiavi da pre-leggere, determinato dal numero di elementi in *rgIndexRanges.*

*pcRangesPreread*

Numero di intervalli di chiavi effettivamente preletti.

*rgcolumnidPreread*

Elenco di ID di colonna per le colonne con valori lunghi da leggere in modo preliminare. Per impostazione predefinita, solo il record nella pagina è prelettura. Se le colonne con valori lunghi fuori pagina devono essere prelette, i relativi ID colonna devono essere passati tramite questo parametro.

*ccolumnidPreread*

Numero di ID di colonna per le colonne con valori lunghi da preletre, determinato dal numero di elementi in *rgcolumnidPreread.*

*grbit*

Gruppo di bit che specifica zero o più valori della direzione di prelettura elencati nella tabella seguente.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>Inoltra</p> | <p>Prelettura in avanti.</p> | 
| <p>Indietro</p> | <p>Prelettura all'indietro.</p> | 
| <p>FirstPageOnly</p> | <p>Prelettura solo la prima pagina di qualsiasi colonna lunga.</p> | 
| <p>NormalizedKey</p> | <p>Chiave/segnalibro normalizzato fornito al posto del valore della colonna.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti elencati nella tabella seguente. Per altre informazioni sui possibili errori ESE [(Extensible](./extensible-storage-engine-errors.md) Archiviazione Engine), vedere Extensible Archiviazione Engine Errors and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 



#### <a name="remarks"></a>Commenti

Se i record con gli intervalli di chiavi specificati non sono presenti nella cache del buffer, è necessario avviare le letture asincrone per portare i record nella cache del buffer del database.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2012.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedi anche

[JET_ERR](./jet-err.md)
