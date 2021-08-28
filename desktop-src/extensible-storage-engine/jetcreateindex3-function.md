---
description: Altre informazioni sulla funzione JetCreateIndex3
title: Funzione JetCreateIndex3
TOCTitle: JetCreateIndex3 Function
ms:assetid: bc9b940e-65c6-49d6-ad32-74434527d29f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294075(v=EXCHG.10)
ms:contentKeyID: 32765690
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex3A
- JetCreateIndex3
- JetCreateIndex3W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0e50c0d2a2baab2b512a7525e5a852b335f99d4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981944"
---
# <a name="jetcreateindex3-function"></a>Funzione JetCreateIndex3


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreateindex3-function"></a>Funzione JetCreateIndex3

La **funzione JetCreateIndex3** crea indici sui dati in un database ESE, che possono essere usati per individuare rapidamente dati specifici.

**Windows 7: JetCreateIndex3** è stato introdotto nel sistema operativo Windows 7.

```cpp
    JET_ERR JET_API JetCreateIndex3(
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

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errCannotIndex</p> | <p>È stato effettuato un tentativo di indicizzazione su una colonna escrow-update o SLV (si noti che le colonne SLV sono deprecate).</p> | 
| <p>JET_errColumnNotFound</p> | <p>È stato effettuato un tentativo di indicizzare una colonna inesistente. Anche il tentativo di indicizzare in modo condizionale una colonna inesistente può generare questo errore.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Questo errore verrà restituito se il membro <strong>ulDensity</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su un numero minore di 20 o maggiore di 100.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>È stato effettuato un tentativo di definire due indici identici.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>È stato effettuato un tentativo di specificare più di un indice primario per una tabella. Una tabella deve avere esattamente un indice primario. Se non viene specificato alcun indice primario, il motore di database ne creerà in modo trasparente uno.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>È stata specificata una definizione di indice non valida. Di seguito sono riportati alcuni possibili motivi per la ricezione di questo errore:</p><ul><li><p>Un indice primario è condizionale (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has JET_bitIndexPrimary set e il membro <strong>cConditionalColumn</strong> di <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è maggiore di zero).</p></li><li><p>Windows Server 2003 e versioni successive di Windows. Tentativo di creare un indice di tupla con limiti di tupla, ma senza passare informazioni nel membro <strong>ptuplelimits</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ovvero <em>grbit</em> ha JET_bitIndexTupleLimits impostato, ma il <strong>puntatore ptuplelimits</strong> è NULL).</p></li><li><p>Passaggio di una definizione di chiave non valida nel membro <strong>szKey</strong> della <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> struttura. Vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> per una descrizione delle definizioni valide.</p></li><li><p>L'impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> deve essere maggiore di JET_cbPrimaryKeyMost (per un indice primario) o maggiore di JET_cbSecondaryKeyMost (per un indice secondario).</p></li><li><p>Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit JET_bitIndexUnicode impostato nel membro <strong>grbit</strong> <a href="gg294082(v=exchg.10).md">di JET_INDEXCREATE2</a>). Alcune cause comuni possono essere che il campo pidxunicode della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> sia NULL o che l'LCID specificato nella struttura pidxunicode non sia valido.</p></li><li><p>Specifica di una colonna multivalore per un indice primario.</p></li><li><p>Tentativo di indicizzare troppe colonne condizionali. Il <strong>membro cConditionalColumn</strong> della <a href="gg294082(v=exchg.10).md">struttura JET_INDEXCREATE2</a> non deve essere maggiore di JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP e versioni successive di Windows. È <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> specificata una struttura e i relativi limiti non sono supportati. Vedere la sezione osservazioni della <a href="gg269207(v=exchg.10).md">struttura</a> JET_TUPLELIMITS.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP e versioni successive di Windows. Un indice di tupla non può essere univoco (<em>grbit</em> non deve avere sia JET_bitIndexTuples che JET_bitIndexUnique impostati).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP e versioni successive di Windows. Un indice di tupla può essere solo su una singola colonna, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha un set di JET_bitIndexTuples e il membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> specifica più colonne.</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP e versioni successive di Windows. Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexTuples set.</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP e versioni successive di Windows. Un indice di tupla può essere solo in una colonna di tipo text o Unicode. Un tentativo di indicizzare altre colonne(ad esempio, colonne binarie) avrà come risultato JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP e versioni successive di Windows. Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> struttura .</p> | 
| <p>JET_errInTransaction</p> | <p>È stato effettuato un tentativo di creare un indice senza informazioni sulla versione durante una transazione.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>La definizione dell'indice non è valida perché il membro <strong>grbit</strong> <a href="gg294082(v=exchg.10).md">della struttura</a> JET_INDEXCREATE2 contiene valori incoerenti. Di seguito sono riportati alcuni possibili motivi:</p><ul><li><p>Per un indice primario è stato specificato un bit ignore (JET_bitIndexPrimary è stato passato uno dei JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</p></li><li><p>Un indice vuoto non ignora i campi NULL, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha JET_bitIndexEmpty impostato, ma non JET_bitIndexIgnoreAnyNull set.</p></li><li><p>Passaggio di una <a href="gg269214(v=exchg.10).md">struttura JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit non</strong> valido. Vedere <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Quando si creano più indici contemporaneamente, ovvero se il parametro <em>cIndexCreate</em> è maggiore di uno, nessuno degli indici può contenere uno dei bit seguenti:</p><ul><li><p>JET_bitIndexPrimary</p></li><li><p>JET_bitIndexUnversioned</p></li><li><p>JET_bitIndexEmpty</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>È stato passato un ID impostazioni locali (LCID) non valido (tramite il membro <strong>lcid</strong> nella struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX,</a> che il membro <strong>pidxunicode</strong> nella struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene un puntatore a o tramite il membro <strong>lcid</strong> della <a href="gg294082(v=exchg.10).md">struttura JET_INDEXCREATE2).</a></p> | 
| <p>JET_errInvalidName</p> | <p>È stato specificato un nome di indice non valido. Vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> per altri dettagli.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Nell'API è stato passato un parametro non valido. Di seguito sono riportati alcuni motivi per cui questo errore può essere restituito:</p><ul><li><p>Il <strong>campo cbKey</strong> di una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> struttura è impostato su zero.</p></li><li><p>Il <strong>membro cbStruct</strong> di una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è impostato su sizeof( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode. Ciò può essere causato dall'estrazione di risorse di sistema.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Un elemento della struttura degli hint per lo spazio JET non era corretto o gestibile.</p> | 



#### <a name="remarks"></a>Commenti

Il valore restituito JET_errSuccess al completamento di tutti gli indici specificati.

**JetCreateIndex3** scorre gli indici dati in **pindexcreate** e talvolta viene interrotto al primo errore. Tutti gli indici dopo il primo indice con un errore potrebbero non essere stati tentati, anche se il membro **err** della struttura JET_INDEXCREATE2 [contiene](./jet-indexcreate2-structure.md) JET_errSuccess.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetCreateIndex3W</strong> (Unicode) e <strong>JetCreateIndex3A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

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
