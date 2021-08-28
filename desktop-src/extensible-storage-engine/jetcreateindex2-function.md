---
description: 'Altre informazioni su: Funzione JetCreateIndex2'
title: Funzione JetCreateIndex2
TOCTitle: JetCreateIndex2 Function
ms:assetid: 8810eaed-40cb-4561-aafc-9a9bbdb0d05b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269324(v=EXCHG.10)
ms:contentKeyID: 32765614
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex2W
- JetCreateIndex2A
- JetCreateIndex2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc11fe1e5d2b4d6f14ad77cb98434b0daf6b81f1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987454"
---
# <a name="jetcreateindex2-function"></a>Funzione JetCreateIndex2


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreateindex2-function"></a>Funzione JetCreateIndex2

La **funzione JetCreateIndex2** crea indici sui dati in un database ESE, che possono essere usati per individuare rapidamente dati specifici.

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*tableid*

Tabella in cui verrà creato l'indice.

*pindexcreate*

Matrice di [JET_INDEXCREATE,](./jet-indexcreate-structure.md) ognuna delle quali definisce un indice da creare.

*cIndexCreate*

Numero di elementi nella matrice *pindexcreate.*

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errCannotIndex</p> | <p>È stato effettuato un tentativo di indicizzazione su una colonna di aggiornamento del deposito o SLV (si noti che le colonne SLV sono deprecate).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Si è tentato di indicizzare una colonna inesistente. Anche il tentativo di indicizzare in modo condizionale una colonna inesistente può generare questo errore.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Questo errore verrà restituito se il membro <strong>ulDensity</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è impostato su un numero minore di 20 o maggiore di 100.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>È stato effettuato un tentativo di definire due indici identici.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Si è tentato di specificare più di un indice primario per una tabella. Una tabella deve avere esattamente un indice primario. Se non viene specificato alcun indice primario, il motore di database ne creerà uno in modo trasparente.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>È stata specificata una definizione di indice non valida. Alcuni dei possibili motivi per la ricezione di questo errore sono:</p><ul><li><p>Un indice primario è condizionale (<strong>il membro grbit</strong> di <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha JET_bitIndexPrimary impostato e il membro <strong>cConditionalColumn</strong> <a href="gg269186(v=exchg.10).md">di JET_INDEXCREATE</a> è maggiore di zero).</p></li><li><p>Windows Server 2003 e versioni successive. Tentativo di creare un indice di tupla con limiti di tupla, ma senza passare informazioni nel membro <strong>ptuplelimits</strong> in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (ovvero, <em>grbit</em> ha JET_bitIndexTupleLimits impostato, ma il puntatore <strong>ptuplelimits</strong> è NULL).</p></li><li><p>Passaggio di una definizione di chiave non valida nel <strong>membro szKey</strong> della <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> struttura . Vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> per una descrizione delle definizioni valide.</p></li><li><p>L'impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> deve essere maggiore di JET_cbPrimaryKeyMost (per un indice primario) o maggiore di JET_cbSecondaryKeyMost (per un indice secondario).</p></li><li><p>Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit JET_bitIndexUnicode impostato nel membro <strong>grbit</strong> <a href="gg269186(v=exchg.10).md">di JET_INDEXCREATE</a>). Alcune cause comuni possono essere il fatto che il campo pidxunicode della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è NULL o che l'LCID specificato nella struttura pidxunicode non è valido.</p></li><li><p>Specifica di una colonna multivalore per un indice primario.</p></li><li><p>Tentativo di indicizzare troppe colonne condizionali. Il <strong>membro cConditionalColumn</strong> della <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non deve essere maggiore di JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP e versioni successive. È <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> specificata una struttura e i relativi limiti non sono supportati. Vedere la sezione osservazioni della struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> dati.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP e versioni successive. Un indice di tupla non può essere univoco (<em>grbit</em> non deve avere sia JET_bitIndexTuples che JET_bitIndexUnique impostati).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP e versioni successive. Un indice di tupla può essere su una sola colonna, ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha un set di JET_bitIndexTuples e il membro <strong>szKey</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> specifica più di una colonna.</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP e versioni successive. Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexTuples set.</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP e versioni successive. Un indice di tupla può essere utilizzato solo in una colonna di tipo text o Unicode. Un tentativo di indicizzare altre colonne( ad esempio, colonne binarie) avrà come risultato JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP e versioni successive. Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> struttura .</p> | 
| <p>JET_errInTransaction</p> | <p>Si è tentato di creare un indice senza informazioni sulla versione durante una transazione.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>La definizione dell'indice non è valida perché il <strong>membro grbit</strong> della <a href="gg269186(v=exchg.10).md">struttura JET_INDEXCREATE</a> contiene valori incoerenti. Alcuni possibili motivi sono:</p><ul><li><p>Per un indice primario è stato specificato un bit ignore (JET_bitIndexPrimary è stato passato uno dei valori JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</p></li><li><p>Un indice vuoto non ignora i campi NULL, ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha JET_bitIndexEmpty impostato, ma non JET_bitIndexIgnoreAnyNull impostato.</p></li><li><p>Passaggio di una <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit non</strong> valido. Vedere <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Quando si creano più indici contemporaneamente, ovvero se il parametro <em>cIndexCreate</em> è maggiore di uno, nessuno degli indici può contenere uno dei bit seguenti:</p><ul><li><p>JET_bitIndexPrimary</p></li><li><p>JET_bitIndexUnversioned</p></li><li><p>JET_bitIndexEmpty</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>È stato passato un ID impostazioni locali (LCID) non valido (tramite il membro <strong>lcid</strong> nella struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX,</a> a cui il membro <strong>pidxunicode</strong> nella struttura JET_INDEXCREATE contiene un puntatore o tramite il membro <strong>lcid</strong> della <a href="gg269186(v=exchg.10).md">struttura JET_INDEXCREATE).</a> <a href="gg269186(v=exchg.10).md"></a></p> | 
| <p>JET_errInvalidName</p> | <p>È stato specificato un nome di indice non valido. Vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> per altri dettagli.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un parametro non valido è stato passato all'API. Ecco alcuni dei motivi per cui questo errore può essere restituito:</p><ul><li><p>Il <strong>campo cbKey</strong> di una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è impostato su zero.</p></li><li><p>Il <strong>membro cbStruct</strong> di una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non è impostato su sizeof(<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode. Questo problema può essere causato dall'estrazione di risorse di sistema.</p> | 



#### <a name="remarks"></a>Commenti

Il valore restituito viene JET_errSuccess al completamento di tutti gli indici specificati.

**JetCreateIndex2** scorre gli indici dati in **pindexcreate** e talvolta viene interrotta al primo errore. Tutti gli indici dopo il primo indice con un errore potrebbero non essere stati tentati, anche se il membro **err** della struttura JET_INDEXCREATE [contiene](./jet-indexcreate-structure.md) JET_errSuccess.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetCreateIndex2W</strong> (Unicode) e <strong>JetCreateIndex2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
