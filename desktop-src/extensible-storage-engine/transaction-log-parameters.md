---
description: 'Altre informazioni: Parametri del log delle transazioni'
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
ms.openlocfilehash: 1d8f3ed19d01eece0b22e22b4a2a16d8d985751a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982179"
---
# <a name="transaction-log-parameters"></a>Parametri del log delle transazioni


_**Si applica a:** Windows | Windows Server_

**In questo articolo**  
Parametri del log delle transazioni  
Requisiti  
Vedere anche  

## <a name="transaction-log-parameters"></a>Parametri del log delle transazioni

In questo argomento sono contenuti i parametri utilizzati per i log delle transazioni.

*JET_paramBaseName*  
3  

Questo parametro imposta il prefisso di tre lettere usato per molti dei file usati dal motore di database. Ad esempio, il file del checkpoint è denominato EDB. ChK per impostazione predefinita perché EDB è il nome di base predefinito. Il nome di base può essere usato per distinguere facilmente tra set di file appartenenti a istanze diverse o ad applicazioni diverse.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>"edb"</p> | 
| <p>Digitare:</p> | <p>Stringa</p> | 
| <p>Intervallo valido:</p> | <p>3 caratteri</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramCircularLog*  
17  

Questo parametro consente di configurare la modalità di gestione dei file di log delle transazioni da parte del motore di database.

Quando la registrazione circolare è disattivata, tutti i file di log delle transazioni generati vengono mantenuti su disco fino a quando non sono più necessari perché è stato eseguito un backup completo del database. In questa modalità è possibile eseguire il ripristino da un backup precedente e riprodurre in avanti tutti i file di log delle transazioni conservati in modo che non si persa alcuna perdita di dati a causa dell'emergenza che ha forzato il ripristino. Sono necessari backup completi regolari per evitare che il disco si riempia di file di log delle transazioni.

Quando la registrazione circolare è attivata, solo i file di log delle transazioni più piccoli rispetto al checkpoint corrente vengono mantenuti su disco. Il vantaggio di questa modalità è che i backup non sono necessari per ritirare i file di log delle transazioni meno recente. Il compromesso è che un ripristino senza perdita di dati non è più possibile.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Falso</p> | 
| <p>Digitare:</p> | <p>Boolean</p> | 
| <p>Intervallo valido:</p> | <p>False, True</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramCommitDefault*  
16  

Questo parametro controlla l'azione predefinita eseguita quando viene eseguito il commit della transazione più esterna in una sessione. Qualsiasi opzione valida che può essere passata a [JetCommitTransaction](./jetcommittransaction-function.md) può anche essere impostata come predefinita per tutte le sessioni in un'istanza e/o per una sessione specifica. Per altri dettagli su queste opzioni, vedere [JetCommitTransaction.](./jetcommittransaction-function.md)

Questo parametro influisce sull'affidabilità e sulle prestazioni delle transazioni. Per altri [dettagli, vedere JetCommitTransaction.](./jetcommittransaction-function.md)


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>0</p> | 
| <p>Digitare:</p> | <p>JET_GRBIT (integer)</p> | 
| <p>Intervallo valido:</p> | <p>Opzione valida per JetCommitTransaction</p> | 
| <p>Ambito:</p> | <p>Istanza o sessione</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramDeleteOldLogs*  
48  

Quando questo parametro è true e i file di log delle transazioni a cui punta il percorso del file di log (**JET_paramLogFilePath**) sono tutti di una versione obsoleta, tali file di log delle transazioni verranno eliminati automaticamente.

**Windows 2000:**  Quando si aggiorna un database da Windows NT a Windows 2000, è necessario usare questo parametro. Se il database non è in uno stato coerente e i vecchi file di log vengono eliminati, il contenuto del database andrà perso.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p><strong>Windows 2000:</strong>  False</p><p><strong>Windows XP:</strong>  Vero</p> | 
| <p>Digitare:</p> | <p>Boolean</p> | 
| <p>Intervallo valido:</p> | <p>False, True</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramIgnoreLogVersion*  
47  

Se questo parametro è true, il motore di database non convaliderà il numero di versione del file di log delle transazioni durante [JetInit.](./jetinit-function.md)

**Windows XP:**  A Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Falso</p> | 
| <p>Digitare:</p> | <p>Boolean</p> | 
| <p>Intervallo valido:</p> | <p>False, True</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramLegacyFileNames*  
136  

Questo parametro garantisce la compatibilità con le versioni precedenti delle convenzioni di denominazione dei file delle versioni precedenti del motore di database.

Sono attualmente supportate le opzioni seguenti:

JET_bitESE98FileNames

Quando questa opzione è presente, il motore di database userà le convenzioni di denominazione seguenti per i relativi file:

  - I file di log delle transazioni useranno . LOG per l'estensione del file

  - I file del checkpoint useranno . CHK per l'estensione di file


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>JET_bitESE98FileNames</p> | 
| <p>Digitare:</p> | <p>JET_GRBIT (integer)</p> | 
| <p>Intervallo valido:</p> | <p>0, JET_bitESE98FileNames</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Windows Vista e versioni successive</p> | 



