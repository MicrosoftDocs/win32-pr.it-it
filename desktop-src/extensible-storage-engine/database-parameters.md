---
description: 'Altre informazioni su: Parametri di database'
title: Parametri del database
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13de02c7d322933f64361cfdabcb8f95ead837ad915ad69c3961a8b8874d5b9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117561"
---
# <a name="database-parameters"></a>Parametri del database


_**Si applica a:** Windows | Windows Server_

## <a name="database-parameters"></a>Parametri del database

Questo argomento contiene i parametri usati per il database.

*JET_paramCheckFormatWhenOpenFail*  
44  

Questo parametro, se impostato, causerà la restituzione di un errore speciale da parte di [JetInit](./jetinit-function.md) quando viene aperto un database o un log delle transazioni da una versione precedente del motore di database. Questi errori sono:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Errore</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errDatabase200Format</p></td>
<td><p>I file di database e/o di log delle transazioni sono stati creati con il motore di database in Windows NT 3.51.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format</p></td>
<td><p>I file di database e/o di log delle transazioni sono stati creati con il motore di database in una versione di test precedente a Windows NT Server 4.0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format</p></td>
<td><p>I file di database e/o di log delle transazioni sono stati creati con il motore di database in Windows NT Server 4.0.</p></td>
</tr>
</tbody>
</table>


**Windows Vista:**  Per Windows Vista e versioni successive, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>Vero</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramDatabasePageSize*  
64  

Questo parametro configura le dimensioni della pagina per il database. Le dimensioni della pagina sono la più piccola unità di allocazione di spazio possibile per un file di database. Anche le dimensioni della pagina del database sono molto importanti perché imposta il limite superiore per le dimensioni di un singolo record nel database.

**Nota** Al momento è supportata una sola dimensione di pagina del database per ogni processo. Ciò significa che se si è in un singolo processo che contiene applicazioni diverse che usano il motore di database, devono tutti concordare le dimensioni della pagina del database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>4096</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>2048, 4096, 8192</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramDbExtensionSize*  
18  

Questo parametro controlla la quantità di spazio che viene aggiunta a un file di database ogni volta che deve aumentare per contenere più dati. Le dimensioni sono in pagine di database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>256</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p>
<p><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableIndexChecking*  
45  

Quando questo parametro è true, ogni database viene controllato al momento [di JetAttachDatabase](./jetattachdatabase-function.md) per gli indici su colonne chiave Unicode compilate usando una versione precedente della libreria NLS nel sistema operativo. Questa operazione deve essere eseguita perché il motore di database rende persistenti le chiavi di ordinamento generate da [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) e il valore di queste chiavi di ordinamento cambia da rilascio a rilascio.

Se viene rilevato che un indice primario si trova in questo stato, [JetAttachDatabase](./jetattachdatabase-function.md) avrà sempre esito negativo JET_errPrimaryIndexCorrupted.

Se viene rilevato che uno degli indici secondari è in questo stato, esistono due possibili risultati. Se JET_bitDbDeleteCorruptIndexes passato a [JetAttachDatabase,](./jetattachdatabase-function.md) questi indici verranno eliminati e JET_wrnCorruptIndexDeleted restituiti da [JetAttachDatabase](./jetattachdatabase-function.md). Questi indici dovranno essere ricreati dall'applicazione. Se JET_bitDbDeleteCorruptIndexes non è stato passato [a JetAttachDatabase,](./jetattachdatabase-function.md) la chiamata avrà esito negativo con JET_errSecondaryIndexCorrupted.

**Nota** È consigliabile impostare questo parametro su True dall'applicazione.

**Nota** È consigliabile che le applicazioni evitino l'uso di colonne chiave Unicode negli indici di chiave primaria (cluster).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p>
<p><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableIndexCleanup*  
54  

Quando questo parametro è impostato su true, il motore di database può pulire automaticamente gli indici sulle colonne chiave Unicode all'ora [JetInit](./jetinit-function.md) in base alle esigenze per evitare modifiche al formato del database causate dalle modifiche apportate alla libreria NLS in Windows. Tali modifiche vengono apportate regolarmente alla libreria NLS per aggiungere il supporto per nuove lingue, aggiungere caratteri mancanti a una lingua, aggiungere un ordine delle regole di confronto a una lingua o correggere i bug nell'ordine delle regole di confronto di una lingua. Queste modifiche influiscono sulle chiavi di ordinamento prodotte da [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) che vengono rese persistenti dal motore di database come componenti delle chiavi di indice.

