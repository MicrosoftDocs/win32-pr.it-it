---
description: 'Altre informazioni su: funzione JetPrereadIndexRanges'
title: JetPrereadIndexRanges (funzione)
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
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128163"
---
# <a name="jetprereadindexranges-function"></a>JetPrereadIndexRanges (funzione)


_**Si applica a:** Windows | Windows Server_

La funzione **JetPrereadIndexRanges** legge gli indici per migliorare le prestazioni.

La funzione **JetPrereadIndexRanges** è stata introdotta nel sistema operativo Windows 8.

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

*TableID*

Tabella su cui eseguire le preletture.

*rgIndexRanges*

Intervalli di chiavi da preleggere.

*cIndexRanges*

Numero di intervalli di chiavi da preleggere, determinato dal numero di elementi in *rgIndexRanges*.

*pcRangesPreread*

Numero di intervalli di chiavi effettivamente preletti.

*rgcolumnidPreread*

Elenco di ID di colonna per le colonne con valore esteso da preleggere. Per impostazione predefinita, solo il record di pagina è preletto. Se è necessario preleggere le colonne con valore Long all'esterno della pagina, gli ID di colonna devono essere passati tramite questo parametro.

*ccolumnidPreread*

Numero di ID di colonna per le colonne con valore lungo da preleggere, determinato dal numero di elementi in *rgcolumnidPreread*.

*grbit*

Gruppo di bit che specifica zero o più valori di direzione di prelettura elencati nella tabella seguente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Inoltra</p></td>
<td><p>Prelettura in futuro.</p></td>
</tr>
<tr class="even">
<td><p>Indietro</p></td>
<td><p>Prelettura indietro.</p></td>
</tr>
<tr class="odd">
<td><p>FirstPageOnly</p></td>
<td><p>Prelettura solo della prima pagina di qualsiasi colonna lungo.</p></td>
</tr>
<tr class="even">
<td><p>NormalizedKey</p></td>
<td><p>Chiave/segnalibro normalizzato fornito al posto del valore della colonna.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente. Per ulteriori informazioni sui possibili errori di Extensible Storage Engine (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Se i record con gli intervalli di chiavi specificati non si trovano nella cache buffer, è consigliabile avviare le letture asincrone per inserire i record nella cache buffer del database.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedi anche

[JET_ERR](./jet-err.md)
