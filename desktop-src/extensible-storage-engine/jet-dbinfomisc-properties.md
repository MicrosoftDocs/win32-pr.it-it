---
description: 'Altre informazioni su: Proprietà JET_DBINFOMISC'
title: Proprietà JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc_properties(v=EXCHG.10)
ms:contentKeyID: 39515692
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 43f65126c3c257f2e0c9c7735348befa44198729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749895"
---
# <a name="jet_dbinfomisc-properties"></a>Proprietà JET_DBINFOMISC

Includi membri protetti  
Includi membri ereditati  

Il tipo di [JET_DBINFOMISC](./jet-dbinfomisc-class.md) espone i membri seguenti.

## <a name="properties"></a>Proprietà

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh578821(v=exchg.10).md">bkinfoCopyPrev</a></td>
<td>Ottiene informazioni sull'ultimo backup di copia riuscito.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh565264(v=exchg.10).md">bkinfoDiffPrev</a></td>
<td>Ottiene informazioni sull'ultimo backup differenziale riuscito. Reimposta quando <a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a> è impostato.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh577657(v=exchg.10).md">bkinfoFullCur</a></td>
<td>Ottiene informazioni sul backup corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a></td>
<td>Ottiene informazioni sull'ultimo backup completo completato correttamente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh564433(v=exchg.10).md">bkinfoIncPrev</a></td>
<td>Ottiene informazioni sull'ultimo backup incrementale riuscito. Questo valore viene reimpostato quando <a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a> è impostato.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh578850(v=exchg.10).md">cbPageSize</a></td>
<td>Ottiene le dimensioni della pagina del database. Il valore 0 indica le pagine 4Kb.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh558061(v=exchg.10).md">dbstate</a></td>
<td>Ottiene lo stato coerente/incoerente del database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh566598(v=exchg.10).md">dwBuildNumber</a></td>
<td>Ottiene il numero di build del sistema operativo dall'ultima connessione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh578966(v=exchg.10).md">dwMajorVersion</a></td>
<td>Ottiene la versione principale del sistema operativo dall'ultima connessione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh596571(v=exchg.10).md">dwMinorVersion</a></td>
<td>Ottiene la versione secondaria del sistema operativo dall'ultima connessione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh564660(v=exchg.10).md">fShadowingDisabled</a></td>
<td>Ottiene un valore che indica se l'ombreggiatura del catalogo è abilitata. Questo valore è solo per uso interno.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh565757(v=exchg.10).md">fUpgradeDb</a></td>
<td>Ottiene un valore che indica se il database è in fase di aggiornamento. Questo valore è solo per uso interno.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh579055(v=exchg.10).md">genCommitted</a></td>
<td>Ottiene la generazione massima di log di cui è stato eseguito il commit nel database. In genere la generazione del log corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh579109(v=exchg.10).md">genMaxRequired</a></td>
<td>Ottiene la generazione massima di log necessaria per la riproduzione dei log.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh565891(v=exchg.10).md">genMinRequired</a></td>
<td>Ottiene la generazione minima di log necessaria per la riproduzione dei log. In genere la generazione del checkpoint.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh577443(v=exchg.10).md">lgposAttach</a></td>
<td>Ottiene il LGPO dell'ultima connessione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh163307(v=exchg.10).md">lgposConsistent</a></td>
<td>Ottiene il LGPO quando il database è stato reso consistente. Questo valore è null se il database è incoerente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh566733(v=exchg.10).md">lgposDetach</a></td>
<td>Ottiene il LGPO dell'ultimo scollegamento.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh564456(v=exchg.10).md">logtimeAttach</a></td>
<td>Ottiene l'ora in cui è stato collegato il database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh566711(v=exchg.10).md">logtimeBadChecksum</a></td>
<td>Ottiene l'ultima volta in cui è stato trovato un errore di checksum non correggibile.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh557946(v=exchg.10).md">logtimeConsistent</a></td>
<td>Ottiene l'ora in cui il database è stato reso consistente. Questo valore è null se il database è incoerente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh556940(v=exchg.10).md">logtimeDetach</a></td>
<td>Ottiene l'ora dell'ultima disconnessione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh557356(v=exchg.10).md">logtimeECCFixFail</a></td>
<td>Ottiene l'ultima volta in cui è stato rilevato un errore di un bit non correggibile.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh578967(v=exchg.10).md">logtimeECCFixSuccess</a></td>
<td>Ottiene l'ultima volta in cui è stato corretto un errore di un bit.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh577625(v=exchg.10).md">logtimeGenMaxCreate</a></td>
<td>Ottiene l'ora di creazione del file di log <a href="hh579109(v=exchg.10).md">genMaxRequired</a> .</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh579510(v=exchg.10).md">logtimeRepair</a></td>
<td>Ottiene l'ultima volta in cui è stato eseguito il ripristino sul database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh565142(v=exchg.10).md">lSPNumber</a></td>
<td>Ottiene il numero del Service Pack del sistema operativo dall'ultima connessione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh564996(v=exchg.10).md">signDb</a></td>
<td>Ottiene la firma del database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh578351(v=exchg.10).md">signLog</a></td>
<td>Ottiene la firma logfile dei log utilizzati per modificare il database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh596347(v=exchg.10).md">ulBadChecksum</a></td>
<td>Ottiene il numero di volte in cui è stato trovato un errore di checksum non correggibile.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh557876(v=exchg.10).md">ulBadChecksumOld</a></td>
<td>Ottiene il numero di volte in cui è stato rilevato un errore di checksum non correggibile prima dell'ultimo ripristino.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh566254(v=exchg.10).md">ulECCFixFail</a></td>
<td>Ottiene il numero di volte in cui è stato rilevato un errore di un bit non correggibile.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh564490(v=exchg.10).md">ulECCFixFailOld</a></td>
<td>Ottiene il numero di volte in cui è stato rilevato un errore di un bit non correggibile.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh578574(v=exchg.10).md">ulECCFixSuccess</a></td>
<td>Ottiene il numero di volte in cui un errore di un bit è stato corretto correttamente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh578638(v=exchg.10).md">ulECCFixSuccessOld</a></td>
<td>Ottiene il numero di volte in cui un errore di un bit è stato corretto prima dell'ultimo ripristino.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh579357(v=exchg.10).md">ulRepairCount</a></td>
<td>Ottiene il numero di volte in cui è stato chiamato il metodo Repair sul database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh557020(v=exchg.10).md">ulRepairCountOld</a></td>
<td>Ottiene il numero di volte in cui il database è stato ripristinato prima dell'ultima deframmentazione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh596219(v=exchg.10).md">ulUpdate</a></td>
<td>Ottiene la versione incrementale di ESENT che ha creato il database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh577854(v=exchg.10).md">ulVersion</a></td>
<td>Ottiene la versione di ESENT che ha creato il database.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_DBINFOMISC](./jet-dbinfomisc-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
