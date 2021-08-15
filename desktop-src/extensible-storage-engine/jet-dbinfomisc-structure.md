---
description: 'Altre informazioni su: JET_DBINFOMISC struttura'
title: Struttura JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
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
ms.openlocfilehash: 6c7684fe69cff252d75ea2cceb0872044e8a011b39e88375d6eb576cb1b5360e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118486334"
---
# <a name="jet_dbinfomisc-structure"></a>Struttura JET_DBINFOMISC


_**Si applica a:** Windows | Windows Server_

## <a name="jet_dbinfomisc-structure"></a>Struttura JET_DBINFOMISC

La **JET_DBINFOMISC** contiene informazioni varie su un database. Si tratta delle informazioni contenute nell'intestazione del database.

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
    } JET_DBINFOMISC;
```

### <a name="members"></a>Membri

**ulVersion**

Versione nativa del motore di database che ha creato il database. Vedere [JetGetVersion per](./jetgetversion-function.md) recuperare la versione nativa per il motore di database corrente.

**ulUpdate**

Tiene traccia degli aggiornamenti incrementali del formato di database compatibili con le versioni precedenti.

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
<td><p>0x620,0</p></td>
<td><p>Formato beta del sistema operativo originale (22/4/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620,1</p></td>
<td><p>Aggiungere colonne nel catalogo per l'indicizzazione condizionale e OLD (29/5/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,2</p></td>
<td><p>Aggiungere il flag fLocalizedText in IDB (5/6/97).</p></td>
</tr>
<tr class="even">
<td><p>0x620,3</p></td>
<td><p>Aggiungere SPLIT_BUFFER alle pagine radice dell'albero dello spazio (30/10/97).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,2</p></td>
<td><p>Ripristinare la revisione per mantenere la compatibilità con ESE97 (28/01/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620,3</p></td>
<td><p>Aggiungere nuove colonne con tag al catalogo ( &quot; CallbackData &quot; e &quot; CallbackDependencies &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,4</p></td>
<td><p>Supporto SLV: signSLV, fSLVExists nell'intestazione db (5/5/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620,5</p></td>
<td><p>Nuovo albero dello spazio SLV (29/5/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,6</p></td>
<td><p>Mappa spaziatrice SLV (12/10/98).</p></td>
</tr>
<tr class="even">
<td><p>0x620,7</p></td>
<td><p>IDXSEG a 4 byte (10/12/98).</p></td>
</tr>
<tr class="odd">
<td><p>0x620,8</p></td>
<td><p>Nuovo formato di colonna modello (25/1/99).</p></td>
</tr>
<tr class="even">
<td><p>0x620,9</p></td>
<td><p>Colonne modello ordinate (24/6/99).</p></td>
</tr>
<tr class="odd">
<td><p>0x623,0</p></td>
<td><p>New Space Manager (15/5/99).</p></td>
</tr>
</tbody>
</table>


**signDb**

Firma del database (inclusa l'ora di creazione). Questa struttura è di 28 byte.

**dbstate**

Questo è lo stato del database.

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
<td><p>Per poter essere utilizzato o spostato, il database richiede l'esecuzione di un ripristino rigido o soft. Non è consigliabile provare a spostare i database in questo stato.</p></td>
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

Null se il database si trova in uno stato dirty. Si tratta della posizione del log utilizzata per l'ultima volta che il database è stato portato a uno stato di arresto pulito.

**logtimeConsistent**

Null se il database si trova in uno stato dirty. Si tratta dell'ora dell'ultimo arresto del database.

**logtimeAttach**

Ora dell'ultimo collegamento del database [con JetAttachDatabase](./jetattachdatabase-function.md).

**lgposAttach**

Posizione del log utilizzata l'ultima volta in cui il database è stato collegato [con JetAttachDatabase](./jetattachdatabase-function.md).

**logtimeDetach**

Ora dell'ultimo scollegamento del database [con JetDetachDatabase](./jetdetachdatabase-function.md).

**lgposDetach**

Posizione del log utilizzata l'ultima volta in cui il database è stato scollegato [con JetDetachDatabase](./jetdetachdatabase-function.md).

**signLog**

Supporta l'infrastruttura ESE e non può essere usato nel codice.

**bkinfoFullPrev**

Supporta l'infrastruttura ESE e non può essere usato nel codice.

**bkinfoIncPrev**

Supporta l'infrastruttura ESE e non può essere usato nel codice.

**bkinfoFullCur**

Supporta l'infrastruttura ESE e non può essere usato nel codice.

**fShadowingDisabled**

Supporta l'infrastruttura ESE e non può essere usato nel codice.

**fUpgradeDb**

Supporta l'infrastruttura ESE e non può essere usato nel codice.

**dwMajorVersion**

Rappresenta i Windows NT di versione quando sono stati aggiornati gli indici dei database. Utilizzato per l'aggiornamento degli indici.

**dwMinorVersion**

Rappresenta i Windows NT di versione quando sono stati aggiornati gli indici dei database. Utilizzato per l'aggiornamento degli indici.

**dwBuildNumber**

Rappresenta i Windows NT di versione quando sono stati aggiornati gli indici dei database. Usato per l'aggiornamento degli indici.

**lSPNumber**

Rappresenta i Windows NT di versione quando gli indici dei database sono stati aggiornati. Usato per l'aggiornamento degli indici.

**cbPageSize**

Dimensioni della pagina del database. 0 indica che le dimensioni della pagina sono di 4 KB.

Questo valore viene recuperato solo se JET_DbInfoMisc è stato passato a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) [o JetGetDatabaseFileInfo.](./jetgetdatabasefileinfo-function.md)

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
<td><p>Dichiarato in Esent.h.</p></td>
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
