---
description: 'Altre informazioni su: struttura JET_DBINFOMISC4'
title: Struttura JET_DBINFOMISC4
TOCTitle: JET_DBINFOMISC4 Structure
ms:assetid: 63f446bc-98b7-4a60-9575-d6b4757fb0fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269269(v=EXCHG.10)
ms:contentKeyID: 32765571
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e2242b1e419c4834a2a1843165e1c9a2ad1f2de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305787"
---
# <a name="jet_dbinfomisc4-structure"></a>Struttura JET_DBINFOMISC4


_**Si applica a:** Windows | Windows Server_

## <a name="jet_dbinfomisc4-structure"></a>Struttura JET_DBINFOMISC4

La struttura **JET_DBINFOMISC4** include informazioni varie su un database. Si tratta delle informazioni contenute nell'intestazione del database.

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
      unsigned long genCommitted;
      JET_BKINFO bkinfoCopyPrev;
      JET_BKINFO bkinfoDiffPrev;
    } JET_DBINFOMISC4;
```

### <a name="members"></a>Membri

**ulVersion**

Versione nativa del motore di database che ha creato il database. Vedere [JetGetVersion](./jetgetversion-function.md) per recuperare la versione nativa per il motore di database corrente.

**ulUpdate**

Tiene traccia degli aggiornamenti del formato del database incrementale che sono compatibili con le versioni precedenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ulVersion, ulUpdate =</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0x620, 0</p></td>
<td><p>Formato beta originale del sistema operativo (4/22/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 1</p></td>
<td><p>Aggiungere le colonne nel catalogo per l'indicizzazione condizionale e quella precedente (5/29/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Aggiungere il flag fLocalizedText in IDB (6/5/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Aggiungere SPLIT_BUFFER alle pagine radice dell'albero dello spazio (10/30/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 2</p></td>
<td><p>Ripristinare la revisione affinché ESE97 rimanga compatibile con le versioni successive (1/28/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 3</p></td>
<td><p>Aggiungere nuove colonne con tag al catalogo ( &quot; CallbackData &quot; e &quot; CallbackDependencies &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 4</p></td>
<td><p>Supporto di SLV: signSLV, fSLVExists nell'intestazione DB (5/5/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 5</p></td>
<td><p>Nuovo albero dello spazio SLV (5/29/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 6</p></td>
<td><p>Mappa dello spazio SLV (10/12/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 7</p></td>
<td><p>IDXSEG a 4 byte (12/10/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 8</p></td>
<td><p>Nuovo formato di colonna modello (1/25/99).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 9</p></td>
<td><p>Colonne modello ordinate (6/24/99).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, A</p></td>
<td><p>Codebase unita (3/26/2003).</p></td>
</tr>
<tr class="even">
<td><p>0x620, B</p></td>
<td><p>Nuovo formato di checksum (1/08/2004).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, C</p></td>
<td><p>Aumento della lunghezza massima della chiave a 1000/2000 byte per le pagine 4/8KB (1/15/2004).</p></td>
</tr>
<tr class="even">
<td><p>0x620, D</p></td>
<td><p>Hint dello spazio del catalogo space_header. V2 (7/15/2007).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, E</p></td>
<td><p>Aggiungere il nuovo formato di nodo/extent a gestione spazio, usarlo per i pool di spazio riservati (8/9/2007).</p></td>
</tr>
<tr class="even">
<td><p>0x620, F</p></td>
<td><p>Compressione per valori Long intrinseci (10/30/2007).</p></td>
</tr>
<tr class="odd">
<td><p>0x620, 10</p></td>
<td><p>Compressione per valori Long separati (12/05/2007).</p></td>
</tr>
<tr class="even">
<td><p>0x620, 11</p></td>
<td><p>Nuove dimensioni del blocco LV per pagine di grandi dimensioni (12/29/2007).</p></td>
</tr>
</tbody>
</table>


**signDb**

Firma del database (inclusa l'ora di creazione). Questa struttura è di 28 byte.

**dbstate**

Si tratta dello stato del database.

Per questo membro sono disponibili le opzioni seguenti.

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
<td><p>JET_dbstateJustCreated<br />
1</p></td>
<td><p>Il database è stato appena creato.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateDirtyShutdown<br />
2</p></td>
<td><p>Il database richiede l'esecuzione di un ripristino software o hardware per poter essere utilizzato o spostabile. Non provare a spostare i database in questo stato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateCleanShutdown<br />
3</p></td>
<td><p>Il database è in uno stato pulito. Il database può essere collegato senza file di log.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbstateBeingConverted<br />
4</p></td>
<td><p>È in corso l'aggiornamento del database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_dbstateForceDetach<br />
5</p></td>
<td><p>Interno.</p></td>
</tr>
</tbody>
</table>


**lgposConsistent**

Null se il database è in uno stato dirty. Si tratta della posizione del log utilizzata quando il database è stato portato per l'ultima volta a uno stato di chiusura normale.

**logtimeConsistent**

Null se il database è in uno stato dirty. Si tratta dell'ora in cui il database è stato portato per l'ultima volta a uno stato di chiusura normale.

**logtimeAttach**

Ora dell'ultima connessione del database con [JetAttachDatabase](./jetattachdatabase-function.md).

**lgposAttach**

Posizione del log utilizzata per l'ultima volta che il database è stato collegato a [JetAttachDatabase](./jetattachdatabase-function.md).

**logtimeDetach**

Data e ora dell'ultimo scollegamento del database con [JetDetachDatabase](./jetdetachdatabase-function.md).

**lgposDetach**

Posizione del log utilizzata per l'ultima volta in cui il database è stato scollegato con [JetDetachDatabase](./jetdetachdatabase-function.md).

**signLog**

Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.

**bkinfoFullPrev**

Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.

**bkinfoIncPrev**

Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.

**bkinfoFullCur**

Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.

**fShadowingDisabled**

Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.

**fUpgradeDb**

Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.

**dwMajorVersion**

Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database. Utilizzato per l'aggiornamento degli indici.

**dwMinorVersion**

Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database. Utilizzato per l'aggiornamento degli indici.

**dwBuildNumber**

Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database. Utilizzato per l'aggiornamento degli indici.

**lSPNumber**

Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database. Utilizzato per l'aggiornamento degli indici.

**cbPageSize**

Dimensioni di pagina del database. 0 indica che le dimensioni della pagina sono pari a 4 KB.

Questo valore viene recuperato solo se JET_DbInfoMisc è stato passato a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).

**genMinRequired**

Rappresenta la generazione minima di log necessaria per la riproduzione dei log. Questa operazione viene in genere utilizzata come generazione del checkpoint.

**genMaxRequired**

Rappresenta la generazione massima di log necessaria per la riproduzione dei log.

**logtimeGenMaxCreate**

Rappresenta la data e l'ora di creazione del file di log genMax.

**ulRepairCount**

Numero di volte in cui è stata richiamata una riparazione su questo database.

**logtimeRepair**

Rappresenta la data e l'ora in cui è stato eseguito l'ultimo ripristino.

**ulRepairCountOld**

Il numero di volte in cui la riparazione è stata eseguita nel database prima dell'ultima deframmentazione.

**ulECCFixSuccess**

Il numero di volte in cui è stato corretto un errore di un bit che ha generato una pagina corretta.

**logtimeECCFixSuccess**

Rappresenta la data e l'ora in cui è stato corretto l'ultimo errore di un bit ed è stata generata una pagina corretta.

**ulECCFixSuccessOld**

Rappresenta il numero di volte in cui è stato corretto un errore di un bit e ha generato una pagina corretta prima dell'ultima correzione.

**ulECCFixFail**

Il numero di volte in cui è stato corretto un errore di un bit e il risultato è una pagina non valida.

**logtimeECCFixFail**

Rappresenta la data e l'ora in cui è stato corretto l'ultimo errore di un bit ed è stata generata una pagina non valida.

**ulECCFixFailOld**

Il numero di volte in cui è stato corretto un errore di un bit che ha generato una pagina errata prima dell'ultima correzione.

**ulBadChecksum**

Il numero di volte in cui è stato trovato un errore ECC/checksum non correggibile.

**logtimeBadChecksum**

Rappresenta la data e l'ora in cui è stato rilevato l'ultimo errore ECC/checksum non correggibile.

**ulBadChecksumOld**

Il numero di volte in cui è stato trovato un errore ECC/checksum non correggibile prima dell'ultimo ripristino.

**genCommitted**

Numero massimo di generazioni di log di cui è stato eseguito il commit nel database. In genere la generazione del log corrente.

**bkinfoCopyPrev**

Ultimo backup di copia riuscito.

**bkinfoDiffPrev**

Ultimo backup differenziale riuscito. Questo valore viene reimpostato quando bkinfoFullPrev è impostato.

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
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_SIGNATURE](./jet-signature-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
