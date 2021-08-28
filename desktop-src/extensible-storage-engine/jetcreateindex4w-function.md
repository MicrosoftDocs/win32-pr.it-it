---
description: Altre informazioni sulla funzione JetCreateIndex4W
title: Funzione JetCreateIndex4W
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c79f1638645f0dcd7e4306f543a9ee15b9668843
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987444"
---
# <a name="jetcreateindex4w-function"></a>Funzione JetCreateIndex4W


_**Si applica a:** Windows | Windows Server_

La **funzione JetCreateIndex4W** crea indici sui dati in un database ESE (Extensible Archiviazione Engine), che può essere usato per individuare rapidamente dati specifici.

La **funzione JetCreateIndex4W** è stata introdotta nel Windows 8 operativo.

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*tableid*

Tabella in cui verrà creato l'indice.

*pindexcreate*

Matrice di [JET_INDEXCREATE2,](./jet-indexcreate2-structure.md) ognuna delle quali definisce un indice da creare.

*cIndexCreate*

Numero di elementi nella matrice *pindexcreate.*

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti elencati nella tabella seguente. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errCannotIndex</p> | <p>È stato effettuato un tentativo di indicizzazione su una colonna di aggiornamento del deposito o SLV (si noti che le colonne SLV sono deprecate).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Si è tentato di indicizzare una colonna inesistente. Anche un tentativo di indicizzare in modo condizionale una colonna inesistente può generare questo errore.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Questo errore verrà restituito se il membro <strong>ulDensity</strong> della <a href="gg294082(v=exchg.10).md">struttura JET_INDEXCREATE2</a> è impostato su un numero minore di 20 o maggiore di 100.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>È stato effettuato un tentativo di definire due indici identici.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Si è tentato di specificare più di un indice primario per una tabella. Una tabella deve avere esattamente un indice primario. Se non viene specificato alcun indice primario, il motore di database ne creerà uno in modo trasparente.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>È stata specificata una definizione di indice non valida. Di seguito sono riportati alcuni possibili motivi per questo errore:</p><ul><li><p>Un indice primario è condizionale ( il membro<strong>grbit</strong> di <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha JET_bitIndexPrimary <strong>impostato</strong> e il membro <strong>cConditionalColumn</strong> <a href="gg294082(v=exchg.10).md">di JET_INDEXCREATE2</a> è maggiore di zero).</p></li><li><p>Si applica alle versioni Windows a partire da Windows Server 2003. È stato effettuato un tentativo di creare un indice di tupla con limiti di tupla, ma senza passare informazioni nel membro <strong>ptuplelimits</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ovvero, <em>grbit</em> ha JET_bitIndexTupleLimits <strong>impostato,</strong> ma il puntatore <strong>ptuplelimits</strong> è Null).</p></li><li><p>Passaggio di una definizione di chiave non valida nel <strong>membro szKey</strong> della <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> struttura . Per informazioni sulle definizioni valide, <a href="gg294082(v=exchg.10).md">vedere JET_INDEXCREATE2</a>.</p></li><li><p>Impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> su maggiore di <strong>JET_cbPrimaryKeyMost</strong> (per un indice primario) o maggiore <strong>di JET_cbSecondaryKeyMost</strong> (per un indice secondario).</p></li><li><p>Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit <strong>JET_bitIndexUnicode</strong> impostato nel membro <strong>grbit</strong> <a href="gg294082(v=exchg.10).md">di JET_INDEXCREATE2</a>). Alcune cause comuni possono essere il fatto che il campo pidxunicode della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è Null o che l'LCID specificato nella struttura pidxunicode non è valido.</p></li><li><p>Specifica di una colonna multivalore per un indice primario.</p></li><li><p>Tentativo di indicizzare troppe colonne condizionali. Il <strong>membro cConditionalColumn</strong> della <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve essere maggiore di <strong>JET_ccolKeyMost</strong>.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Si applica alle versioni di Windows a partire da Windows XP. È <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> specificata una struttura e i relativi limiti non sono supportati. Per altre informazioni, vedere la sezione osservazioni della <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> struttura .</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla non può essere univoco (<em>grbit</em> non deve avere sia JET_bitIndexTuples <strong>che</strong> <strong>JET_bitIndexUnique</strong> impostati).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla può essere su una sola colonna, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha un <strong>set</strong> di JET_bitIndexTuples e il membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> specifica più di una colonna.</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla non può essere un indice primario, ovvero il <strong></strong> membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere sia JET_bitIndexPrimary che <strong>JET_bitIndexTuples</strong> impostati.</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla può essere utilizzato solo in una colonna di tipo text o Unicode. Se si tenta di indicizzare altre colonne, ad esempio colonne binarie, verrà JET_errIndexTuplesTextColumnsOnly <strong>.</strong></p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> struttura .</p> | 
| <p>JET_errInTransaction</p> | <p>Si è tentato di creare un indice senza informazioni sulla versione durante una transazione.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>La definizione dell'indice non è valida perché il <strong>membro grbit</strong> della <a href="gg294082(v=exchg.10).md">struttura JET_INDEXCREATE2</a> contiene valori incoerenti. Di seguito sono riportati alcuni possibili motivi:</p><ul><li><p>Per un indice primario è stato specificato un bit ignore (JET_bitIndexPrimary passato con uno dei valori <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>o <strong>JET_bitIndexIgnoreFirstNull</strong>).</p></li><li><p>Un indice vuoto non ignora i campi Null, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha JET_bitIndexEmpty <strong>impostato,</strong> ma <strong>non JET_bitIndexIgnoreAnyNull</strong> impostato.</p></li><li><p>Passaggio di una <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit non</strong> valido. Vedere <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Quando si creano più indici contemporaneamente, ovvero se il parametro <em>cIndexCreate</em> è maggiore di uno, nessuno degli indici può contenere uno dei bit seguenti:</p><ul><li><p><strong>JET_bitIndexPrimary</strong></p></li><li><p><strong>JET_bitIndexUnversioned</strong></p></li><li><p><strong>JET_bitIndexEmpty</strong></p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>È stato passato un ID delle impostazioni locali (LCID) non valido (tramite il membro <strong>lcid</strong> nella struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX,</a> a cui il membro <strong>pidxunicode</strong> nella struttura JET_INDEXCREATE2 contiene un puntatore o tramite il membro <strong>lcid</strong> della <a href="gg294082(v=exchg.10).md">struttura JET_INDEXCREATE2).</a> <a href="gg294082(v=exchg.10).md"></a></p> | 
| <p>JET_errInvalidName</p> | <p>È stato specificato un nome di indice non valido. Vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> per altri dettagli.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un parametro non valido è stato passato all'API. Di seguito sono riportati alcuni motivi per cui può essere restituito questo errore:</p><ul><li><p>Il <strong>campo cbKey</strong> di una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su zero.</p></li><li><p>Il <strong>membro cbStruct</strong> di una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è impostato su sizeof(JET_INDEXCREATE2).</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode. Questo problema può essere causato dall'estrazione di risorse di sistema.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Un elemento della struttura degli hint di spazio JET non era corretto o utilizzabile.</p> | 



#### <a name="remarks"></a>Commenti

La **funzione JetCreateIndex4W** scorre gli indici dati nel parametro *pindexcreate* e talvolta viene interrotta al primo errore. Tutti gli indici dopo il primo indice con un errore potrebbero non essere stati tentati, anche se il membro **err** della struttura JET_INDEXCREATE2 [contiene](./jet-indexcreate2-structure.md) JET_errSuccess.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2012.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedi anche

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JET_SPACEHINTS](./jet-spacehints-structure.md)
