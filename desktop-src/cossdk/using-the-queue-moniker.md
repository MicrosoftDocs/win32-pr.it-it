---
description: Il moniker della coda viene utilizzato per attivare un componente in coda a livello di codice.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Utilizzo del moniker della coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228964157d08aca868474167ae16590692f16ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304929"
---
# <a name="using-the-queue-moniker"></a>Utilizzo del moniker della coda

Il moniker della coda viene utilizzato per attivare un componente in coda a livello di codice. Il moniker della coda richiede la ricezione dell'ID di classe (CLSID) dell'oggetto da richiamare direttamente dal nuovo moniker. Quando il prefisso è a sinistra, il nuovo moniker passa il CLSID al moniker alla sua sinistra.

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Non è valida.

## <a name="visual-basic"></a>Visual Basic

Il parametro del nome visualizzato GetObject è "queue:/New:", seguito dall'ID del programma o dal GUID del formato stringa, con o senza parentesi graffe, dell'oggetto server di cui creare un'istanza. Gli esempi seguenti illustrano tre attivazioni valide di un componente con il moniker della coda:

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a>C/C++

Il parametro del nome visualizzato [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) è "queue:/New:", seguito dall'ID del programma o dal GUID del formato stringa, con o senza parentesi graffe, dell'oggetto server per cui creare un'istanza. Gli esempi seguenti illustrano tre attivazioni valide di un componente con il moniker della coda:

1.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:QCShip.Ship",
      NULL, IID_IShip, (void**)&pShip);
    ```

2.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}", 
      NULL, IID_IShip, (void**)&pShip);
    ```

