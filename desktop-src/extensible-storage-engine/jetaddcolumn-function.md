---
description: Altre informazioni sulla funzione JetAddColumn
title: Funzione JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1f59d4bb49145dd897994bebb776249a55e14d8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466378"
---
# <a name="jetaddcolumn-function"></a>Funzione JetAddColumn


_**Si applica a:** Windows | Windows Server_

## <a name="jetaddcolumn-function"></a>Funzione JetAddColumn

La **funzione JetAddColumn** aggiunge una nuova colonna a una tabella esistente in un database ESE.

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*tableid*

Tabella a cui aggiungere la colonna.

*szColumnName*

Nome della colonna da aggiungere. Il nome deve soddisfare i criteri seguenti:

  - La lunghezza deve essere inferiore JET_cbNameMost caratteri, senza includere il carattere **DI TERMINAZIONE NULL.**

  - Deve contenere caratteri solo dai set seguenti: da 0 a 9, da A a Z, da a a z e tutti gli altri segni di punteggiatura ad eccezione del punto esclamativo ( ), della virgola (,), della parentesi di apertura ( ) e della parentesi di chiusura ( ), ovvero i caratteri ASCII 0x20, 0x22 fino a 0x2d, 0x2f fino a 0x5a, 0x5c e 0x5d tramite \! \[ \] 0x7f.

  - Non può iniziare con uno spazio.

  - Deve contenere almeno un carattere non spazio.

*pcolumndef*

Puntatore a una [JET_COLUMNDEF](./jet-columndef-structure.md) struttura che definisce i dati che possono essere archiviati in una colonna.

*pvDefault*

Puntatore a un buffer che contiene il valore predefinito per la colonna. La lunghezza del buffer è **cbDefault**. Se non è presente alcun valore predefinito, impostare **pvDefault** su **NULL** e **cbDefault** su zero. I valori predefiniti non possono essere maggiori di JET_cbColumnMost byte per le colonne fisse o JET_cbLVDefaultValueMost byte per i valori lunghi. Se un valore predefinito è maggiore di questo, verrà troncato automaticamente.

Se *grbit* ha JET_bitColumnUserDefinedDefault, **pvDefault** verrà interpretato come puntatore a una [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) struttura.

*cbDefault*

Dimensione, in byte, del buffer specificato in **pvDefault.**

*pcolumnid*

