---
description: Altre informazioni sulla funzione JetPrereadKeys
title: Funzione JetPrereadKeys
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
ms.openlocfilehash: 067fe72e2e00fc01b433dbda819d5e89336fc68c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467188"
---
# <a name="jetprereadkeys-function"></a>Funzione JetPrereadKeys


_**Si applica a:** Windows | Windows Server_

## <a name="jetprereadkeys-function"></a>Funzione JetPrereadKeys

La **funzione JetPrereadKeys** legge i valori delle chiavi per migliorare le prestazioni della pulizia dell'archivio versioni.

**Windows 7: la funzione PrereadKeys** è stata introdotta in Windows 7.

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

*tableid*

Cursore da utilizzare per questa chiamata.

*rgpvKeys*

Matrice di puntatori alle chiavi. Le chiavi possono essere effettuate [con JetMakeKey](./jetmakekey-function.md) o recuperate [con JetGetBookmark.](./jetgetbookmark-function.md) Le chiavi devono essere ordinate in ordine crescente o decrescente, a seconda del grbit passato. Le chiavi possono essere ordinate con memcmp.

*rgcbKeys*

Matrice di lunghezze di chiave. rgpvKeys \[ n deve puntare a una chiave di lunghezza \] rgcbKeys \[ n\]

*tasti di scelta rapida*

Numero di chiavi. rgpvKeys e rgcbKeys devono puntare a una matrice con almeno elementi ckeys.

*pckeysPreread*

Restituisce il numero di chiavi per cui sono state effettivamente emesse le prelettura. Questo parametro può essere NULL.

*grbit*

Deve essere JET_bitPrereadForward o JET_bitPrereadBackward. Se grbit è JET_bitPrereadForward, le chiavi devono essere ordinate in ordine crescente. Se grbit è JET_bitPrereadBackward, le chiavi devono essere ordinate in ordine decrescente.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

È possibile restituire vari errori di I/O insieme a questi errori di utilizzo dell'API:


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errInvalidGrbit</p> | <p>Grbit non era né JET_bitPrereadForward né JET_bitPrereadBackward.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>È stata passata una dimensione di chiave non corretta. Le chiavi non possono essere né 0 né più lunghe della lunghezza massima della chiave per la tabella.</p> | 
| <p>JET_errInvalidParameter</p> | <p>È stato passato un parametro non valido. Ciò può essere causato da un valore Null per un parametro obbligatorio o può indicare che la matrice di chiavi non è ordinata correttamente.</p> | 



**JetPrereadKeys** attraversa le pagine interne dell'albero b per determinare quali pagine foglia contengono le chiavi specificate da rgpvKeys/rgcbKeys. L'elenco delle pagine foglia viene ordinato e quindi vengono rilasciate prelettura per gli intervalli di pagine. Il numero di pagine che è possibile leggere in modo preliminare è limitato, pertanto è possibile che non tutte le chiavi siano prelette. In tal caso, il numero di chiavi effettivamente prelettura viene restituito in pckeysPreread.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows 7.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 R2.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 