3.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE",
      NULL, IID_IShip, (void**)&pShip);
    ```

## <a name="remarks"></a>Commenti

Il moniker della coda accetta parametri facoltativi che modificano le proprietà del messaggio inviato a Accodamento messaggi. Ad esempio, per fare in modo che il messaggio di Accodamento messaggi venga inviato con una priorità 6, il componente in coda verrebbe attivato come segue:

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

Nella tabella seguente sono elencati i parametri del moniker della coda che interessano la coda di destinazione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parametro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>NomeComputer</em><br/></td>
<td>Specifica la parte relativa al nome del computer di un nome di percorso della coda di Accodamento messaggi. Il nome del percorso della coda di Accodamento messaggi è formattato come <em>nomecomputer</em> \ <em>QueueName</em>. Se non specificato, viene usato il nome computer associato all'applicazione configurata.<br/></td>
</tr>
<tr class="even">
<td><em>QueueName</em><br/></td>
<td>Specifica il nome della coda di Accodamento messaggi. Il nome del percorso della coda di Accodamento messaggi è formattato come <em>nomecomputer</em> \ <em>QueueName</em>. Se non specificato, viene usato il nome della coda associato all'applicazione configurata.<br/> Per ottenere una coda non transazionale, è possibile specificare prima il nome della coda, quindi creare un'applicazione COM+ con lo stesso nome.<br/></td>
</tr>
<tr class="odd">
<td><em>PathName</em><br/></td>
<td>Specifica il nome completo del percorso della coda di Accodamento messaggi. Se non specificato, viene utilizzato il nome del percorso della coda di Accodamento messaggi associato all'applicazione configurata. Per eseguire l'override del nome di destinazione, è possibile specificare il percorso nel formato seguente per l'installazione di un gruppo di lavoro di Accodamento messaggi:<br/> Queue:<em>pathname</em> = <em>nomecomputer</em>\Private $ \ AppName/New: MyProject. CMyClass<br/>
<blockquote>
[!Note]<br />
Per entrambi i linguaggi di programmazione C e Microsoft Visual C++ sono necessarie due barre rovesciate per rappresentare una barra rovesciata nei valori letterali stringa, ad esempio la \\ retribuzione di Chicago.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><em>FormatName</em><br/></td>
<td>Quando si contrassegna un'applicazione COM+ come accodata, COM+ crea una coda di Accodamento messaggi il cui nome corrisponde a quello dell'applicazione. Il nome del formato di Accodamento messaggi della coda si trova nel catalogo COM+, associato all'applicazione COM+. Per eseguire l'override del nome di destinazione, il nome del formato può essere specificato nel formato seguente per l'installazione di un gruppo di lavoro di Accodamento messaggi:<br/> Queue:<em>FormatName</em>= Direct = OS:<em>nomecomputer</em>\Private $ \ AppName/New: ProgID<br/> In una configurazione di Active Directory, &quot; private $ &quot; non è specificato come parte del nome della coda. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> I parametri facoltativi del moniker della coda vengono elaborati da sinistra a destra. Specificare ogni parola chiave solo una volta. La specifica del parametro *pathname* sostituisce i parametri *ComputerName* e *QueueName*. Un parametro *FormatName* specifico Elimina la conoscenza precedente di un parametro *ComputerName*, *QueueName* e *pathname* .

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a>Associazione del listener dei componenti in coda a una coda privata specifica

Il listener dei componenti in coda COM+ riceve solo dalle code associate all'applicazione COM+ contrassegnata come accodata. Quando si contrassegna un'applicazione COM+ come accodata, COM+ crea una coda di Accodamento messaggi il cui nome corrisponde a quello dell'applicazione. Il nome del formato di Accodamento messaggi della coda si trova nel catalogo COM+, associato all'applicazione COM+. Quando l'applicazione COM+ viene avviata e contrassegnata come Listen, viene avviato un listener nel processo dell'applicazione COM+ e viene aperta la coda. Nella tabella seguente sono elencati i parametri del moniker della coda che influiscono sul messaggio di Accodamento messaggi.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parametro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>AppSpecific</em><br/></td>
<td>Specifica un Unsigned Integer ad esempio, AppSpecific = 12345.<br/></td>
</tr>
<tr class="even">
<td><em>AuthLevel</em><br/></td>
<td>Specifica il livello di autenticazione del messaggio. Un messaggio autenticato è firmato digitalmente e richiede un certificato per l'utente che invia il messaggio. Valori accettabili:<br/>
<ul>
<li>MQMSG_AUTH_LEVEL_NONE, 0</li>
<li>MQMSG_AUTH_LEVEL_ALWAYS, 1</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Recapito</em><br/></td>
<td>Specifica l'opzione di recapito dei messaggi. Questo valore viene ignorato per le code transazionali. Valori accettabili:<br/>
<ul>
<li>MQMSG_DELIVERY_EXPRESS, 0</li>
<li>MQMSG_DELIVERY_RECOVERABLE, 1</li>
</ul></td>
</tr>
<tr class="even">
<td><em>EncryptAlgorithm</em><br/></td>
<td>Specifica l'algoritmo di crittografia che verrà utilizzato da Accodamento messaggi per crittografare e decrittografare il messaggio. Valori accettabili:<br/>
<ul>
<li>CALG_RC2, CALG_RC4</li>
<li>Qualsiasi valore intero accettabile per l'accodamento dei messaggi per un <em>EncryptAlgorithm</em>.</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>HashAlgorithm</em><br/></td>
<td>Specifica una funzione hash crittografica. Valori accettabili:<br/>
<ul>
<li>CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</li>
<li>Qualsiasi valore intero accettabile per l'accodamento dei messaggi per un oggetto <em>HashAlgorithm</em>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Rivista<br/></td>
<td>Specifica l'opzione del journal dei messaggi di Accodamento messaggi. Valori accettabili:<br/>
<ul>
<li>MQMSG_JOURNAL_NONE, 0</li>
<li>MQMSG_DEADLETTER, 1</li>
<li>MQMSG_JOURNAL, 2</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Etichetta</em><br/></td>
<td>Specifica una stringa di etichetta del messaggio fino a MQ_MAX_MSG_LABEL_LEN caratteri. <br/></td>
</tr>
<tr class="even">
<td><em>MaxTimeToReachQueue</em><br/></td>
<td>Specifica il tempo massimo, in secondi, per il raggiungimento della coda da parte del messaggio. <br/> Valori accettabili:<br/>
<ul>
<li>INFINITE</li>
<li>LONG_LIVED</li>
<li>Numero di secondi</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>MaxTimeToReceive</em><br/></td>
<td>Specifica il tempo massimo, in secondi, per la ricezione del messaggio da parte dell'applicazione di destinazione. Valori accettabili:<br/>
<ul>
<li>INFINITE</li>
<li>LONG_LIVED</li>
<li>Numero di secondi</li>
</ul></td>
</tr>
<tr class="even">
<td><em>Priorità</em><br/></td>
<td>Specifica un livello di priorità del messaggio, all'interno dei valori di Accodamento messaggi consentiti.<br/> Valori accettabili:<br/>
<ul>
<li>MQ_MIN_PRIORITY, 0</li>
<li>MQ_MAX_PRIORITY, 7</li>
<li>MQ_DEFAULT_PRIORITY, 3</li>
<li>Numero compreso tra 0 e 7</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>PrivLevel</em><br/></td>
<td>Specifica un livello di privacy utilizzato per crittografare i messaggi.<br/> Valori accettabili:<br/>
<ul>
<li>MQMSG_PRIV_LEVEL_NONE, NESSUNA, 0</li>
<li>MQMSG_PRIV_LEVEL_BODY, CORPO,</li>
<li>MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</li>
<li>MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</li>
</ul></td>
</tr>
<tr class="even">
<td><em>Trace</em><br/></td>
<td>Specifica le opzioni di traccia utilizzate nella traccia del routing di Accodamento messaggi.<br/> Valori accettabili:<br/>
<ul>
<li>MQMSG_TRACE_NONE, 0</li>
<li>MQMSG_SEND_ROUTE_TO_REPORT_QUEUE, 1</li>
</ul></td>
</tr>
</tbody>
</table>



 

Il set completo di funzioni SDK di amministrazione COM+ è disponibile tramite oggetti COM. Ciò consente a qualsiasi programma di avviare e arrestare le applicazioni COM+ secondo necessità.

> [!Note]  
> Quando un'applicazione COM+ viene avviata, è l'applicazione in esecuzione, non i singoli componenti all'interno dell'applicazione. Se un'applicazione chiama un componente non in coda, viene avviata l'applicazione COM+ che contiene il componente. Se la casella di controllo listener è abilitata, il listener avvia e inizia l'elaborazione dei messaggi per i componenti in coda. Sebbene il servizio componenti in coda possa essere avviato in questo modo, se i componenti accodati e non accodati vengono inseriti in una singola applicazione COM+, assicurarsi che i componenti accodati vengano avviati se viene eseguito un componente non accodato. In caso contrario, creare un pacchetto dei componenti in coda in un'applicazione COM+ separata dagli altri componenti.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attivazione di code di componenti](activating-component-queues.md)
</dt> </dl>

 

 




