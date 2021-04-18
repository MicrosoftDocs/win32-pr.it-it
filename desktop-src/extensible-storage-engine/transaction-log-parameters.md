---
description: 'Altre informazioni su: parametri del log delle transazioni'
title: Parametri del log delle transazioni
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: 2d72cafc990d8526cadf7c5f6d149796ff846181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315610"
---
# <a name="transaction-log-parameters"></a>Parametri del log delle transazioni


_**Si applica a:** Windows | Windows Server_

**In questo articolo**  
Parametri del log delle transazioni  
Requisiti  
Vedere anche  

## <a name="transaction-log-parameters"></a>Parametri del log delle transazioni

Questo argomento contiene i parametri usati per i log delle transazioni.

*JET_paramBaseName*  
3  

Questo parametro imposta il prefisso di tre lettere usato per molti dei file usati dal motore di database. Il file del checkpoint, ad esempio, è denominato EDB. CHK per impostazione predefinita, perché EDB è il nome di base predefinito. Il nome di base può essere utilizzato per distinguere facilmente tra i set di file che appartengono a istanze diverse o a applicazioni diverse.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>&quot;edb&quot;</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>string</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>3 caratteri</p></td>
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


*JET_paramCircularLog*  
17  

Questo parametro consente di configurare il modo in cui i file di log delle transazioni vengono gestiti dal motore di database.

Quando la registrazione circolare è disattivata, tutti i file di log delle transazioni generati vengono conservati su disco fino a quando non sono più necessari perché è stato eseguito un backup completo del database. In questa modalità è possibile eseguire il ripristino da un backup precedente e riprodurlo attraverso tutti i file di log delle transazioni conservati, in modo che nessun dato venga perso a causa dell'emergenza che ha forzato il ripristino. Sono necessari backup completi regolari per impedire che il disco si riempia con i file di log delle transazioni.

Quando la registrazione circolare è attiva, solo i file di log delle transazioni più piccoli rispetto al checkpoint corrente vengono conservati su disco. Il vantaggio di questa modalità è che non è necessario che i backup ritirino i vecchi file di log delle transazioni. Il compromesso è che il ripristino di una perdita di dati pari a zero non è più possibile.

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
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>No</p></td>
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


*JET_paramCommitDefault*  
16  

Questo parametro controlla l'azione predefinita eseguita quando viene eseguito il commit della transazione più esterna in una sessione. Qualsiasi opzione valida che può essere passata a [JetCommitTransaction](./jetcommittransaction-function.md) può essere impostata anche come predefinita per tutte le sessioni in un'istanza e/o per una sessione specifica. Per ulteriori informazioni su queste opzioni, vedere [JetCommitTransaction](./jetcommittransaction-function.md) .

Questo parametro ha un effetto sull'affidabilità e sulle prestazioni delle transazioni. Per ulteriori informazioni, vedere [JetCommitTransaction](./jetcommittransaction-function.md) .

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
<td><p>JET_GRBIT (Integer)</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>Opzione valida per JetCommitTransaction</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Istanza o sessione</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sì</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramDeleteOldLogs*  
48  

Se questo parametro è true e i file di log delle transazioni a cui fa riferimento il percorso del file di log (**JET_paramLogFilePath**) sono di una versione obsoleta, i file di log delle transazioni verranno automaticamente eliminati.

**Windows 2000:**  È necessario prestare attenzione con l'utilizzo di questo parametro quando si aggiorna un database da Windows NT a Windows 2000. Se il database non è in uno stato coerente e i file di log obsoleti vengono eliminati, il contenuto del database andrà perso.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p><strong>Windows 2000:</strong>  False</p>
<p><strong>Windows XP:</strong>  True</p></td>
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
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>Sì</p></td>
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


*JET_paramIgnoreLogVersion*  
47  

Se questo parametro è true, il motore di database non convaliderà il numero di versione del file di log delle transazioni durante [JetInit](./jetinit-function.md).

**Windows XP:**  A partire da Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.

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


*JET_paramLegacyFileNames*  
136  

Questo parametro fornisce la compatibilità con le versioni precedenti con le convenzioni di denominazione dei file delle versioni precedenti del motore di database.

Attualmente sono supportate le opzioni seguenti:

JET_bitESE98FileNames

Quando questa opzione è presente, il motore di database utilizzerà le convenzioni di denominazione seguenti per i file:

  - I file di log delle transazioni utilizzeranno. LOG per l'estensione di file

  - I file del checkpoint utilizzeranno. CHK per la relativa estensione di file

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>JET_GRBIT (Integer)</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>0, JET_bitESE98FileNames</p></td>
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
<td><p>Windows Vista e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramLogBuffers*  
12  