*JET_paramLogBuffers*  
12  

Questo parametro configurerà la quantità di memoria utilizzata per memorizzare nella cache i record del log prima che siano scritti nel file di log delle transazioni. L'unità per questo parametro è la dimensione del settore del volume che contiene i file di log delle transazioni. Le dimensioni del settore sono quasi sempre di 512 byte, pertanto è sicuro presupporre che le dimensioni per l'unità.

Questo parametro influisce sulle prestazioni. Quando il motore di database è in condizioni di carico di aggiornamento elevato, questo buffer può diventare pieno molto rapidamente. Una dimensione della cache maggiore per il file di log delle transazioni è fondamentale per prestazioni di aggiornamento ottimali in condizioni di carico così elevate. Il valore predefinito è noto per essere troppo piccolo per questo caso.

**Windows XP e Windows 2000:**  In Windows XP e versioni precedenti, non è consigliabile impostare questo parametro su un numero di buffer maggiore (in byte) della metà delle dimensioni di un file di log delle transazioni.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 80</p><p><strong>Windows Vista:</strong> 126</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 80 – 2147483647</p><p><strong>Windows Vista:</strong> 1 - 2147483647</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramLogCheckpointPeriod*  
14  

Questo parametro configura il motore di database per l'esecuzione di un checkpoint quando è stato generato il numero specificato di settori del file di log.

**Windows XP:**  A Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>1024</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramLogFileCreateAsynch*  
69  

Quando questo parametro è impostato su true, il motore di database creerà il file di log delle transazioni successivo quando viene utilizzato il file di log delle transazioni corrente. Lo scopo è ridurre al minimo il tempo impiegato per il passaggio da un file di log delle transazioni a quello successivo in un carico di aggiornamento elevato.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Vero</p> | 
| <p>Digitare:</p> | <p>Boolean</p> | 
| <p>Intervallo valido:</p> | <p>False, True</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Windows XP e versioni successive</p> | 



*JET_paramLogFilePath*  
2 

Questo parametro indica il percorso relativo o file system assoluto della cartella che conterrà i log delle transazioni per l'istanza. Il percorso deve essere terminato con un carattere barra rovesciata, che indica che il percorso di destinazione è una cartella. I file di log delle transazioni contengono le informazioni necessarie per portare i file di database a uno stato coerente dopo un arresto anomalo. Sono in genere denominati EDB \* . REGISTRO. Il contenuto dei file di log delle transazioni è importante (se non superiore) rispetto ai file di database stessi. È necessario fare tutto il possibile per proteggerli.

Saranno anche disponibili altri file di log di riserva denominati RES1. LOG e RES2. LOG archiviato insieme ai file di log ordinari. Il contenuto di questi file non è importante perché l'unico scopo è riservare spazio su disco per consentire l'arresto del motore normalmente in uno scenario con disco basso. Si tratta anche di un file di log temporaneo denominato in genere EDBTMP. Accedere a questa stessa cartella. Anche il contenuto di questo file non è importante. Questo file è un nuovo file di log preparato per l'uso.

Le proprietà del volume host dei file di log delle transazioni e la relativa posizione rispetto agli altri file usati dal motore di database possono influire notevolmente sulle prestazioni.

**Nota**  Se viene specificato un percorso relativo, sarà relativo alla directory di lavoro corrente del processo che ospita l'applicazione che usa il motore di database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>".\"</p> | 
| <p>Digitare:</p> | <p>Percorso cartella (stringa)</p> | 
| <p>Intervallo valido:</p> | <p>Da 0 a 246 caratteri</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramLogFileSize*  
11  

Questo parametro configurerà le dimensioni dei file di log delle transazioni. Ogni file di log delle transazioni ha dimensioni fisse. La dimensione è uguale all'impostazione di questo parametro di sistema in unità di 1024 byte.

Questo parametro influisce sull'affidabilità. Se l'impostazione è troppo piccola, il numero massimo di file di log (1048575) verrà raggiunto molto più velocemente. In questo caso, è necessario arrestare l'istanza in modo pulito, eliminare i file di log esistenti e riavviare l'istanza. Questa azione non solo ridurrà la disponibilità dell'applicazione, ma invaliderà anche eventuali backup precedenti del database dell'applicazione.

Questo parametro influisce sulle prestazioni. Se l'impostazione è molto grande, [JetInit](./jetinit-function.md) sarà lento perché il motore di database deve leggere almeno il file di log più piccolo durante l'inizializzazione. Se l'impostazione è molto grande, anche il passaggio tra i file di log richiederà più tempo. Se l'impostazione è molto piccola, sarà necessario creare più file di log per un determinato numero di aggiornamenti, con un sovraccarico maggiore.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>5120</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 128 – 32768</p><p><strong>Windows Vista:</strong> 64 – 32768</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramLogWaitingUserMax*  
15  

