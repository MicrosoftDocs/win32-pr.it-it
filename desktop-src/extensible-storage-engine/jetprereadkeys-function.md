---
description: 'Altre informazioni su: funzione JetPrereadKeys'
title: JetPrereadKeys (funzione)
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484876"
---
# <a name="jetprereadkeys-function"></a>JetPrereadKeys (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetprereadkeys-function"></a>JetPrereadKeys (funzione)

La funzione **JetPrereadKeys** legge i valori delle chiavi per migliorare le prestazioni della pulizia dell'archivio versioni.

**Windows 7:** la funzione PrereadKeys è stata introdotta in Windows 7.

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*TableID*

Cursore da utilizzare per questa chiamata.

*rgpvKeys*

Matrice di puntatori alle chiavi. Le chiavi possono essere eseguite con [JetMakeKey](./jetmakekey-function.md) o recuperate con [JetGetBookmark](./jetgetbookmark-function.md). Le chiavi devono essere ordinate in ordine crescente o decrescente, a seconda del grbit passato. Le chiavi possono essere ordinate con memcmp.

*rgcbKeys*

Matrice di lunghezze di chiave. rgpvKeys \[ n \] deve puntare a una chiave di lunghezza rgcbKeys \[ n\]

*ckeys*

Numero di chiavi. rgpvKeys e rgcbKeys devono puntare a una matrice con almeno elementi ckeys.

*pckeysPreread*

Restituisce il numero di chiavi per le quali sono state effettivamente rilasciate le preletture. Questo parametro può essere NULL.

*grbit*

Deve essere JET_bitPrereadForward o JET_bitPrereadBackward. Se grbit è JET_bitPrereadForward, le chiavi devono essere ordinate in ordine crescente. Se grbit è JET_bitPrereadBackward, le chiavi devono essere ordinate in ordine decrescente.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

È possibile restituire vari errori di I/O insieme a questi errori di utilizzo dell'API:

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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Grbit non è né JET_bitPrereadForward né JET_bitPrereadBackward.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>È stata passata una dimensione della chiave non corretta. Le chiavi non possono essere 0 o più lunghe della lunghezza massima della chiave per la tabella.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>È stato passato un parametro non valido. Questo problema può essere causato da un valore null per un parametro obbligatorio oppure può indicare che la matrice di chiavi non è ordinata correttamente.</p></td>
</tr>
</tbody>
</table>


**JetPrereadKeys** attraversa le pagine interne dell'albero b per determinare quali pagine foglia contengono le chiavi specificate da RgpvKeys/rgcbKeys. L'elenco delle pagine foglia viene ordinato, quindi vengono rilasciate le preletture per gli intervalli di pagine. Il numero di pagine che è possibile preleggere è limitato ed è quindi possibile che non tutte le chiavi vengano prelette. In tal caso, il numero di chiavi effettivamente prelette viene restituito in pckeysPreread.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows 7.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 R2.</p></td>
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
