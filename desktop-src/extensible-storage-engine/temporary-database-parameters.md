---
description: 'Altre informazioni su: parametri di database temporanei'
title: Parametri di database temporanei
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: c137472d03f1088da061c20b52050ae1a1f6629e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233352"
---
# <a name="temporary-database-parameters"></a>Parametri di database temporanei


_**Si applica a:** Windows | Windows Server_

## <a name="temporary-database-parameters"></a>Parametri di database temporanei

In questo argomento sono contenuti i parametri utilizzati per il database temporaneo.

*JET_paramEnableTempTableVersioning*  
46  

Questo parametro controlla l'utilizzo delle transazioni nelle tabelle temporanee. Quando questo parametro è false, le tabelle temporanee saranno più veloci, ma non sarà possibile eseguire il rollback degli aggiornamenti effettuati in una transazione.

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
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramPageTempDBMin*  
19  

Questo parametro controlla la dimensione iniziale del database temporaneo. Le dimensioni sono le pagine del database. Una dimensione pari a zero indica che devono essere utilizzate le dimensioni predefinite di un database normale.

È spesso consigliabile che le piccole applicazioni configurino il database temporaneo in modo che sia il più piccolo possibile. L'impostazione di questo parametro su 14 consentirà di ottenere il database temporaneo più piccolo possibile. Si noti che è possibile eliminare completamente il database temporaneo impostando **JET_paramMaxTemporaryTables** su zero.

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
<td><p>Integer</p></td>
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
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramTempPath*  
1  

Questo parametro indica il percorso file system relativo o assoluto della cartella o del file che conterrà il database temporaneo per l'istanza di. Se il percorso è una cartella che conterrà il database temporaneo, deve terminare con un carattere barra rovesciata. Il database temporaneo viene utilizzato per contenere dati volatili generati durante il processo di gestione delle chiamate alle informazioni API ESE, creazione di indici o archiviazione del contenuto di una tabella temporanea.

**Nota**  Se viene specificato un percorso relativo, sarà relativo alla directory di lavoro corrente del processo che ospita l'applicazione che utilizza il motore di database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>&quot;tmp. edb&quot;</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Path (stringa)</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>da 0 a 247 caratteri</p></td>
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
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
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


### <a name="see-also"></a>Vedere anche

[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