È importante tenere conto che è possibile che le modifiche all'indice siano così grandi che non è possibile eseguire una pulizia incrementale. In questo caso, l'indice verrà gestito come indicato **da** JET_paramEnableIndexChecking .

**Nota** È consigliabile impostare questo parametro e **JET_paramEnableIndexChecking** su **True** dall'applicazione.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>Vero</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p>
<p><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows Server 2003 e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramOneDatabasePerSession*  
102  

Quando questo parametro è true, solo un database può essere aperto con [JetOpenDatabase](./jetopendatabase-function.md) da una determinata sessione contemporaneamente. Il database temporaneo è escluso da questa restrizione.

**Windows XP e Windows Server 2003:**  Questo parametro è scritto solo in Windows XP e Windows Server 2003.

**Windows Vista:**  Questo parametro si comporta normalmente come Windows Vista.

**Nota**  Questo parametro è di sola scrittura.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>No</p>
<p><strong>Windows Vista:</strong>  Per Windows Vista e versioni successive: Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows XP e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableOnlineDefrag*  
35  

Questo parametro controlla il comportamento della deframmentazione online quando viene avviato tramite [JetDefragment](./jetdefragment-function.md). Per altre [informazioni, vedere JetDefragment.](./jetdefragment-function.md)

Windows 2000: Windows 2000, questo parametro era un booleano semplice che cancellerebbe la deframmentazione online quando viene avviata da [JetDefragment](./jetdefragment-function.md). Se impostato su **TRUE,** la deframmentazione online verrà eseguita sui record di ogni tabella nel database.

**Windows XP:**  In Windows XP e versioni successive, questo parametro può essere impostato su una o più delle opzioni seguenti:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Opzione</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_OnlineDefragDisable</p></td>
<td><p>Non eseguire la deframmentazione online. Si tratta dell'equivalente binario dell'Windows 2000 di False per questo parametro.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAllOBSOLETE</p></td>
<td><p>Eseguire la deframmentazione online completa. Si tratta dell'equivalente binario dell'Windows 2000 di True per questo parametro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragDatabases</p></td>
<td><p>Eseguire la deframmentazione online dei record di ogni tabella nel database.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragSpaceTrees</p></td>
<td><p>Eseguire la deframmentazione online degli alberi dello spazio di ogni tabella nel database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragStreamingFiles</p></td>
<td><p>Questo parametro viene usato per supportare l'infrastruttura Exchange Microsoft e non deve essere usato nell'applicazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAll</p></td>
<td><p>Eseguire la deframmentazione online completa. Si tratta dell'equivalente concettuale dell'Windows 2000 di True per questo parametro.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p><strong>Windows 2000:</strong>  Vero</p>
<p><strong>Windows XP: per Windows XP e versioni successive:</strong> JET_OnlineDefragAll</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p><strong>Windows 2000:</strong>  Boolean</p>
<p><strong>Windows XP e versioni successive:</strong>  JET_GRBIT (integer)</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000:</strong>  False, True</p>
<p><strong>Windows XP e versioni successive:</strong> 0 - JET_OnlineDefragAll</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramPageFragment*  
20  

Questo parametro è la soglia utilizzata dal motore di database per controllare la frammentazione dello spazio disponibile. Le dimensioni sono in pagine di database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>8</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramRecordUpgradeDirtyLevel*  
78

Questo parametro controlla l'aggressività con cui il gestore della cache delle pagine del database scriverà una pagina di database sottoposta a una conversione del formato sul posto. Queste conversioni di formato vengono eseguite in tempo reale quando le pagine vengono caricate da un database creato con il motore di database di Windows 2000 ma usato da Windows XP o da una versione successiva del motore di database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0-3</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows XP e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramWaypointLatency*  
153  

La latenza (nei log) dietro il log di suggerimento/commit più elevato per rinviare gli scaricamenti delle pagine del database. L'abilitazione di questa latenza può consentire il ripristino del database in caso di perdita irreversica del file di log più recente. Vedere JET_bitReplayIgnoreLostLogs.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0-1023</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTrees*  
160  

Attivare/disattivare la deframmentazione automatica sequenziale dell'albero B.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0-1</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*  
161  

Determina la frequenza di controllo della densità dell'albero B.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>Numero intero massimo 0</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramIOThrottlingTimeQuanta*  
162  

Tempo massimo, in millisecondi, che il meccanismo di limitazione di I/O concede a un'attività di essere eseguita perché sia considerata "completata".

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>125</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Intero</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0-10000</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Globale</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


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

[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetInit](./jetinit-function.md)
