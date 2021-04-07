---
description: 'Altre informazioni su: struttura JET_INDEXCREATE'
title: Struttura JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE Structure
ms:assetid: 0c55f25c-d42a-49ba-a1fe-549850fdc9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269186(v=EXCHG.10)
ms:contentKeyID: 32765489
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
ms.openlocfilehash: 4c465d81dce628497b1b9210fb08b37a3003e2e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757937"
---
# <a name="jet_indexcreate-structure"></a>Struttura JET_INDEXCREATE


_**Si applica a:** Windows | Windows Server_

La struttura **JET_INDEXCREATE** contiene le informazioni necessarie per creare un indice sui dati in un database Extensible Storage Engine (ESE). La struttura viene utilizzata da funzioni quali [JetCreateIndex2](./jetcreateindex2-function.md)e in strutture quali [JET_TABLECREATE](./jet-tablecreate-structure.md) e [JET_TABLECREATE2](./jet-tablecreate2-structure.md).

``` c++
typedef struct tagJET_INDEXCREATE {
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
} JET_INDEXCREATE;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensione, in byte, della struttura. Impostare questo membro su sizeof (JET_INDEXCREATE).

**szIndexName**

Nome dell'indice da creare.

Il nome dell'indice deve soddisfare le condizioni seguenti:

  - Deve essere minore di JET_cbNameMost, escluso il valore null di terminazione.

  - Deve essere costituito dai caratteri seguenti: 0 (zero) a 9, da A A Z, da a a z e tutti gli altri segni di punteggiatura, ad eccezione di " \! " (punto esclamativo), "," (virgola), " \[ " (parentesi di apertura) e " \] " (parentesi di chiusura), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c, 0x5D tramite 0x7F.

  - Non deve iniziare con uno spazio.

  - Deve essere costituito da almeno un carattere non di spazio.

**szKey**

Puntatore a una stringa con terminazione null di token delimitati da null.

Ogni token è nel formato " \<direction-specifier\> \<column-name\> ", dove Direction-Specification è "+" o "-". Ad esempio, un **szKey** di "+ ABC \\ 0-def \\ 0 + ghi \\ 0" effettuerà l'indice sulle tre colonne "ABC" (in ordine crescente), "def" (in ordine decrescente) e "ghi" (in ordine crescente). Nel linguaggio C i valori letterali stringa hanno un carattere di terminazione **null** implicito; Pertanto, la stringa precedente verrà terminata da un valore Double NULL.

Il numero di colonne specificato in **szKey** non può superare il valore di **JET_ccolKeyMost** , ovvero una costante dipendente dalla versione.

Almeno una colonna deve essere denominata in **szKey**.

Comportamento obsoleto: dopo il carattere di terminazione doppio NULL, è possibile specificare un ID lingua (una parola che viene passata in MAKELCID (LangID, SORT_DEFAULT)) come metodo per specificare l'LCID per l'indice. Non è consentito specificare sia un ID lingua in **szKey** che un LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) , impostando JET_bitIndexUnicode in *grbit*.

Deprecato: dopo l'ID lingua, è possibile passare **cbVarSegMac** come UShort. Il comportamento non è definito se USHORT è impostato in **szKey** e se **cbVarSegMac** è impostato nella struttura.

**cbKey**

Lunghezza, in byte, di **szKey** , inclusi i due valori null di terminazione.

**grbit**

Gruppo di bit che include zero o più valori elencati nella tabella seguente.

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
<td><p>JET_bitIndexUnique</p></td>
<td><p>Non sono consentite voci di indice duplicate (chiavi). Questa operazione viene applicata quando viene chiamato <a href="gg269288(v=exchg.10).md">JetUpdate</a> , non quando viene chiamato <a href="gg294137(v=exchg.10).md">JetSetColumn</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexPrimary</p></td>
<td><p>L'indice è un indice primario (cluster). Ogni tabella deve avere esattamente un indice primario. Se nessun indice primario viene definito in modo esplicito su una tabella, il motore di database creerà il proprio indice primario.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexDisallowNull</p></td>
<td><p>Nessuna delle colonne in cui viene creato l'indice può contenere un valore <strong>null</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreNull</p></td>
<td><p>Non aggiungere una voce di indice per una riga se tutte le colonne indicizzate sono <strong>null</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexIgnoreAnyNull</p></td>
<td><p>Non aggiungere una voce di indice per una riga se una delle colonne indicizzate è <strong>null</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreFirstNull</p></td>
<td><p>Non aggiungere una voce di indice per una riga se la prima colonna indicizzata è <strong>null</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexLazyFlush</p></td>
<td><p>Le operazioni sugli indici verranno registrate in modalità differita.</p>
<p>JET_bitIndexLazyFlush non influisce sulla pigrizia degli aggiornamenti dei dati. Se l'operazione di indicizzazione viene interrotta dalla terminazione del processo, il ripristino soft sarà comunque in grado di ottenere il database in uno stato coerente, ma l'indice potrebbe non essere presente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexEmpty</p></td>
<td><p>Non tentare di compilare l'indice perché tutte le voci restituiscono <strong>null</strong>. <strong>grbit</strong> deve inoltre specificare JET_bitIgnoreAnyNull quando viene passato JET_bitIndexEmpty. Si tratta di un miglioramento delle prestazioni. Se, ad esempio, viene aggiunta una nuova colonna a una tabella, viene creato un indice sulla colonna appena aggiunta e tutti i record della tabella vengono analizzati anche se non vengono aggiunti all'indice. La specifica di JET_bitIndexEmpty ignora l'analisi della tabella, che potrebbe richiedere molto tempo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnversioned</p></td>
<td><p>Causa la visibilità della creazione dell'indice in altre transazioni. In genere, una sessione in una transazione non sarà in grado di visualizzare un'operazione di creazione dell'indice in un'altra sessione. Questo flag può essere utile se è probabile che un'altra transazione crei lo stesso indice. La seconda creazione dell'indice avrà esito negativo anziché causare potenzialmente molte operazioni di database non necessarie. La seconda transazione potrebbe non essere in grado di utilizzare immediatamente l'indice. L'operazione di creazione dell'indice deve essere completata prima che sia utilizzabile. La sessione non deve attualmente trovarsi in una transazione per creare un indice senza informazioni sulla versione.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexSortNullsHigh</p></td>
<td><p>Se si specifica questo flag, i valori <strong>null</strong> verranno ordinati dopo i dati per tutte le colonne dell'indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnicode</p></td>
<td><p>L'impostazione di questo flag influiscono sull'interpretazione del campo di Unione LCID/pidxunicde nella struttura. L'impostazione del bit significa che il campo <strong>pidxunicode</strong> punta effettivamente a una struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> . JET_bitIndexUnicode non è necessario per indicizzare i dati Unicode. Viene utilizzato solo per personalizzare la normalizzazione dei dati Unicode.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexTuples</p></td>
<td><p>Specifica che l'indice è un indice della tupla. Per una descrizione di un indice di tupla, vedere <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p>
<p>JET_bitIndexTuples è stato introdotto nel sistema operativo Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexTupleLimits</p></td>
<td><p>L'impostazione di questo flag influiscono sull'interpretazione del campo di Unione <strong>cbVarSegMac/ptuplelimits</strong> nella struttura. L'impostazione di questo bit significa che il campo <strong>ptuplelimits</strong> punta effettivamente a una struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> per consentire limiti di indice di tupla personalizzati (implica JET_bitIndexTuples).</p>
<p>JET_bitIndexTupleLimits è stato introdotto nel sistema operativo Windows Server 2003.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexCrossProduct 0x00004000</p></td>
<td><p>Se si specifica questo flag per un indice con più di una colonna chiave che è una colonna multivalore, verrà creata una voce di indice per ogni risultato di un prodotto incrociato di tutti i valori in tali colonne chiave. In caso contrario, l'indice avrà una sola voce per ogni valore multivalore nella colonna chiave più significativa che è una colonna multivalore e ognuna di queste voci di indice utilizzerà il primo valore multivalore di qualsiasi altra colonna chiave che è costituita da colonne multivalore.</p>
<p>Se, ad esempio, si specifica questo flag per un indice sulla colonna A con i valori &quot; rosso &quot; e &quot; blu &quot; e sulla colonna B con i valori &quot; 1 &quot; e 2 &quot; , &quot; verranno create le voci di indice seguenti: &quot; rosso &quot; , &quot; 1 &quot; ; &quot; rosso &quot; , &quot; 2 &quot; ; &quot; blu &quot; , &quot; 1 &quot; ; &quot; blu &quot; , &quot; 2 &quot; . In caso contrario, verranno create le voci di indice seguenti: &quot; rosso &quot; , &quot; 1 &quot; ; &quot; blu &quot; , &quot; 1 &quot; .</p>
<p>JET_bitIndexCrossProduct è stato introdotto nel sistema operativo Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexKeyMost 0x00008000</p></td>
<td><p>Se si specifica questo flag, l'indice utilizzerà la dimensione massima della chiave specificata nel campo <strong>cbKeyMost</strong> della struttura. In caso contrario, l'indice utilizzerà JET_cbKeyMost (255) come dimensione massima della chiave.</p>
<p>JET_bitIndexKeyMost è stato introdotto in Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexDisallowTruncation 0x00010000</p></td>
<td><p>Se si specifica questo flag, eventuali aggiornamenti all'indice che comporteranno la mancata riuscita di una chiave troncata con JET_errKeyTruncated. In caso contrario, le chiavi verranno troncate automaticamente. Per ulteriori informazioni sul troncamento delle chiavi, vedere la funzione <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</p>
<p><strong>Windows Vista: JET_bitIndexDisallowTruncation</strong> è stato introdotto in Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexNestedTable 0x00020000</p></td>
<td><p>Se si specifica questo flag, l'indice verrà aggiornato su più colonne multivalore, ma solo con valori dello stesso <strong>itagSequence</strong>.</p>
<p>JET_bitIndexNestedTable è stato introdotto in Windows Vista.</p></td>
</tr>
</tbody>
</table>


**ulDensity**

Densità percentuale dell'albero iniziale B + dell'indice. Se si specifica un numero inferiore a 100, viene utilizzato un maggior numero di spazio per la creazione iniziale dell'indice, ma è possibile applicare una crescita futura dell'indice, evitando così la frammentazione interna.

**lcid**

Identificatore delle impostazioni locali (LCID) da usare per la normalizzazione dei dati quando il valore di JET_bitIndexUnicode non è specificato nel parametro *grbit* . L'LCID influiscono sulla normalizzazione se l'indice è sovrascrivendo le colonne Unicode.

**pidxunicode**

Puntatore a una struttura [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) se il valore di JET_bitIndexUnicode è specificato nel parametro *grbit* . Ciò consente all'utente di specificare i flag personalizzati che vengono passati alla funzione [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) durante la normalizzazione Unicode.

**cbVarSegMac**

Lunghezza massima, in byte, di ogni colonna da archiviare nell'indice quando il valore JET_bitIndexTupleLimits non viene specificato nel parametro *grbit* .

La specifica di un valore pari a 0 (zero) per questo campo è equivalente a:

  - Specifica JET_cbPrimaryKeyMost per un indice primario.

  - Specifica JET_cbSecondaryKeyMost per un indice secondario.

**ptuplelimits**

Puntatore a una struttura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) se il valore di JET_bitIndexTupleLimits è specificato nel parametro *grbit* .

ptuplelimits è stato introdotto in Windows Server 2003.

**rgconditionalcolumn**

Parametro facoltativo di una matrice di strutture di [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , utilizzate per specificare le colonne condizionali nell'indice.

**cConditionalColumn**

Numero di strutture nella matrice **rgconditionalcolumn** .

**Err**

Contiene il codice restituito per la creazione di questo indice.

**cbKeyMost**

Specifica la dimensione massima consentita, in byte, per le chiavi nell'indice. Questo parametro viene ignorato se il valore JET_bitIndexKeyMost non è specificato nel parametro *grbit* . Se questo parametro è impostato su zero e JET_bitIndexKeyMost viene specificato nel parametro *grbit* , la funzione chiamante avrà esito negativo con JET_err_InvalidDef.

Le dimensioni minime massime supportate per la chiave sono JET_cbKeyMostMin (255), ovvero la dimensione massima della chiave legacy.

Le dimensioni massime della chiave dipendono dalle dimensioni della pagina del database (JET_paramDatabasePageSize), come indicato di seguito:

  - Se JET_paramDatabasePageSize = 2048 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Se JET_paramDatabasePageSize = 4096 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Se JET_paramDatabasePageSize = 8192 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

Le dimensioni massime supportate per l'istanza possono essere lette anche dal parametro di sistema JET_paramKeyMost.

**cbKeyMost** è stato introdotto in Windows Vista.

### <a name="remarks"></a>Commenti

ESE supporta l'indicizzazione su colonne chiave contenenti più valori. Per usare questa funzionalità, la colonna deve essere un tipo di colonna con tag (JET_bitColumnTagged) ed è necessario contrassegnarla per avere più valori indicizzati con JET_bitColumnMultiValued. Nelle versioni di Windows precedenti a Windows Vista, solo la prima colonna chiave multivalore nell'indice avrà i valori espansi nell'indice. Tutte le altre colonne multivalore e con tag avranno solo i primi valori espansi nell'indice.

Supponendo che le righe seguenti siano presenti in una tabella (la colonna alfa non è multivalore, mentre le colonne beta, gamma e Delta sono multivalore) e viene creato un indice come "+ Alpha \\ 0 + Beta \\ 0 + gamma \\ 0 + Delta \\ 0 \\ 0":

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Alfa</p></th>
<th><p>Beta</p></th>
<th><p>Gamma</p></th>
<th><p>Delta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>ABC<br />
GHI<br />
JKL</p></td>
<td><p>MNO<br />
PQR<br />
S</p></td>
<td><p>VWX<br />
YZ</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>IL</p></td>
<td><p>PIOGGIA<br />
Spagna</p></td>
<td><p>IN<br />
RIENTRA</p></td>
</tr>
</tbody>
</table>


Verranno archiviate le tuple degli indici in calo:

{1, ABC, MNO, VWX}  
{1, GHI, MNO, VWX}  
{1, JKL, MNO, VWX}  
{2,, PIOGGIA, IN}

Si noti che {2,, SPAIN, IN} non è archiviato, anche se la colonna Alpha nella seconda riga ha un singolo valore multivalore.

Nelle versioni di Windows a partire da Windows Vista, tutte le colonne multivalore possono essere espanse nell'indice specificando JET_bitIndexCrossProduct.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JET_ INDEXCREATE_W</strong> (Unicode) e <strong>JET_ INDEXCREATE_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
