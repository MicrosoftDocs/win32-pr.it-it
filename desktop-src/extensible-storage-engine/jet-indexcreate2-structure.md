---
description: 'Altre informazioni su: JET_INDEXCREATE2 Structure'
title: Struttura JET_INDEXCREATE2
TOCTitle: JET_INDEXCREATE2 Structure
ms:assetid: c574500e-8695-4f29-8e9d-6dff987af2a2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294082(v=EXCHG.10)
ms:contentKeyID: 32765697
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00d5a788113b7427fb96a4f270478c1dd7572d54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473207"
---
# <a name="jet_indexcreate2-structure"></a>Struttura JET_INDEXCREATE2


_**Si applica a:** Windows | Windows Server_

La **JET_INDEXCREATE2** contiene le informazioni necessarie per creare un indice sui dati in un database ESE (Extensible Archiviazione Engine). La struttura viene usata da funzioni come [JetCreateIndex2](./jetcreateindex2-function.md) [](./jet-tablecreate-structure.md) e in strutture come JET_TABLECREATE [e JET_TABLECREATE2](./jet-tablecreate2-structure.md).

La **JET_INDEXCREATE2** è stata introdotta nel sistema operativo Windows 7.

```cpp
typedef struct tagJET_INDEXCREATE2 {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
    unsigned long cbKeyMost;
  JET_SPACEHINTS* pSpacehints;
} JET_INDEXCREATE;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensione, in byte, della struttura. Impostare questo membro su sizeof( JET_INDEXCREATE2 ).

**szIndexName**

Nome dell'indice da creare.

Il nome deve soddisfare le condizioni seguenti:

  - Deve essere minore di JET_cbNameMost, senza includere il valore Null di terminazione.

  - Deve essere costituito dal set di caratteri seguente: da 0 (zero) a 9, da A a Z, da a a z e da tutti gli altri segni di punteggiatura ad eccezione di " \! " (punto esclamativo), "," \[ (virgola), " " (parentesi di apertura) e " " (parentesi quadra di chiusura), ovvero caratteri ASCII 0x20, da 0x22 a 0x2d, da 0x2f a 0x5a, 0x5c e 0x5d fino \] a 0x7f.

  - Non deve iniziare con uno spazio.

  - Deve contenere almeno un carattere non spazio.

**szKey**

Puntatore a una stringa con terminazione double-null di token delimitati da Null.

Ogni token ha il formato " \<direction-specifier\> \<column-name\> ", dove direction-specification è "+" o "-". Ad esempio, **szKey** di "+abc \\ 0-def 0+ghi 0" indicizza le tre colonne \\ \\ "abc" (in ordine crescente), "def" (in ordine decrescente) e "ghi" (in ordine crescente). Nel linguaggio C i valori letterali stringa hanno un terminatore **NULL** implicito, quindi la stringa precedente verrà terminata da un valore double-NULL.

Il numero di colonne specificato in **szKey** non deve superare JET_ccolKeyMost (costante dipendente dalla versione).

Almeno una colonna deve essere denominata in **szKey**.

Comportamento obsoleto: dopo il carattere di terminazione double-NULL, è possibile specificare un ID di lingua (word che viene passato in MAKELCID( langid, SORT_DEFAULT ) come modo per specificare l'LCID per l'indice. Non è valido specificare sia un ID lingua in **szKey** che un LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (impostando JET_bitIndexUnicode in *grbit*).

Deprecato: dopo l'ID lingua, è possibile passare **cbVarSegMac** come tipo di dati **USHORT.** Il comportamento non è definito se USHORT è impostato sia in **szKey** che se **cbVarSegMac** è impostato nella struttura .

**cbKey**

Lunghezza, in byte, di **szKey**, inclusi i due valori Null di terminazione.

**grbit**

Gruppo di bit che contengono zero o più opzioni valore elencate nella tabella seguente.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitIndexUnique</p> | <p>Le voci di indice duplicate (chiavi) non sono consentite. Viene applicato quando viene chiamato <a href="gg269288(v=exchg.10).md">JetUpdate,</a> non quando <a href="gg294137(v=exchg.10).md">viene chiamato JetSetColumn.</a></p> | 
| <p>JET_bitIndexPrimary</p> | <p>L'indice è un indice primario (cluster). Ogni tabella deve avere esattamente un indice primario. Se non viene definito in modo esplicito alcun indice primario su una tabella, il motore di database creerà il proprio indice primario.</p> | 
| <p>JET_bitIndexDisallowNull</p> | <p>Nessuna delle colonne in cui viene creato l'indice può contenere un <strong>valore NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreNull</p> | <p>Non aggiungere una voce di indice per una riga se tutte le colonne indicizzate sono <strong>NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreAnyNull</p> | <p>Non aggiungere una voce di indice per una riga se una delle colonne indicizzate è <strong>NULL.</strong></p> | 
| <p>JET_bitIndexIgnoreFirstNull</p> | <p>Non aggiungere una voce di indice per una riga se la prima colonna indicizzata è <strong>NULL.</strong></p> | 
| <p>JET_bitIndexLazyFlush</p> | <p>Specifica che le operazioni sull'indice verranno registrate in modo lazily.</p><p>JET_bitIndexLazyFlush non influisce sulla pigrizia degli aggiornamenti dei dati. Se l'operazione di indicizzazione viene interrotta dalla terminazione del processo, il ripristino soft sarà comunque in grado di ottenere lo stato coerente del database, ma l'indice potrebbe non essere presente.</p> | 
| <p>JET_bitIndexEmpty</p> | <p>Non provare a compilare l'indice, perché tutte le voci restituiscono <strong>NULL.</strong> <strong>grbit</strong> DEVE anche specificare JET_bitIgnoreAnyNull quando JET_bitIndexEmpty viene passato. Si tratta di un miglioramento delle prestazioni. Ad esempio, se viene aggiunta una nuova colonna a una tabella e quindi viene creato un indice su questa colonna appena aggiunta, tutti i record nella tabella vengono analizzati anche se non vengono aggiunti all'indice. Se si JET_bitIndexEmpty l'analisi della tabella viene ignorata, il che potrebbe richiedere molto tempo.</p> | 
| <p>JET_bitIndexUnversioned</p> | <p>JET_bitIndexUnversioned la creazione dell'indice sia visibile ad altre transazioni. In genere, una sessione in una transazione non sarà in grado di visualizzare un'operazione di creazione dell'indice in un'altra sessione. Questo flag può essere utile se è probabile che un'altra transazione crei lo stesso indice. La seconda creazione dell'indice avrà semplicemente esito negativo anziché causare molte operazioni di database non necessarie. La seconda transazione potrebbe non essere in grado di usare immediatamente l'indice. L'operazione di creazione dell'indice deve essere completata prima che sia utilizzabile. La sessione non deve essere attualmente in una transazione per creare un indice senza informazioni sulla versione.</p> | 
| <p>JET_bitIndexSortNullsHigh</p> | <p>Se si specifica questo flag, i <strong>valori NULL</strong> vengono ordinati dopo i dati per tutte le colonne nell'indice.</p> | 
| <p>JET_bitIndexUnicode</p> | <p>La specifica di questo flag influisce sull'interpretazione del campo lcid/pidxunicde union nella struttura . L'impostazione del bit indica che il campo pidxunicode punta effettivamente a una <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> struttura. JET_bitIndexUnicode non è necessario indicizzare i dati Unicode. È necessario solo personalizzare la normalizzazione dei dati Unicode.</p> | 
| <p>JET_bitIndexTuples</p> | <p>Specifica che l'indice è un indice di tupla. Vedere <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> per una descrizione di un indice di tupla.</p><p>Il JET_bitIndexTuples è stato introdotto nel sistema operativo Windows XP.</p> | 
| <p>JET_bitIndexTupleLimits</p> | <p>La specifica di questo flag influisce sull'interpretazione del campo di unione <strong>cbVarSegMac/ptuplelimits</strong> nella struttura . L'impostazione di questo bit significa che il campo <strong>ptuplelimits</strong> punta <a href="gg269207(v=exchg.10).md">effettivamente</a> a una struttura JET_TUPLELIMITS per consentire limiti personalizzati dell'indice di tupla (implica JET_bitIndexTuples).</p><p>Il <strong>JET_bitIndexTupleLimits</strong> è stato introdotto nel sistema operativo Windows Server 2003.</p> | 
| <p>JET_bitIndexCrossProduct<br />0x00004000</p> | <p>Se si specifica questo flag per un indice con più di una colonna chiave che è una colonna multivalore, verrà creata una voce di indice per ogni risultato di un prodotto incrociato di tutti i valori in tali colonne chiave. In caso contrario, l'indice avrebbe una sola voce per ogni multivalore nella colonna chiave più significativa che è una colonna multivalore e ognuna di queste voci di indice userebbe il primo multivalore da qualsiasi altra colonna chiave che sono colonne multivalore.</p><p>Se ad esempio è stato specificato questo flag per un indice sulla colonna A con i valori "red" e "blue" e sulla colonna B con i valori "1" e "2", verranno create le voci di indice seguenti: "red", "1"; "red", "2"; "blue", "1"; "blue", "2". In caso contrario, verranno create le voci di indice seguenti: "red", "1"; "blue", "1".</p><p>Il <strong>JET_bitIndexCrossProduct</strong> è stato introdotto in Windows Vista.</p> | 
| <p>JET_bitIndexKeyMost<br />0x00008000</p> | <p>Se si specifica questo flag, l'indice userà le dimensioni massime della chiave specificate nel campo <strong>cbKeyMost</strong> nella struttura . In caso contrario, l'indice userà JET_cbKeyMost (255) come dimensione massima della chiave.</p><p>Il <strong>JET_bitIndexKeyMost</strong> è stato introdotto in Windows Vista.</p> | 
| <p>JET_bitIndexDisallowTruncation<br />0x00010000</p> | <p>Se si specifica questo flag, qualsiasi aggiornamento all'indice che potrebbe determinare un troncamento della chiave avrà esito negativo con il JET_errKeyTruncated di risposta. In caso contrario, le chiavi verranno troncate automaticamente. Per altre informazioni sul troncamento della chiave, <a href="gg269329(v=exchg.10).md">vedere JetMakeKey.</a></p><p>Il <strong>JET_bitIndexDisallowTruncation</strong> è stato introdotto in Windows Vista.</p> | 



**ulDensity**

Densità percentuale dell'albero B+ dell'indice iniziale. Se si specifica un numero minore di 100, viene inizialmente utilizzata più spazio per creare l'indice, ma è possibile che l'aumento futuro dell'indice sia disponibile, evitando così la frammentazione interna.

**lcid**

Identificatore delle impostazioni locali (LCID) da utilizzare durante la normalizzazione dei dati quando il valore JET_bitIndexUnicode non è specificato nel *parametro grbit.* L'identificatore LCID influisce sulla normalizzazione se l'indice è su colonne Unicode.

**pidxunicode**

Puntatore a una [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) struttura se il JET_bitIndexUnicode specificato nel *parametro grbit.* In questo modo l'utente può specificare flag personalizzati che vengono passati alla [funzione LCMapString durante](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) la normalizzazione Unicode.

**cbVarSegMac**

Lunghezza massima, in byte, di ogni colonna da archiviare nell'indice quando il valore JET_bitIndexTupleLimits non è specificato nel *parametro grbit.*

Specificare il valore 0 (zero) per questo campo equivale a quanto segue:

  - Specifica di JET_cbPrimaryKeyMost per un indice primario.

  - Specifica JET_cbSecondaryKeyMost per un indice secondario.

**ptuplelimits**

Puntatore a una [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) struttura se il JET_bitIndexTupleLimits specificato nel *parametro grbit.*

**ptuplelimits** è stato introdotto in Windows Server 2003.

**rgconditionalcolumn**

Parametro facoltativo di una matrice [di JET_CONDITIONALCOLUMN,](./jet-conditionalcolumn-structure.md) utilizzate per specificare le colonne condizionali nell'indice.

**cConditionalColumn**

Numero di strutture nella matrice **rgconditionalcolumn.**

**Err**

Contiene il codice restituito per la creazione dell'indice.

**cbKeyMost**

Specifica la dimensione massima consentita, in byte, per le chiavi nell'indice. Questo parametro viene ignorato se JET_bitIndexKeyMost non è specificato nel *parametro grbit.* Se questo parametro è impostato su zero e JET_bitIndexKeyMost è specificato nel membro *grbit,* la funzione chiamante avrà esito negativo con JET_err_InvalidDef.

Le dimensioni massime minime supportate per la chiave JET_cbKeyMostMin (255), ovvero le dimensioni massime della chiave legacy.

Le dimensioni massime della chiave dipendono dalle dimensioni della pagina del database (JET_paramDatabasePageSize) come indicato di seguito:

  - Se JET_paramDatabasePageSize = 2048, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Se JET_paramDatabasePageSize = 4096, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Se JET_paramDatabasePageSize = 8192, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

Le dimensioni massime della chiave supportate per l'istanza possono essere lette anche dal JET_paramKeyMost di sistema.

**cbKeyMost è** stato introdotto in Windows Vista.

**pSpacehints**

Puntatore a una [JET_SPACEHINTS](./jet-spacehints-structure.md) struttura .

**pSpacehints** è stato introdotto in Windows 7.

### <a name="remarks"></a>Commenti

ESE supporta l'indicizzazione su colonne chiave contenenti più valori. Per usare questa funzionalità, la colonna deve essere un tipo di colonna con tag (JET_bitColumnTagged) e deve essere contrassegnata in modo che i relativi valori multipli siano indicizzati con JET_bitColumnMultiValued. Nelle versioni di Windows precedenti Windows Vista, solo la prima colonna chiave multivalore nell'indice avrà i valori espansi nell'indice. Per tutte le altre colonne multivalore e con tag i primi valori verranno espansi solo nell'indice.

Supponendo che le righe seguenti esistano in una tabella (la colonna Alfa non è multivalore, mentre le colonne Beta, Gamma e Delta sono multivalore) e viene creato un indice come "+Alpha \\ 0+Beta \\ 0+Gamma \\ 0+Delta \\ \\ 0 0":


| <p>Alfa</p> | <p>Beta</p> | <p>Gamma</p> | <p>Delta</p> | 
|--------------|-------------|--------------|--------------|
| <p>1</p> | <p>ABC<br />GHI<br />JKL</p> | <p>MNO<br />PQR<br />STU</p> | <p>VWX<br />YZ</p> | 
| <p>2</p> | <p>LE</p> | <p>PIOGGIA<br />SPAGNA</p> | <p>IN<br />FALLS</p> | 



Verranno archiviate le tuple di indice seguenti:

{1,ABC,MNO,VWX}  
{1,GHI,MNO,VWX}  
{1,JKL,MNO,VWX}  
{2,THE,RAIN,IN}

Si noti che {2,THE,SPAGNA,IN} non viene archiviato, anche se la colonna Alfa nella seconda riga ha un singolo multivalore.

Nelle versioni di Windows a partire da Windows Vista, tutte le colonne multivalore possono essere espanse nell'indice specificando JET_bitIndexCrossProduct.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_ INDEXCREATE2_W</strong> (Unicode) <strong>e JET_ INDEXCREATE2_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Vedi anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