Questo parametro consente di configurare la quantità di memoria utilizzata per memorizzare nella cache i record del log prima che vengano scritti nel file di log delle transazioni. L'unità per questo parametro è la dimensione settoriale del volume che include i file di log delle transazioni. La dimensione del settore è quasi sempre di 512 byte, quindi è sicuro presupporre che le dimensioni dell'unità.

Questo parametro ha un effetto sulle prestazioni. Quando il motore di database è sottoposto a un carico di aggiornamento intenso, questo buffer può essere pieno molto rapidamente. Una dimensione della cache maggiore per il file di log delle transazioni è essenziale per le prestazioni di aggiornamento ottimali in una condizione di carico elevato. Il valore predefinito è troppo piccolo per questo caso.

**Windows XP e windows 2000:**  In Windows XP e nelle versioni precedenti non è consigliabile impostare questo parametro su un numero di buffer maggiore (in byte) della metà delle dimensioni di un file di log delle transazioni.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  80</p>
<p><strong>Windows Vista:</strong>  126</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  80 – 2147483647</p>
<p><strong>Windows Vista:</strong>  1 – 2147483647</p></td>
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


*JET_paramLogCheckpointPeriod*  
14  

Questo parametro configura il motore di database per l'esecuzione di un checkpoint quando è stato generato il numero specificato di settori dei file di log.

**Windows XP:**  A partire da Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>1024</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramLogFileCreateAsynch*  
69  

Quando questo parametro è impostato su true, il motore di database creerà il file di log delle transazioni successivo mentre viene utilizzato il file di log delle transazioni corrente. Lo scopo è ridurre al minimo il tempo impiegato per passare da un file di log delle transazioni a quello successivo in un carico di aggiornamento intenso.

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
<td><p>Windows XP e versioni successive</p></td>
</tr>
</tbody>
</table>


*JET_paramLogFilePath*  
2 

Questo parametro indica il percorso file system relativo o assoluto della cartella che conterrà i log delle transazioni per l'istanza. Il percorso deve terminare con un carattere barra rovesciata, che indica che il percorso di destinazione è una cartella. I file di log delle transazioni contengono le informazioni necessarie per portare i file di database in uno stato coerente dopo un arresto anomalo. In genere sono denominate EDB \* . LOG. Il contenuto dei file di log delle transazioni è altrettanto importante (in caso contrario) rispetto ai file di database stessi. Per proteggerli, è necessario effettuare tutte le operazioni necessarie.

Saranno disponibili anche altri file di log riservati denominati RES1. LOG e RES2. LOG archiviato insieme ai file di log ordinari. Il contenuto di questi file non è importante perché il loro unico scopo è quello di riservare spazio su disco per consentire al motore di arrestarsi normalmente in uno scenario con un disco insufficiente. Si tratta anche di un file di log temporaneo in genere denominato EDBTMP. ACCEDERE alla stessa cartella. Il contenuto di questo file non è importante. Questo file è un nuovo file di log preparato per l'utilizzo.

Le proprietà del volume host dei file di log delle transazioni e della relativa posizione rispetto agli altri file utilizzati dal motore di database possono avere un impatto significativo sulle prestazioni.

**Nota**  Se viene specificato un percorso relativo, sarà relativo alla directory di lavoro corrente del processo che ospita l'applicazione che utilizza il motore di database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>&quot;.\& quot</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Percorso cartella (stringa)</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>da 0 a 246 caratteri</p></td>
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
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Sì</p></td>
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


*JET_paramLogFileSize*  
11  

Questo parametro consente di configurare le dimensioni dei file di log delle transazioni. Ogni file di log delle transazioni è a dimensione fissa. La dimensione è uguale all'impostazione del parametro di sistema in unità di 1024 byte.

Questo parametro ha un effetto sull'affidabilità. Se l'impostazione è troppo piccola, il numero massimo di file di log (1048575) verrà raggiunto molto più velocemente. Quando si verifica questa situazione, è necessario che l'istanza venga arrestata in modo corretto, che i file di log esistenti vengano eliminati e che sia necessario riavviare l'istanza. Questa azione non solo riduce la disponibilità dell'applicazione, ma invalida anche eventuali backup precedenti del database dell'applicazione.

