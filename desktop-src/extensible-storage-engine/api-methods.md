---
description: 'Altre informazioni su: Metodi API'
title: Metodi API
TOCTitle: Api methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api_methods(v=EXCHG.10)
ms:contentKeyID: 55100697
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 75a2c7e81952b7afdbb73eb75228314f8ae3c77a35329626975fc6f5b03dee8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272829"
---
# <a name="api-methods"></a>Metodi API

Includere membri protetti  
Includi membri ereditati  

Il [tipo API](./api-class.md) espone i membri seguenti.

## <a name="methods"></a>Metodi

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292138(v=exchg.10).md">DeserializeObjectFromColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Deserializzare un oggetto da una colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292115(v=exchg.10).md">DeserializeObjectFromColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Deserializzare un oggetto da una colonna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292114(v=exchg.10).md">EscrowUpdate</a></td>
<td>Eseguire l'addizione atomica su una colonna. La colonna deve essere di tipo <a href="hh577895(v=exchg.10).md">Long.</a> Questa funzione consente a più sessioni di aggiornare lo stesso record contemporaneamente senza conflitti.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292099(v=exchg.10).md">GetBookmark</a></td>
<td>Recupera il segnalibro per il record associato alla voce di indice nella posizione corrente di un cursore. Questo segnalibro può quindi essere usato per riposizionare il cursore sullo stesso record usando JetGotoBookmark.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292098(v=exchg.10).md">GetColumnDictionary</a></td>
<td>Crea un dizionario che esegue il mapping dei nomi di colonna ai relativi ID colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292101(v=exchg.10).md">GetTableColumnid</a></td>
<td>Ottiene il valore columnid della colonna specificata.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292090(v=exchg.10).md">GetTableColumns(JET_SESID, JET_TABLEID)</a></td>
<td>Scorre tutte le colonne della tabella, restituisce informazioni su ognuna di queste colonne.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292089(v=exchg.10).md">GetTableColumns(JET_SESID, JET_DBID, String)</a></td>
<td>Scorre tutte le colonne della tabella, restituisce informazioni su ognuna di queste colonne.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292093(v=exchg.10).md">GetTableIndexes(JET_SESID, JET_TABLEID)</a></td>
<td>Scorre tutti gli indici nella tabella, restituisce informazioni su ognuno di essi.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292092(v=exchg.10).md">GetTableIndexes(JET_SESID, JET_DBID, String)</a></td>
<td>Scorre tutti gli indici nella tabella, restituisce informazioni su ognuno di essi.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292095(v=exchg.10).md">GetTableNames</a></td>
<td>Restituisce i nomi delle tabelle nel database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292094(v=exchg.10).md">IntersectIndexes</a></td>
<td>Interseca un gruppo di intervalli di indici e restituisce i segnalibri dei record presenti in tutti gli intervalli di indici. Vedere anche <a href="dn292212(v=exchg.10).md">JetIntersectIndexes(JET_SESID, [], Int32, JET_RECORDLIST, IntersectIndexesGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292097(v=exchg.10).md">JetAddColumn</a></td>
<td>Aggiungere una nuova colonna a una tabella esistente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292096(v=exchg.10).md">JetAttachDatabase</a></td>
<td>Collega un file di database da utilizzare con un'istanza del database. Per usare il database, sarà necessario aprirlo successivamente con <a href="dn292219(v=exchg.10).md">JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292100(v=exchg.10).md">JetAttachDatabase2</a></td>
<td>Collega un file di database da utilizzare con un'istanza del database. Per usare il database, sarà necessario aprirlo successivamente con <a href="dn292219(v=exchg.10).md">JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292102(v=exchg.10).md">JetBackupInstance</a></td>
<td>Esegue un backup di flusso di un'istanza di , inclusi tutti i database collegati, in una directory. Con più metodi di backup supportati dal motore, questa è la funzione più semplice e incapsulata.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance</a></td>
<td>Avvia un backup esterno mentre il motore e il database sono online e attivi.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292103(v=exchg.10).md">JetBeginSession</a></td>
<td>Inizializzare una nuova sessione ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292105(v=exchg.10).md">JetBeginTransaction</a></td>
<td>Determina l'immissione di una transazione in una sessione o la creazione di un nuovo punto di salvataggio in una transazione esistente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292106(v=exchg.10).md">JetBeginTransaction2</a></td>
<td>Determina l'immissione di una transazione in una sessione o la creazione di un nuovo punto di salvataggio in una transazione esistente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292107(v=exchg.10).md">JetCloseDatabase</a></td>
<td>Chiude un file di database precedentemente aperto con <a href="dn292219(v=exchg.10).md">JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit) o</a> creato con <a href="dn292118(v=exchg.10).md">JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292108(v=exchg.10).md">JetCloseFileInstance</a></td>
<td>Chiude un file aperto con JetOpenFileInstance dopo l'estrazione dei dati da tale file tramite JetReadFileInstance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292109(v=exchg.10).md">JetCloseTable</a></td>
<td>Chiudere una tabella aperta.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292110(v=exchg.10).md">JetCommitTransaction</a></td>
<td>Esegue il commit delle modifiche apportate allo stato del database durante il punto di salvataggio corrente ed esegue la migrazione al punto di salvataggio precedente. Se viene eseguito il commit del punto di salvataggio più esterno, verrà eseguito il commit delle modifiche apportate durante tale punto di salvataggio allo stato del database e la sessione chiuderà la transazione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292112(v=exchg.10).md">JetCompact</a></td>
<td>Crea una copia di un database esistente. La copia viene compattata in uno stato ottimale per l'utilizzo. I dati nei dati copiati verranno imballati in base alle misure scelte per gli indici in fase di creazione dell'indice. In questo modo, i dati compattati possono essere archiviati nel modo più denso possibile. In alternativa, i dati compattati possono riservare spazio per la successiva crescita di record o inserimenti di indici.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292113(v=exchg.10).md">JetComputeStats</a></td>
<td>Illustra ogni indice di una tabella per calcolare esattamente il numero di voci in un indice e il numero di chiavi distinte in un indice. Queste informazioni, insieme al numero di pagine di database allocate per un indice e all'ora corrente del calcolo, vengono archiviate nei metadati dell'indice nel database. Questi dati possono essere recuperati successivamente con operazioni di informazioni.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292118(v=exchg.10).md">JetCreateDatabase</a></td>
<td>Crea e collega un file di database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292120(v=exchg.10).md">JetCreateDatabase2</a></td>
<td>Crea e collega un file di database con le dimensioni massime del database specificate.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292121(v=exchg.10).md">JetCreateIndex</a></td>
<td>Crea un indice sui dati in un database ESE. Un indice può essere usato per individuare rapidamente dati specifici.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292123(v=exchg.10).md">JetCreateIndex2</a></td>
<td>Crea indici sui dati in un database ESE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292122(v=exchg.10).md">JetCreateInstance</a></td>
<td>Alloca una nuova istanza del motore di database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292126(v=exchg.10).md">JetCreateInstance2</a></td>
<td>Allocare una nuova istanza del motore di database per l'uso in un singolo processo, con un nome visualizzato specificato.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292127(v=exchg.10).md">JetCreateTable</a></td>
<td>Creare una tabella vuota. La tabella appena creata viene aperta in modo esclusivo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3</a></td>
<td>Crea una tabella, aggiunge colonne e indici in tale tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292130(v=exchg.10).md">JetDefragment</a></td>
<td>Avvia e arresta le attività di deframmentazione del database che migliorano l'organizzazione dei dati all'interno di un database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292145(v=exchg.10).md">JetDefragment2</a></td>
<td>Avvia e arresta le attività di deframmentazione del database che migliorano l'organizzazione dei dati all'interno di un database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292131(v=exchg.10).md">JetDelete</a></td>
<td>Elimina il record corrente in una tabella di database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292133(v=exchg.10).md">JetDeleteColumn</a></td>
<td>Elimina una colonna da una tabella di database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292132(v=exchg.10).md">JetDeleteColumn2</a></td>
<td>Elimina una colonna da una tabella di database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292135(v=exchg.10).md">JetDeleteIndex</a></td>
<td>Elimina un indice da una tabella di database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292134(v=exchg.10).md">JetDeleteTable</a></td>
<td>Elimina una tabella da un database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292139(v=exchg.10).md">JetDetachDatabase</a></td>
<td>Rilascia un file di database precedentemente collegato a una sessione di database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292136(v=exchg.10).md">JetDetachDatabase2</a></td>
<td>Rilascia un file di database precedentemente collegato a una sessione di database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292137(v=exchg.10).md">JetDupCursor</a></td>
<td>Duplica un cursore aperto e restituisce un handle al cursore duplicato. Se il cursore duplicato è un cursore di sola lettura, anche il cursore duplicato è un cursore di sola lettura. Qualsiasi stato correlato alla costruzione di una chiave di ricerca o all'aggiornamento di un record non viene copiato nel cursore duplicato. Inoltre, la posizione del cursore originale non viene duplicata nel cursore duplicato. Il cursore duplicato viene sempre aperto nell'indice cluster e la relativa posizione è sempre sulla prima riga della tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292140(v=exchg.10).md">Sessione JetDupSession</a></td>
<td>Inizializza una nuova sessione ESE nella stessa istanza del sesid specificato.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292142(v=exchg.10).md">JetEndExternalBackupInstance</a></td>
<td>Termina una sessione di backup esterna. Questa API è l'ultima API di una serie di API che devono essere chiamate per eseguire correttamente un backup online (non basato su VSS).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292143(v=exchg.10).md">JetEndExternalBackupInstance2</a></td>
<td>Termina una sessione di backup esterna. Questa API è l'ultima API di una serie di API che devono essere chiamate per eseguire correttamente un backup online (non basato su VSS).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292144(v=exchg.10).md">JetEndSession</a></td>
<td>Termina una sessione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292148(v=exchg.10).md">JetEnumerateColumns</a></td>
<td>Recupera in modo efficiente un set di colonne e i relativi valori dal record corrente di un cursore o dal buffer di copia del cursore. Le colonne e i valori recuperati possono essere limitati da un elenco di ID di colonna, numeri itagSequence e altre caratteristiche. Questa API di recupero colonna è univoca perché restituisce informazioni nella memoria allocata dinamicamente ottenuta usando un callback compatibile con la rialloca fornito dall'utente. Questa nuova flessibilità consente il recupero efficiente dei dati della colonna con caratteristiche specifiche, ad esempio dimensioni e molteplicità, sconosciute al chiamante. In questo modo si elimina la necessità di usare le modalità di individuazione di JetRetrieveColumn per determinare tali caratteristiche per configurare una chiamata finale a JetRetrieveColumn che recupererà correttamente i dati desiderati.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292150(v=exchg.10).md">JetEscrowUpdate</a></td>
<td>Esegue un'operazione di addizione atomica su una colonna. Questa funzione consente a più sessioni di aggiornare lo stesso record contemporaneamente senza conflitti. Vedere anche <a href="dn292114(v=exchg.10).md">EscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292147(v=exchg.10).md">JetFreeBuffer</a></td>
<td>Libera la memoria allocata da una chiamata al motore di database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292154(v=exchg.10).md">JetGetAttachInfoInstance</a></td>
<td>Utilizzato durante un backup avviato da <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)</a> per eseguire una query su un'istanza per i nomi dei file di database che devono far parte del set di file di backup. Verranno considerati solo i database attualmente collegati all'istanza tramite <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit).</a> Questi file possono essere successivamente aperti usando <a href="dn292230(v=exchg.10).md">JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> e letti <a href="dn332987(v=exchg.10).md">usando JetReadFileInstance(JET_INSTANCE, JET_HANDLE, [], Int32, Int32).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292149(v=exchg.10).md">JetGetBookmark</a></td>
<td>Recupera il segnalibro per il record associato alla voce di indice nella posizione corrente di un cursore. Questo segnalibro può quindi essere usato per riposizionare il cursore nello stesso record usando <a href="dn292200(v=exchg.10).md">JetGotoBookmark(JET_SESID, JET_TABLEID, [], Int32)</a>. Il segnalibro non sarà più lungo di <a href="dn351215(v=exchg.10).md">BookmarkMost</a> bytes. Vedere anche <a href="dn292099(v=exchg.10).md">GetBookmark(JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292158(v=exchg.10).md">JetGetColumnInfo(JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)</a></td>
<td>Recupera informazioni su una colonna in una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292151(v=exchg.10).md">JetGetColumnInfo(JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</a></td>
<td>Recupera informazioni su una colonna della tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292152(v=exchg.10).md">JetGetColumnInfo(JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)</a></td>
<td>Recupera informazioni su tutte le colonne di una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292153(v=exchg.10).md">JetGetCurrentIndex</a></td>
<td>Determina il nome dell'indice corrente di un cursore specificato. Questo nome viene usato anche per selezionare nuovamente l'indice in un secondo momento come indice corrente usando <a href="dn334011(v=exchg.10).md">JetSetCurrentIndex(JET_SESID, JET_TABLEID, String).</a> Può essere usato anche per individuare le proprietà dell'indice tramite JetGetTableIndexInfo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292155(v=exchg.10).md">JetGetCursorInfo</a></td>
<td>Determinare se un aggiornamento del record corrente di un cursore determinerà un conflitto di scrittura, in base allo stato di aggiornamento corrente del record. È possibile che alla fine verrà restituito un conflitto di scrittura anche se JetGetCursorInfo viene restituito correttamente. perché un'altra sessione può aggiornare il record prima che la sessione corrente sia in grado di aggiornare lo stesso record.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292159(v=exchg.10).md">JetGetDatabaseFileInfo(String, JET_DBINFOMISC, JET_DbInfo)</a></td>
<td>Recupera determinate informazioni sul database specificato.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292161(v=exchg.10).md">JetGetDatabaseFileInfo(String, Int32, JET_DbInfo)</a></td>
<td>Recupera determinate informazioni sul database specificato.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292160(v=exchg.10).md">JetGetDatabaseFileInfo(String, Int64, JET_DbInfo)</a></td>
<td>Recupera determinate informazioni sul database specificato.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292162(v=exchg.10).md">JetGetDatabaseInfo(JET_SESID, JET_DBID, JET_DBINFOMISC, JET_DbInfo)</a></td>
<td>Recupera determinate informazioni sul database specificato.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292164(v=exchg.10).md">JetGetDatabaseInfo(JET_SESID, JET_DBID, Int32, JET_DbInfo)</a></td>
<td>Recupera determinate informazioni sul database specificato.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292167(v=exchg.10).md">JetGetDatabaseInfo(JET_SESID, JET_DBID, String, JET_DbInfo)</a></td>
<td>Recupera determinate informazioni sul database specificato.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292168(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</a></td>
<td><strong>Obsoleto.</strong> Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292172(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292166(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292171(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, Int32, JET_IdxInfo)</a></td>
<td>Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292169(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)</a></td>
<td>Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292173(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</a></td>
<td>Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292170(v=exchg.10).md">JetGetInstanceInfo</a></td>
<td>Recupera informazioni sulle istanze in esecuzione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292175(v=exchg.10).md">JetGetLock</a></td>
<td>Riservare in modo esplicito la possibilità di aggiornare una riga, di scrivere un blocco o di impedire in modo esplicito che una riga venga aggiornata da qualsiasi altra sessione, il blocco di lettura. In genere, i blocchi di scrittura delle righe vengono acquisiti in modo implicito in seguito all'aggiornamento delle righe. I blocchi di lettura non sono in genere necessari a causa del controllo delle versioni dei record. Tuttavia, in alcuni casi una transazione può voler bloccare in modo esplicito una riga per imporre la serializzazione o per garantire che un'operazione successiva avrà esito positivo.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292174(v=exchg.10).md">JetGetLogInfoInstance</a></td>
<td>Utilizzato durante un backup avviato da <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)</a> per eseguire una query su un'istanza per i nomi dei file di patch del database e dei file di log che devono far parte del set di file di backup. Questi file possono essere successivamente aperti usando <a href="dn292230(v=exchg.10).md">JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> e letti <a href="dn332987(v=exchg.10).md">con JetReadFileInstance(JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292177(v=exchg.10).md">JetGetLS</a></td>
<td>Consente all'applicazione di recuperare l'handle di contesto noto come Archiviazione associato a un cursore o alla tabella associata a tale cursore. Questo handle di contesto deve essere stato impostato in precedenza usando <a href="dn334015(v=exchg.10).md">JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)</a>. È anche possibile usare JetGetLS per recuperare contemporaneamente l'handle di contesto corrente per un cursore o una tabella e reimpostare tale handle di contesto.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292179(v=exchg.10).md">JetGetObjectInfo(JET_SESID, JET_DBID, JET_OBJECTLIST)</a></td>
<td>Recupera informazioni sugli oggetti di database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292178(v=exchg.10).md">JetGetObjectInfo(JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)</a></td>
<td>Recupera informazioni sugli oggetti di database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292181(v=exchg.10).md">JetGetRecordPosition</a></td>
<td>Restituisce la posizione frazionaria del record corrente nell'indice corrente sotto forma di JET_RECPOS <a href="dn335256(v=exchg.10).md">struttura</a> . Vedere anche <a href="dn292207(v=exchg.10).md">JetGotoPosition(JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292180(v=exchg.10).md">JetGetSecondaryIndexBookmark</a></td>
<td>Recupera un segnalibro speciale per la voce di indice secondaria nella posizione corrente di un cursore. Questo segnalibro può quindi essere usato per riposizionare in modo efficiente il cursore sulla stessa voce di indice usando JetGotoSecondaryIndexBookmark. Ciò è particolarmente utile quando si riposiziona in un indice secondario che contiene chiavi duplicate o che contiene più voci di indice per lo stesso record.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292182(v=exchg.10).md">JetGetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</a></td>
<td>Ottiene le opzioni di configurazione del database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292185(v=exchg.10).md">JetGetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)</a></td>
<td>Ottiene le opzioni di configurazione del database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292186(v=exchg.10).md">JetGetTableColumnInfo(JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</a></td>
<td>Recupera informazioni su una colonna della tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292187(v=exchg.10).md">JetGetTableColumnInfo(JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)</a></td>
<td>Recupera informazioni su una colonna della tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292189(v=exchg.10).md">JetGetTableColumnInfo(JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)</a></td>
<td>Recupera informazioni su tutte le colonne della tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292191(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</a></td>
<td><strong>Obsoleto.</strong> Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292190(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292196(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292193(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)</a></td>
<td>Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292192(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)</a></td>
<td>Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292195(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</a></td>
<td>Recupera informazioni sugli indici in una tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a></td>
<td>Recupera varie informazioni su una tabella in un database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a></td>
<td>Recupera varie informazioni su una tabella in un database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a></td>
<td>Recupera varie informazioni su una tabella in un database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a></td>
<td>Recupera varie informazioni su una tabella in un database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a></td>
<td>Recupera varie informazioni su una tabella in un database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292199(v=exchg.10).md">JetGetTruncateLogInfoInstance</a></td>
<td>Utilizzato durante un backup avviato da <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)</a> per eseguire una query su un'istanza per i nomi dei file di log delle transazioni che possono essere eliminati in modo sicuro dopo il completamento del backup.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292203(v=exchg.10).md">JetGetVersion</a></td>
<td>Recupera la versione del motore di database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292200(v=exchg.10).md">JetGotoBookmark</a></td>
<td>Posiziona un cursore su una voce di indice per il record associato al segnalibro specificato. Il segnalibro può essere usato con qualsiasi indice definito su una tabella. Il segnalibro per un record può essere recuperato usando <a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292207(v=exchg.10).md">JetGotoPosition</a></td>
<td>Sposta un cursore in una nuova posizione che rappresenta una frazione dell'indice corrente. Vedere anche <a href="dn292181(v=exchg.10).md">JetGetRecordPosition(JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark</a></td>
<td>Posiziona un cursore su una voce di indice associata al segnalibro dell'indice secondario specificato. Il segnalibro dell'indice secondario deve essere usato con lo stesso indice sulla stessa tabella da cui è stato recuperato in origine. Il segnalibro di indice secondario per una voce di indice può essere recuperato usando <a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, [], Int32, [], Int32, GotoSecondaryIndexBookmarkGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292206(v=exchg.10).md">JetGrowDatabase</a></td>
<td>Estende le dimensioni di un database attualmente aperto.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292208(v=exchg.10).md">JetIdle</a></td>
<td>Esegue attività di pulizia inattive o controlla lo stato dell'archivio versioni in ESE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292209(v=exchg.10).md">JetIndexRecordCount</a></td>
<td>Conta il numero di voci nell'indice corrente dalla posizione corrente in avanti. La posizione corrente è inclusa nel conteggio. Il conteggio può essere maggiore del numero totale di record nella tabella se l'indice corrente è su una colonna multivalore e le istanze della colonna hanno più valori. Se la tabella è vuota, verrà restituito 0 per il conteggio.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292210(v=exchg.10).md">JetInit</a></td>
<td>Inizializzare il motore di database ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292214(v=exchg.10).md">JetInit2</a></td>
<td>Inizializzare il motore di database ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292212(v=exchg.10).md">JetIntersectIndexes</a></td>
<td>Calcola l'intersezione tra più set di voci di indice da indici secondari diversi sulla stessa tabella. Questa operazione è utile per trovare il set di record in una tabella che corrispondono a due o più criteri che possono essere espressi tramite intervalli di indici. Vedere anche <a href="dn292094(v=exchg.10).md">IntersectIndexes(JET_SESID, [])</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292216(v=exchg.10).md">JetMakeKey</a></td>
<td>Costruisce chiavi di ricerca che possono quindi essere usate da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292218(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)</a></td>
<td>Spostarsi all'interno di un indice. Il cursore può essere posizionato all'inizio o alla fine dell'indice e spostato avanti e indietro di un numero specificato di voci di indice. Vedere anche <a href="dn334150(v=exchg.10).md">TryMoveFirst(JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast(JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext(JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious(JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a></td>
<td>Spostarsi all'interno di un indice. Il cursore può essere posizionato all'inizio o alla fine dell'indice e spostato avanti e indietro di un numero specificato di voci di indice. Vedere anche <a href="dn334150(v=exchg.10).md">TryMoveFirst(JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast(JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext(JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious(JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292219(v=exchg.10).md">JetOpenDatabase</a></td>
<td>Apre un database collegato in precedenza con <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a>, da usare con una sessione di database. Questa funzione può essere chiamata più volte per lo stesso database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292230(v=exchg.10).md">JetOpenFileInstance</a></td>
<td>Apre un database collegato, un file di patch del database o un file di log delle transazioni di un'istanza attiva allo scopo di eseguire un backup fuzzy di streaming. I dati di questi file possono essere successivamente letti tramite l'handle restituito usando JetReadFileInstance. L'handle restituito deve essere chiuso tramite JetCloseFileInstance. Un backup esterno dell'istanza deve essere stato avviato in precedenza usando JetBeginExternalBackupInstance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292234(v=exchg.10).md">JetOpenTable</a></td>
<td>Apre un cursore su una tabella creata in precedenza.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292231(v=exchg.10).md">JetOpenTempTable</a></td>
<td>Crea una tabella temporanea con un singolo indice. Una tabella temporanea archivia e recupera i record esattamente come una normale tabella creata usando JetCreateTableColumnIndex. Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile. Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando vi si accede in modo puramente sequenziale. Vedere anche <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292232(v=exchg.10).md">JetOpenTempTable2</a></td>
<td>Crea una tabella temporanea con un singolo indice. Una tabella temporanea archivia e recupera i record esattamente come una normale tabella creata usando JetCreateTableColumnIndex. Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile. Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando vi si accede in modo puramente sequenziale. Vedere anche <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292233(v=exchg.10).md">JetOpenTempTable3</a></td>
<td>Crea una tabella temporanea con un singolo indice. Una tabella temporanea archivia e recupera i record esattamente come una normale tabella creata usando JetCreateTableColumnIndex. Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile. Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando vi si accede in modo puramente sequenziale. Vedere anche <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332998(v=exchg.10).md">JetOSSnapshotFreeze</a></td>
<td>Avvia uno snapshot. Mentre lo snapshot è in corso, non è possibile eseguire alcuna attività di scrittura su disco da parte del motore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn292235(v=exchg.10).md">JetOSSnapshotPrepare</a></td>
<td>Avvia i preparativi per una sessione snapshot. Una sessione snapshot è un breve intervallo di tempo in cui il motore non esegue operazioni di I/O di scrittura su disco, in modo che il motore possa partecipare a una sessione di snapshot del volume (se guidata da un writer di snapshot).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332986(v=exchg.10).md">JetOSSnapshotThaw</a></td>
<td>Notifica al motore che può riprendere le normali operazioni di I/O dopo un periodo di blocco e uno snapshot riuscito.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332988(v=exchg.10).md">JetPrepareUpdate</a></td>
<td>Preparare un cursore per l'aggiornamento.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332987(v=exchg.10).md">JetReadFileInstance</a></td>
<td>Recupera il contenuto di un file aperto con <a href="dn292230(v=exchg.10).md">JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332989(v=exchg.10).md">JetRegisterCallback</a></td>
<td>Consente all'applicazione di configurare il motore di database per inviare notifiche all'applicazione per eventi specifici. Queste notifiche sono associate a una tabella specifica e rimangono effettive solo fino a quando l'istanza contenente la tabella non viene arrestata usando <a href="dn334020(v=exchg.10).md">JetTerm(JET_INSTANCE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332990(v=exchg.10).md">JetRenameColumn</a></td>
<td>Modifica il nome di una colonna esistente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332993(v=exchg.10).md">JetRenameTable</a></td>
<td>Modifica il nome di una tabella esistente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332991(v=exchg.10).md">JetResetSessionContext</a></td>
<td>Disassocia una sessione dal thread corrente. Deve essere usato insieme a <a href="dn334027(v=exchg.10).md">JetSetSessionContext(JET_SESID, IntPtr).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332994(v=exchg.10).md">JetResetTableSequential</a></td>
<td>Notifica al motore di database che l'applicazione non esegue più l'analisi dell'intero indice su cui è posizionato il cursore. Questa chiamata inverte una notifica inviata da <a href="dn334018(v=exchg.10).md">JetSetTableSequential(JET_SESID, JET_TABLEID, SetTableSequentialGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332992(v=exchg.10).md">JetRestoreInstance</a></td>
<td>Ripristina e ripristina un backup in streaming di un'istanza di , inclusi tutti i database collegati. È progettato per funzionare con un backup creato con la funzione <a href="dn292102(v=exchg.10).md">JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS).</a> Si tratta della funzione di ripristino più semplice e incapsulata.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332995(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore. In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore. Questa funzione può anche recuperare i dati della colonna da una voce di indice che fa riferimento al record corrente. Oltre a recuperare il valore effettivo della colonna, è anche possibile usare JetRetrieveColumn per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna stessa in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn332997(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore. In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore. Questa funzione può anche recuperare i dati della colonna da una voce di indice che fa riferimento al record corrente. Oltre a recuperare il valore effettivo della colonna, è anche possibile usare JetRetrieveColumn per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna stessa in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334004(v=exchg.10).md">Oggetti JetRetrieveColumns</a></td>
<td>Recupera più valori di colonna dal record corrente in una singola operazione. Una matrice di JET_RETRIEVECOLUMN viene usata per descrivere il set di valori di colonna da recuperare e per descrivere i buffer di output per ogni valore di colonna da recuperare.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334002(v=exchg.10).md">JetRetrieveKey</a></td>
<td>Recupera la chiave per la voce di indice nella posizione corrente di un cursore. Vedere anche <a href="dn334085(v=exchg.10).md">RetrieveKey(JET_SESID, JET_TABLEID, RetrieveKeyGrbit).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334001(v=exchg.10).md">JetRollback</a></td>
<td>Annulla le modifiche apportate allo stato del database e torna all'ultimo punto di salvataggio. JetRollback chiuderà anche tutti i cursori aperti durante il punto di salvataggio. Se il punto di salvataggio più esterno viene annullato, la sessione chiuderà la transazione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334003(v=exchg.10).md">JetSeek</a></td>
<td>Posiziona in modo efficiente un cursore in una voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca in tale cursore e alla disuguaglianza specificata. Una chiave di ricerca deve essere stata creata in precedenza usando <a href="dn292216(v=exchg.10).md">JetMakeKey(JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>. Vedere anche <a href="dn334145(v=exchg.10).md">TrySeek(JET_SESID, JET_TABLEID, SeekGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334009(v=exchg.10).md">JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, SetColumnGrbit, JET_SETINFO)</a></td>
<td>La funzione JetSetColumn modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente. Può sovrascrivere un valore esistente, aggiungere un nuovo valore a una sequenza di valori in una colonna multivalore, rimuovere un valore da una sequenza di valori in una colonna multivalore o aggiornare tutto o parte di un valore long (una colonna di tipo <a href="hh577895(v=exchg.10).md">LongText</a> <a href="hh577895(v=exchg.10).md">o LongBinary).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334008(v=exchg.10).md">JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, SetColumnGrbit, JET_SETINFO)</a></td>
<td>La funzione JetSetColumn modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente. Può sovrascrivere un valore esistente, aggiungere un nuovo valore a una sequenza di valori in una colonna multivalore, rimuovere un valore da una sequenza di valori in una colonna multivalore o aggiornare tutto o parte di un valore long (una colonna di tipo <a href="hh577895(v=exchg.10).md">LongText</a> <a href="hh577895(v=exchg.10).md">o LongBinary).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334010(v=exchg.10).md">JetSetColumnDefaultValue</a></td>
<td>Modifica il valore predefinito di una colonna esistente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334006(v=exchg.10).md">Oggetti JetSetColumns</a></td>
<td>Consente a un'applicazione di impostare più valori di colonna in una singola operazione. Una matrice di <a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a> viene usata per descrivere il set di valori di colonna da impostare e per descrivere i buffer di input per ogni valore di colonna da impostare.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334011(v=exchg.10).md">JetSetCurrentIndex</a></td>
<td>Imposta l'indice corrente di un cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334005(v=exchg.10).md">JetSetCurrentIndex2</a></td>
<td>Imposta l'indice corrente di un cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334012(v=exchg.10).md">JetSetCurrentIndex3</a></td>
<td>Imposta l'indice corrente di un cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334013(v=exchg.10).md">JetSetCurrentIndex4</a></td>
<td>Imposta l'indice corrente di un cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334014(v=exchg.10).md">JetSetDatabaseSize</a></td>
<td>Imposta le dimensioni di un file di database non aperto.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334024(v=exchg.10).md">JetSetIndexRange</a></td>
<td>Limita temporaneamente il set di voci di indice che il cursore può spostarsi usando <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a> a quelli a partire dalla voce di indice corrente e terminando in corrispondenza della voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca nel cursore e ai criteri associati specificati. Una chiave di ricerca deve essere stata creata in precedenza usando <a href="dn292216(v=exchg.10).md">JetMakeKey(JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>. Vedere anche <a href="dn334099(v=exchg.10).md">TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334015(v=exchg.10).md">JetSetLS</a></td>
<td>Consente all'applicazione di associare un handle di contesto noto come local Archiviazione a un cursore o alla tabella associata a tale cursore. Questo handle di contesto può essere utilizzato dall'applicazione per archiviare i dati ausiliari associati a un cursore o a una tabella. L'applicazione viene in seguito notificata tramite un callback di runtime quando è necessario il rilascio dell'handle di contesto. In questo modo è possibile associare lo stato allocato dinamicamente a un cursore o a una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334027(v=exchg.10).md">JetSetSessionContext</a></td>
<td>Associa una sessione al thread corrente utilizzando l'handle di contesto specificato. Questa associazione sostituisce il requisito predefinito del motore in base al cui thread deve essere eseguita una transazione per una determinata sessione. Usare <a href="dn332991(v=exchg.10).md">JetResetSessionContext(JET_SESID)</a> per rimuovere l'associazione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334028(v=exchg.10).md">JetSetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)</a></td>
<td>Imposta le opzioni di configurazione del database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334017(v=exchg.10).md">JetSetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, Int32, String)</a></td>
<td>Imposta le opzioni di configurazione del database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334029(v=exchg.10).md">JetSetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)</a></td>
<td>Imposta le opzioni di configurazione del database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334018(v=exchg.10).md">JetSetTableSequential</a></td>
<td>Notifica al motore di database che l'applicazione sta eseguendo l'analisi dell'intero indice su cui è posizionato il cursore. Di conseguenza, i metodi usati per accedere ai dati dell'indice verranno ottimizzati per rendere questo scenario il più veloce possibile. Vedere anche <a href="dn332994(v=exchg.10).md">JetResetTableSequential(JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334032(v=exchg.10).md">JetStopBackupInstance</a></td>
<td>Impedisce che l'attività correlata al backup di streaming continui in un'istanza in esecuzione specifica, terminando così il backup di streaming in modo prevedibile.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334035(v=exchg.10).md">JetStopServiceInstance</a></td>
<td>Prepara un'istanza per la terminazione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334020(v=exchg.10).md">JetTerm</a></td>
<td>Terminare un'istanza creata con <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> o <a href="dn292122(v=exchg.10).md">JetCreateInstance(JET_INSTANCE, String)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334037(v=exchg.10).md">JetTerm2</a></td>
<td>Terminare un'istanza creata con <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> o <a href="dn292122(v=exchg.10).md">JetCreateInstance(JET_INSTANCE, String)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334022(v=exchg.10).md">JetTruncateLogInstance</a></td>
<td>Utilizzato durante un backup avviato da JetBeginExternalBackup per eliminare tutti i file di log delle transazioni che non saranno più necessari al termine del backup corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334019(v=exchg.10).md">JetUnregisterCallback</a></td>
<td>Configura il motore di database per arrestare l'invio di notifiche all'applicazione come richiesto in precedenza tramite <a href="dn332989(v=exchg.10).md">JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334036(v=exchg.10).md">JetUpdate(JET_SESID, JET_TABLEID)</a></td>
<td>La funzione JetUpdate esegue un'operazione di aggiornamento che include l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente. L'eliminazione di una riga di tabella viene eseguita chiamando <a href="dn292131(v=exchg.10).md">JetDelete(JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334023(v=exchg.10).md">JetUpdate(JET_SESID, JET_TABLEID, [], Int32, Int32)</a></td>
<td>La funzione JetUpdate esegue un'operazione di aggiornamento che include l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente. L'eliminazione di una riga di tabella viene eseguita chiamando <a href="dn292131(v=exchg.10).md">JetDelete(JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334042(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Boolean, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334026(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Byte, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334044(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, [], MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334025(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, DateTime, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334046(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Double, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334030(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334048(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Int16, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334031(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Int32, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334050(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Int64, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334033(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Single, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334052(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334054(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334034(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334038(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)</a></td>
<td>Costruisce una chiave di ricerca che può essere usata da <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334058(v=exchg.10).md">MoveAfterLast</a></td>
<td>Posizionare il cursore dopo l'ultimo record nella tabella. Uno spostamento successivo precedente posizionerà il cursore sull'ultimo record.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334057(v=exchg.10).md">MoveBeforeFirst</a></td>
<td>Posizionare il cursore prima del primo record nella tabella. Uno spostamento successivo posizionerà il cursore sul primo record.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334040(v=exchg.10).md">ResetIndexRange</a></td>
<td>Rimuove un intervallo di indici creato con <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a> o <a href="dn334099(v=exchg.10).md">TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>. Se non è presente alcun intervallo di indici, questo metodo non esegue alcuna operazione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore. In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore. Questa funzione può anche recuperare i dati della colonna da una voce di indice che fa riferimento al record corrente. Oltre a recuperare il valore effettivo della colonna, è possibile usare JetRetrieveColumn anche per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334045(v=exchg.10).md">RetrieveColumnAsBoolean(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valore di colonna booleano dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334078(v=exchg.10).md">RetrieveColumnAsBoolean(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna booleano dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334047(v=exchg.10).md">RetrieveColumnAsByte(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valore di colonna byte dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334074(v=exchg.10).md">RetrieveColumnAsByte(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna byte dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334077(v=exchg.10).md">RetrieveColumnAsDateTime(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valore di colonna datetime dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334051(v=exchg.10).md">RetrieveColumnAsDateTime(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna datetime dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334053(v=exchg.10).md">RetrieveColumnAsDouble(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valore di colonna doppia dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334084(v=exchg.10).md">RetrieveColumnAsDouble(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna doppia dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334056(v=exchg.10).md">RetrieveColumnAsFloat(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valore di colonna float dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334092(v=exchg.10).md">RetrieveColumnAsFloat(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna float dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334093(v=exchg.10).md">RetrieveColumnAsGuid(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valore di colonna GUID dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334061(v=exchg.10).md">RetrieveColumnAsGuid(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna GUID dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334062(v=exchg.10).md">RetrieveColumnAsInt16(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334098(v=exchg.10).md">RetrieveColumnAsInt16(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna int16 dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334100(v=exchg.10).md">RetrieveColumnAsInt32(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334068(v=exchg.10).md">RetrieveColumnAsInt32(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna int32 dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334066(v=exchg.10).md">RetrieveColumnAsInt64(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334091(v=exchg.10).md">RetrieveColumnAsInt64(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334067(v=exchg.10).md">RetrieveColumnAsString(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore. Viene usata la codifica Unicode.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334103(v=exchg.10).md">RetrieveColumnAsString(JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding)</a></td>
<td>Recupera un valore di colonna stringa dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334070(v=exchg.10).md">RetrieveColumnAsString(JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna stringa dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334069(v=exchg.10).md">RetrieveColumnAsUInt16(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valore di colonna uint16 dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334106(v=exchg.10).md">RetrieveColumnAsUInt16(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna uint16 dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334108(v=exchg.10).md">RetrieveColumnAsUInt32(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valore di colonna uint32 dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334073(v=exchg.10).md">RetrieveColumnAsUInt32(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna uint32 dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334072(v=exchg.10).md">RetrieveColumnAsUInt64(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valore di colonna uint64 dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334113(v=exchg.10).md">RetrieveColumnAsUInt64(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera un valore di colonna uint64 dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334075(v=exchg.10).md">RetrieveColumns</a></td>
<td>Recupera le colonne in oggetti ColumnValue.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334076(v=exchg.10).md">RetrieveColumnSize(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera le dimensioni di un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore. In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore. Questa funzione può anche recuperare i dati della colonna da una voce di indice che fa riferimento al record corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334117(v=exchg.10).md">RetrieveColumnSize(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</a></td>
<td>Recupera le dimensioni di un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore. In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore. Questa funzione può anche recuperare i dati della colonna da una voce di indice che fa riferimento al record corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334085(v=exchg.10).md">RetrieveKey</a></td>
<td>Recupera la chiave per la voce di indice nella posizione corrente di un cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334120(v=exchg.10).md">SerializeObjectToColumn</a></td>
<td>Scrivere un formato serializzato di un oggetto in una colonna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334123(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Boolean)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334080(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Byte)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334121(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [])</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334082(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334125(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Double)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334081(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Guid)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334127(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334083(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334130(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334087(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Single)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334132(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334086(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334135(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334089(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], SetColumnGrbit)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334136(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334090(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding, SetColumnGrbit)</a></td>
<td>Modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334138(v=exchg.10).md">SetColumns</a></td>
<td>Imposta le colonne dagli oggetti ColumnValue.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334139(v=exchg.10).md">TryGetLock</a></td>
<td>Riservare in modo esplicito la possibilità di aggiornare una riga, di scrivere un blocco o di impedire in modo esplicito l'aggiornamento di una riga da qualsiasi altra sessione, il blocco di lettura. In genere, i blocchi di scrittura delle righe vengono acquisiti in modo implicito in seguito all'aggiornamento delle righe. I blocchi di lettura non sono in genere necessari a causa del controllo delle versioni dei record. Tuttavia, in alcuni casi una transazione potrebbe voler bloccare in modo esplicito una riga per applicare la serializzazione o per garantire che un'operazione successiva avrà esito positivo.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334094(v=exchg.10).md">TryMove</a></td>
<td>Provare a spostarsi all'interno di un indice. Se la navigazione ha esito positivo, questo metodo restituisce true. Se non è presente alcun record per passare a questo metodo, restituisce false. Verrà generata un'eccezione per altri errori.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334150(v=exchg.10).md">TryMoveFirst</a></td>
<td>Provare a passare al primo record della tabella. Se la tabella è vuota, restituisce false, se viene rilevato un errore diverso viene generata un'eccezione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334140(v=exchg.10).md">TryMoveLast</a></td>
<td>Provare a passare all'ultimo record della tabella. Se la tabella è vuota, restituisce false, se viene rilevato un errore diverso viene generata un'eccezione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334095(v=exchg.10).md">TryMoveNext</a></td>
<td>Provare a passare al record successivo nella tabella. Se non è presente un record successivo, restituisce false, se viene rilevato un errore diverso viene generata un'eccezione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334144(v=exchg.10).md">TryMovePrevious</a></td>
<td>Provare a passare al record precedente nella tabella. Se non è presente un record precedente, restituisce false, se viene rilevato un errore diverso viene generata un'eccezione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334096(v=exchg.10).md">TryOpenTable</a></td>
<td>Provare ad aprire una tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334145(v=exchg.10).md">TrySeek</a></td>
<td>Posiziona in modo efficiente un cursore in una voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca in tale cursore e alla disuguaglianza specificata. Una chiave di ricerca deve essere stata costruita in precedenza usando JetMakeKey.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334099(v=exchg.10).md">TrySetIndexRange</a></td>
<td>Limita temporaneamente il set di voci di indice che il cursore può spostare usando JetMove a quelle che iniziano dalla voce di indice corrente e terminano in corrispondenza della voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca in tale cursore e ai criteri associati specificati. Una chiave di ricerca deve essere stata costruita in precedenza usando JetMakeKey. Restituisce true se l'intervallo dell'indice è non vuoto; in caso contrario, false.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