Puntatore a una [JET_COLUMNID](./jet-columnid.md) struttura che, in caso di esito positivo, riceverà l'identificatore della colonna appena creata. In caso di errore, il valore non è definito.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L'operazione è stata completata.</p> | 
| <p>JET_errFixedDDL</p> | <p>È stato effettuato un tentativo di modificare la definizione dei dati di una tabella DDL fissa. Un esempio di tabella con DDL fisso è una tabella modello.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Nell'API è stato passato un parametro non valido. Alcuni esempi di parametri non validi sono:</p><ul><li><p>Passaggio delle dimensioni erre della <a href="gg294130(v=exchg.10).md">struttura JET_COLUMNDEF</a> nel relativo <em>membro cbStruct.</em></p></li><li><p>Passando JET_bitColumnUserDefinedDefault, ma non impostando <strong>cbDefault</strong> su sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p></li></ul> | 
| <p>JET_errInTransaction</p> | <p>È stato effettuato un tentativo di aggiungere una colonna con JET_bitColumnUnversioned bit impostato, ma la sessione è attualmente in una transazione.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Una colonna esiste già. È stato effettuato un tentativo di aggiungere una colonna senza informazioni sulla versione e tale colonna esiste già.</p> | 
| <p>JET_errTableNotEmpty</p> | <p>La tabella contiene dati. Una colonna Escrow Update può essere aggiunta solo a una tabella vuota.</p> | 
| <p>JET_errRecordTooBig</p> | <p>Il record è troppo grande. La somma del <strong>parametro cbMax</strong> per le colonne fisse non deve superare un determinato valore.</p> | 
| <p>JET_errTooManyColumns</p> | <p>È stato effettuato un tentativo di aggiungere troppe colonne alla tabella. Una tabella non può avere più di JET_ccolFixedMost fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</p> | 
| <p>JET_errColumnRedundant</p> | <p>È stato effettuato un tentativo di aggiungere una colonna ridondante. Non deve essere presente più di una colonna di ridimensionamento automatico e non più di una colonna di versione per ogni tabella.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>Impossibile risolvere la funzione di callback. È possibile che la DLL non sia stata trovata o che la funzione nella DLL non sia stata trovata. Il registro eventi fornirà altri dettagli se è abilitata una registrazione sufficiente.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Avviso che indica che la lunghezza massima (<strong>cbMax</strong>) di una colonna fissa o variabile è maggiore di JET_cbColumnMost. Questo limite non si applica ai valori long ( ovvero JET_coltypLongBinary <a href="gg269213(v=exchg.10).md">e</a> <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p> | 
| <p>JET_errInvalidName</p> | <p>È stato passato un nome non valido <strong>come szColumnName</strong>. Per altre informazioni sulle restrizioni, vedere i criteri per <strong>szColumnName</strong>.</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Il <strong>campo coltyp</strong> non è stato impostato su un tipo di colonna valido.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Il <strong>parametro cp</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida. Gli unici valori validi per le colonne di testo sono Inglese (1252) e Unicode (1200). Il valore 0 indica che verrà usato il valore predefinito (inglese, 1252).</p> | 
| <p>JET_errTaggedNotNULL</p> | <p>JET_bitColumnNotNULL può essere usato con colonne con tag, valore lungo o SLV.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>È stata specificata una combinazione <em>di grbit non</em> valida. Alcuni dei motivi di questo errore sono:</p><ul><li><p>JET_bitColumnFixed usato in una colonna con tag, valore lungo o SLV.</p></li><li><p>JET_bitColumnEscrowUpdate è stato usato in una colonna che non era di <a href="gg269213(v=exchg.10).md">tipo JET_coltypLong</a>.</p></li><li><p>JET_bitColumnEscrowUpdate usato in una colonna Versione (JET_bitColumnVersion).</p></li><li><p>JET_bitColumnEscrowUpdate usato in una colonna AutoIncrememnt (JET_bitColumnAutoincrement).</p></li><li><p>JET_bitColumnEscrowUpdate usato in una colonna che non ha un valore predefinito (<strong>cbDefault</strong> è uguale a zero).</p></li><li><p>JET_bitColumnFinalize è stato usato in una colonna che non era una colonna Escrow Update (JET_bitColumnEscrowUpdate non è stata impostata).</p></li><li><p>JET_bitColumnDeleteOnZero è stato usato in una colonna che non era una colonna Escrow Update (JET_bitColumnEscrowUpdate non è stata impostata).</p></li><li><p>JET_bitColumnAutoincrement è stato usato in una colonna non <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p><p><strong>Windows 2000:</strong> Questo motivo per il codice di errore viene usato solo in Windows 2000.</p><p>JET_bitColumnAutoincrement usato in una colonna che non era né JET_coltypLong <a href="gg269213(v=exchg.10).md">né</a> <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</p><p><strong>Windows XP:</strong> Questo motivo per il codice di errore viene usato in Windows XP e nei sistemi operativi successivi.</p></li><li><p>JET_bitColumnVersion usato in una colonna non JET_coltypLong <a href="gg269213(v=exchg.10).md">.</a></p></li><li><p>JET_bitColumnVersion usato in una colonna di ridimensionamento automatico.</p></li><li><p>JET_bitColumnUserDefinedDefault usato in combinazione con JET_bitColumnFixed.</p></li><li><p>JET_bitColumnUserDefinedDefault usato in combinazione con JET_bitColumnNotNULL.</p></li><li><p>JET_bitColumnUserDefinedDefault usato in combinazione con JET_bitColumnVersion.</p></li><li><p>JET_bitColumnUserDefinedDefault usato in combinazione con JET_bitColumnAutoincrement.</p></li><li><p>JET_bitColumnUserDefinedDefault usato in combinazione con JET_bitColumnUpdatable.</p></li><li><p>JET_bitColumnUserDefinedDefault usato in combinazione con JET_bitColumnEscrowUpdate.</p></li><li><p>JET_bitColumnUserDefinedDefault usato in combinazione con JET_bitColumnFinalize.</p></li><li><p>JET_bitColumnUserDefinedDefault usato in combinazione con JET_bitColumnDeleteOnZero.</p></li><li><p>JET_bitColumnUserDefinedDefault usato in combinazione con JET_bitColumnMaybeNull.</p></li><li><p>JET_bitColumnUserDefinedDefault è stato usato in una colonna senza tag (che è fissa o variabile).</p></li></ul> | 
| <p>JET_errMultiValuedColumnMustBeTagged</p> | <p>Una colonna multivalore (JET_bitColumnMultiValued) può essere usata solo in una colonna con tag o valore lungo (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> <a href="gg269213(v=exchg.10).md">o JET_coltypLongText</a>).</p> | 
| <p>JET_errCannotBeTagged</p> | <p>È stato effettuato un tentativo di usare una colonna con tag quando la colonna potrebbe non essere contrassegnata. Alcuni dei vincoli per non consentire le colonne con tag sono:</p><ul><li><p>Non è possibile usare una colonna escrow update (JET_bitColumnEscrowUpdate) in una colonna con tag o long value<a href="gg269213(v=exchg.10).md">(JET_coltypLongBinary</a> <a href="gg269213(v=exchg.10).md">o JET_coltypLongText</a>).</p></li><li><p>Una colonna diincremento automatico potrebbe non essere contrassegnata.</p></li><li><p>Una colonna Versione potrebbe non essere contrassegnata.</p></li></ul> | 
| <p>JET_errExclusiveTableLockRequired</p> | <p>Per questa operazione era necessario un blocco esclusivo sulla tabella.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Avviso che indica che la lunghezza massima (<em>cbMax</em>) di una colonna fissa o variabile è maggiore di JET_cbColumnMost. Questo limite non si applica ai valori long ( ovvero JET_coltypLongBinary <a href="gg269213(v=exchg.10).md">e</a> <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p> | 



#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