Questo parametro ha un effetto sulle prestazioni. Se l'impostazione è molto grande, [JetInit](./jetinit-function.md) sarà lento perché il motore di database deve leggere il file di log più recente (come minimo) al momento dell'inizializzazione. Se l'impostazione è molto grande, sarà necessario più tempo per passare da un file di log all'altro. Se l'impostazione è molto piccola, sarà necessario creare più file di log per un determinato numero di aggiornamenti che aggiungono ulteriore sovraccarico.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>5120</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  128 – 32768</p>
<p><strong>Windows Vista:</strong>  64-32768</p></td>
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


*JET_paramLogWaitingUserMax*  
15  

Questo parametro tenta di ottimizzare lo svuotamento del buffer del log causato da un commit durevole attendendo che un numero specificato di sessioni attenda un commit durevole prima di forzare l'esecuzione di uno scaricamento nella speranza che un'altra transazione possa condividere lo scaricamento.

**Windows XP:**  A partire da Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>3</p></td>
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
<td><p>No</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramRecovery*  
34  

Questo parametro è l'opzione master che controlla il ripristino di arresto anomalo del sistema per un'istanza di. Se questo parametro è impostato su "on", verrà usato il ripristino dello stile Ariete per portare tutti i database nell'istanza in uno stato coerente in caso di arresto anomalo di un processo o di un computer. Se questo parametro è impostato su "off", tutti i database nell'istanza verranno gestiti senza il vantaggio del ripristino dell'arresto anomalo del sistema. Ciò significa che se l'istanza non viene arrestata in modo corretto utilizzando [JetTerm](./jetterm-function.md) prima dell'uscita del processo o dell'arresto del computer, il contenuto di tutti i database in tale istanza sarà danneggiato.

La disabilitazione del ripristino è utile in casi speciali in cui è noto che il contenuto di un database non è utile in caso di arresto anomalo del sistema. Il ripristino deve essere abilitato per tutti gli altri casi.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>&quot;On&quot;</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>string</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>da 0 a 259 caratteri</p></td>
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


*JET_paramSystemPath*  
0  

Questo parametro indica il percorso file system relativo o assoluto della cartella che conterrà il file del checkpoint per l'istanza. Il percorso deve terminare con un carattere barra rovesciata, che indica che il percorso di destinazione è una cartella. Il file del checkpoint è un file semplice mantenuto per ogni istanza che ricorda il file di log delle transazioni meno recente che deve essere riprodotto per portare tutti i database di tale istanza in uno stato coerente dopo un arresto anomalo. Il file del checkpoint è in genere denominato EDB. CHK.

**Nota**  Se viene specificato un percorso relativo, sarà relativo alla directory di lavoro corrente del processo che ospita l'applicazione che utilizza il motore di database.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>&quot;.\& quot</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Percorso cartella (stringa)</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>da 0 a 246 caratteri</p></td>
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


*JET_paramWaitLogFlush*  
13 

Questo parametro tenta di ottimizzare lo svuotamento del buffer del log causato da un commit durevole attendendo un periodo di tempo specificato prima di forzare l'esecuzione di uno scaricamento nella speranza che un'altra transazione condivida lo scaricamento.

**Windows XP:**  A partire da Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.

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
<td><p>Istanza o sessione</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>No</p></td>
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
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Tutti</p></td>
</tr>
</tbody>
</table>


*JET_paramLegacyFileNames*  
136  

Questo parametro viene usato per specificare le funzionalità di compatibilità per la denominazione dei file da gestire con Windows Server 2003 e lo schema di denominazione dei file precedenti. Per ulteriori informazioni sui diversi file e i relativi nomi, vedere [file del motore di archiviazione estensibile](./extensible-storage-engine-files.md).

Il JET_bitESE98FileNames garantisce l'estensione di file utilizzata nei file di log delle transazioni e il file del checkpoint corrisponde a quello utilizzato in Windows Server 2003. Nota: se si esegue l'aggiornamento da Windows Server 2003, non è ancora necessario specificare questo bit perché il motore aggiornerà automaticamente le estensioni di file se JET_paramCircularLog è impostato su **true** o se JET_paramCircularLog è **false**, mantenere l'estensione di log precedente.

**Nota**  Per impostare un bit, il valore deve prima essere recuperato, quindi "or" nel bit di compatibilità desiderato.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>JET_GRBIT (Integer)</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>JET_bitESE98FileNames</p></td>
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
<td><p>A partire da Windows Server 2008 e Windows Vista</p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a>Requisiti

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


## <a name="see-also"></a>Vedere anche

[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetTerm](./jetterm-function.md)