Questo parametro tenta di ottimizzare lo scaricamento del buffer di log causato da un commit durevole attendendo che un numero specificato di sessioni attenda un commit durevole prima di forzare l'esecuzione di uno scaricamento nella speranza che un'altra transazione convade lo scaricamento.

**Windows XP:**  A Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>3</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sì</p> | 
| <p>Impostare dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramRecovery*  
34  

Questo parametro è l'opzione master che controlla il ripristino dell'arresto anomalo del sistema per un'istanza di . Se questo parametro è impostato su "On", verrà usato il ripristino in stile ARIES per portare tutti i database nell'istanza a uno stato coerente in caso di arresto anomalo di un processo o di un computer. Se questo parametro è impostato su "Off", tutti i database nell'istanza verranno gestiti senza il vantaggio del ripristino dell'arresto anomalo del sistema. Ciò significa che se l'istanza non viene arrestata in modo pulito usando [JetTerm](./jetterm-function.md) prima dell'uscita del processo o dell'arresto del computer, il contenuto di tutti i database in tale istanza verrà danneggiato.

La disabilitazione del ripristino è utile in casi speciali in cui è noto che il contenuto di un database non è utile in caso di arresto anomalo del sistema. Il ripristino deve essere abilitato per tutti gli altri casi.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>"On"</p> | 
| <p>Digitare:</p> | <p>Stringa</p> | 
| <p>Intervallo valido:</p> | <p>Da 0 a 259 caratteri</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Sì</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>Sì</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramSystemPath*  
0  

Questo parametro indica il percorso relativo o file system assoluto della cartella che conterrà il file del checkpoint per l'istanza di . Il percorso deve terminare con una barra rovesciata, che indica che il percorso di destinazione è una cartella. Il file del checkpoint è un file semplice gestito per ogni istanza che memorizza il file di log delle transazioni meno recente che deve essere riprodotto per portare tutti i database in tale istanza a uno stato coerente dopo un arresto anomalo. Il file del checkpoint è in genere denominato EDB. CHK.

**Nota**  Se viene specificato un percorso relativo, sarà relativo alla directory di lavoro corrente del processo che ospita l'applicazione che usa il motore di database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>".\"</p> | 
| <p>Digitare:</p> | <p>Percorso cartella (stringa)</p> | 
| <p>Intervallo valido:</p> | <p>Da 0 a 246 caratteri</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramWaitLogFlush*  
13 

Questo parametro tenta di ottimizzare lo scaricamento del buffer di log causato da un commit durevole, attendendo un periodo di tempo specificato prima di forzare l'esecuzione di uno scaricamento nella attesa che un'altra transazione con questa possa condividere lo scaricamento.

**Windows XP:**  A Windows XP, questo parametro è obsoleto e non influisce sul funzionamento del motore di database.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>0</p> | 
| <p>Digitare:</p> | <p>Intero</p> | 
| <p>Intervallo valido:</p> | <p>0 – 2147483647</p> | 
| <p>Ambito:</p> | <p>Istanza o sessione</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Sì</p> | 
| <p>Influisce sul layout fisico:</p> | <p>No</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Sì</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>Tutti</p> | 



*JET_paramLegacyFileNames*  
136  

Questo parametro viene utilizzato per specificare le funzionalità di compatibilità di denominazione dei file da mantenere con lo schema di denominazione dei file Windows Server 2003 e con lo schema di denominazione dei file precedente. Per altre informazioni sui diversi file e sulla relativa denominazione, [vedere Extensible Archiviazione Engine Files](./extensible-storage-engine-files.md).

Il JET_bitESE98FileNames garantisce che l'estensione di file usata nei file di log delle transazioni e il file del checkpoint siano uguali a quello usato in Windows Server 2003. Si noti che se si esegue l'aggiornamento da Windows Server 2003, questo bit non deve essere ancora specificato, perché il motore aggiorna automaticamente le estensioni di file se JET_paramCircularLog è impostato su **true** o mantiene l'estensione del log precedente se JET_paramCircularLog è **false.**

**Nota**  Per impostare un bit, è necessario innanzitutto recuperare il valore e quindi "or" nel bit di compatibilità desiderato.


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>JET_bitESE98FileNames</p> | 
| <p>Digitare:</p> | <p>JET_GRBIT (integer)</p> | 
| <p>Intervallo valido:</p> | <p>JET_bitESE98FileNames</p> | 
| <p>Ambito:</p> | <p>Istanza</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sì</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>No</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Sì</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>No</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>No</p> | 
| <p>Influisce sulle risorse:</p> | <p>No</p> | 
| <p>Disponibilità:</p> | <p>A partire da Windows Server 2008 e Windows Vista</p> | 



## <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



## <a name="see-also"></a>Vedere anche

[File del motore Archiviazione estendibile](./extensible-storage-engine-files.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetTerm](./jetterm-function.md)
