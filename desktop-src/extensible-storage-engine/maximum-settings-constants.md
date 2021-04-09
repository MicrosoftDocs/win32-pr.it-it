---
description: 'Altre informazioni su: costanti impostazioni massime'
title: Costanti di impostazioni massime
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879534"
---
# <a name="maximum-settings-constants"></a>Costanti di impostazioni massime


_**Si applica a:** Windows | Windows Server_

## <a name="maximum-settings-constants"></a>Costanti di impostazioni massime

Queste costanti forniscono le impostazioni massime consentite per gli elementi di un database ESE.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Costante/valore</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_BASE_NAME_LENGTH<br />
3</p></td>
<td><p>Imposta la lunghezza per il prefisso utilizzato per denominare i file utilizzati dal motore di database. Questa lunghezza è applicabile al nome impostato per il parametro di sistema <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_MAX_COMPUTERNAME_LENGTH<br />
15</p></td>
<td><p>Imposta la lunghezza massima per <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbBookmarkMost<br />
256</p></td>
<td><p>Dimensioni massime predefinite di un segnalibro. Questo valore è valido quando la dimensione della chiave viene lasciata sul valore predefinito.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbBookmarkMostMost<br />
2000</p></td>
<td><p>Dimensione massima di un segnalibro quando ESENT è configurato in modo da avere le chiavi maggiori possibili.</p>
<p><strong>Windows 7:</strong> JET_cbBookmarkMostMost è stato introdotto in Windows 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbNameMost<br />
64</p></td>
<td><p>Lunghezza massima di un oggetto, una colonna, un indice o un nome di proprietà.</p>
<p><strong>Nota</strong>  Se Unicode, il valore è 128.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbFullNameMost<br />
255</p></td>
<td><p>Lunghezza massima di un &quot; costrutto Name.Name.Name.... &quot;</p>
<p><strong>Nota</strong>  Se Unicode, il valore è 510.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbColumnLVPageOverhead<br />
82</p></td>
<td><p>Questo numero può essere utilizzato per calcolare la quantità massima di un BLOB che può essere archiviato dal motore di database in una singola pagina di database. La formula è max size = JET_paramDatabasePageSize-JET_cbColumnLVPageOverhead.</p>
<p>Questo valore è ora obsoleto. È necessario recuperare le dimensioni del blocco con valore Long con il parametro JET_paramLVChunkSizeMost.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbColumnMost<br />
255</p></td>
<td><p>Dimensione massima dei dati della colonna non di valori Long.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbLVDefaultValueMost<br />
255</p></td>
<td><p>Dimensione massima di un valore predefinito della colonna con valore Long (LongBinary o LongText).</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost<br />
255</p></td>
<td><p>Dimensioni massime predefinite di una chiave di ordinamento o di indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMost<br />
2000</p></td>
<td><p>Dimensioni massime configurabili di una chiave di ordinamento o di indice per qualsiasi dimensione di pagina. (Vedere JET_INDEXCREATE2. cbKeyMost)</p>
<p><strong>Windows 7:</strong> JET_cbKeyMostMost è stato introdotto nel sistema operativo Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost2KBytePage<br />
500</p></td>
<td><p>Dimensioni massime consentite configurabili per una chiave di indice in un database che utilizza pagine a 2048 byte. Per ulteriori informazioni, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage è stato introdotto nel sistema operativo Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMost4KBytePage<br />
1000</p></td>
<td><p>Dimensioni massime consentite configurabili per una chiave di indice in un database che utilizza pagine a 4096 byte. Per ulteriori informazioni, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage è stato introdotto in Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost8KBytePage<br />
2000</p></td>
<td><p>Dimensioni massime consentite configurabili per una chiave di indice in un database che utilizza pagine a 8192 byte. Per ulteriori informazioni, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:  </strong> JET_cbKeyMost8KBytePage è stato introdotto in Windows Vista</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMin<br />
255</p></td>
<td><p>Dimensioni massime consentite minime per una chiave di indice. Per ulteriori informazioni, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista:  </strong> JET_cbKeyMostMin è stato introdotto in Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbLimitKeyMost<br />
256</p></td>
<td><p>Dimensione massima della chiave quando la chiave viene formata usando un limite <em>grbit</em>, ad esempio JET_bitStrLimit, che viene usato nella funzione <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbPrimaryKeyMost<br />
255</p></td>
<td><p>Dimensione massima dell'indice primario. Questa operazione è ora obsoleta.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbSecondaryKeyMost<br />
255</p></td>
<td><p>Dimensione massima dell'indice secondario. Questa operazione è ora obsoleta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolKeyMost<br />
12</p></td>
<td><p>Numero massimo di componenti in una chiave di ordinamento o di indice.</p>
<p><strong>Windows Vista:  </strong> In Windows Vista e nelle versioni successive di Windows il valore è 16.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolMost<br />
0x0000fee0</p></td>
<td><p>Numero massimo di colonne consentite in una tabella.</p>
<p><strong>Windows XP:  </strong> Il valore 0x0000fee0 viene utilizzato in Windows XP e versioni successive e successive di Windows</p>
<p><strong>Windows 2000:  </strong> Il valore 0x00007ffe viene usato in Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolFixedMost<br />
0x0000007F</p></td>
<td><p>Numero massimo di colonne fisse consentite in una tabella, attualmente 127.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolVarMost<br />
0x00000080</p></td>
<td><p>Numero massimo di colonne a lunghezza variabile che possono essere contenute in una tabella, attualmente 128.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolTaggedMost<br />
(JET_ccolMost-0x000000FF)</p></td>
<td><p>Numero massimo di colonne con tag che possono essere contenute in una tabella, attualmente 64993.</p></td>
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
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>

