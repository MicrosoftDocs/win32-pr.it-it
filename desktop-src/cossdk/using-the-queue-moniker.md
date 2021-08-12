---
description: Il moniker della coda viene usato per attivare un componente in coda a livello di codice.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Uso del moniker della coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e83d720478064f1427966de69d98ef06ac82f1da98cc50aa1ec3d3b3ac4c4d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305158"
---
# <a name="using-the-queue-moniker"></a>Uso del moniker della coda

Il moniker della coda viene usato per attivare un componente in coda a livello di codice. Il moniker della coda richiede che riceva l'ID di classe (CLSID) dell'oggetto da richiamare dal nuovo moniker direttamente a destra. Con il prefisso sinistro, il nuovo moniker passa il CLSID al moniker a sinistra.

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Non è valida.

## <a name="visual-basic"></a>Visual Basic

Il parametro del nome visualizzato GetObject è "queue:/new:", seguito dall'ID programma o dal GUID in formato stringa, con o senza parentesi graffe, dell'oggetto server di cui creare un'istanza. Gli esempi seguenti illustrano tre attivazioni valide di un componente con il moniker della coda:

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

Il parametro del nome visualizzato [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) è "queue:/new:", seguito dall'ID programma o dal GUID in formato stringa, con o senza parentesi graffe, dell'oggetto server di cui creare un'istanza. Gli esempi seguenti illustrano tre attivazioni valide di un componente con il moniker della coda:

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

Il moniker della coda accetta parametri facoltativi che modificano le proprietà del messaggio inviato ad Accodamento messaggi. Ad esempio, per inviare il messaggio di accodamento messaggi con priorità 6, il componente in coda viene attivato come segue:

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

Nella tabella seguente sono elencati i parametri del moniker della coda che influiscono sulla coda di destinazione.



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
<td>Specifica la parte relativa al nome computer di un nome di percorso della coda di Accodamento messaggi. Il nome del percorso della coda di Accodamento messaggi è formattato come <em>ComputerName</em> \ <em>QueueName</em>. Se non specificato, viene utilizzato il nome del computer associato all'applicazione configurata.<br/></td>
</tr>
<tr class="even">
<td><em>Queuename</em><br/></td>
<td>Specifica il nome della coda di Accodamento messaggi. Il nome del percorso della coda di Accodamento messaggi è formattato come <em>ComputerName</em> \ <em>QueueName</em>. Se non specificato, viene usato il nome della coda associato all'applicazione configurata.<br/> Per ottenere una coda non transazionale, è possibile specificare prima il nome della coda e quindi creare un'applicazione COM+ con lo stesso nome.<br/></td>
</tr>
<tr class="odd">
<td><em>PathName</em><br/></td>
<td>Specifica il nome completo del percorso della coda di Accodamento messaggi. Se non specificato, viene utilizzato il nome del percorso della coda di Accodamento messaggi associato all'applicazione configurata. Per eseguire l'override del nome di destinazione, è possibile specificare il percorso nel formato seguente per l'installazione di un gruppo di lavoro di Accodamento messaggi:<br/> Coda:<em>PathName</em> = <em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass<br/>
<blockquote>
[!Note]<br />
I linguaggi di programmazione C e Microsoft Visual C++ richiedono due barre rovesciate per rappresentare una barra rovesciata all'interno di valori letterali stringa, ad esempio il libro \\ paga di Chicago.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><em>Formatname</em><br/></td>
<td>Quando si contrassegna un'applicazione COM+ come in coda, COM+ crea una coda di Accodamento messaggi il cui nome corrisponde all'applicazione. Il nome del formato di accodamento messaggi della coda si trova nel catalogo COM+, associato all'applicazione COM+. Per eseguire l'override del nome di destinazione, è possibile specificare il nome di formato nel formato seguente per l'installazione di un gruppo di lavoro di Accodamento messaggi:<br/> Coda:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId<br/> In una configurazione di Active Directory &quot; PRIVATE$ &quot; non viene specificato come parte del nome della coda. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> I parametri facoltativi del moniker della coda vengono elaborati da sinistra a destra. Specificare ogni parola chiave una sola volta. Se si specifica *il parametro PathName,* vengono sostituiti entrambi *i parametri ComputerName* *e QueueName.* Un parametro *FormatName* specifico elimina le conoscenze precedenti di *un parametro ComputerName,* *QueueName* *e PathName.*

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a>Associazione del listener dei componenti in coda a una coda privata specifica

Il listener com+ Queued Components riceve solo dalle code associate all'applicazione COM+ contrassegnate come in coda. Quando si contrassegna un'applicazione COM+ come in coda, COM+ crea una coda di Accodamento messaggi il cui nome corrisponde all'applicazione. Il nome del formato di accodamento messaggi della coda si trova nel catalogo COM+, associato all'applicazione COM+. Quando l'applicazione COM+ viene avviata e contrassegnata come in ascolto, viene avviato un listener nel processo dell'applicazione COM+ e la coda viene aperta. Nella tabella seguente sono elencati i parametri del moniker della coda che influiscono sul messaggio di Accodamento messaggi.



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
<td>Specifica un intero senza segno, ad esempio AppSpecific=12345.<br/></td>
</tr>
<tr class="even">
<td><em>AuthLevel</em><br/></td>
<td>Specifica il livello di autenticazione del messaggio. Un messaggio autenticato è firmato digitalmente e richiede un certificato per l'utente che invia il messaggio. Valori accettabili:<br/>
<ul>
<li>MQMSG_AUTH_LEVEL_NONE,0</li>
<li>MQMSG_AUTH_LEVEL_ALWAYS,1</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Recapito</em><br/></td>
<td>Specifica l'opzione di recapito dei messaggi. Questo valore viene ignorato per le code transazionali. Valori accettabili:<br/>
<ul>
<li>MQMSG_DELIVERY_EXPRESS,0</li>
<li>MQMSG_DELIVERY_RECOVERABLE,1</li>
</ul></td>
</tr>
<tr class="even">
<td><em>EncryptAlgorithm</em><br/></td>
<td>Specifica l'algoritmo di crittografia che deve essere utilizzato da Accodamento messaggi per crittografare e decrittografare il messaggio. Valori accettabili:<br/>
<ul>
<li>CALG_RC2, CALG_RC4</li>
<li>Qualsiasi valore intero accettabile per Accodamento messaggi per <em>un oggetto EncryptAlgorithm.</em></li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Hashalgorithm</em><br/></td>
<td>Specifica una funzione hash crittografica. Valori accettabili:<br/>
<ul>
<li>CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</li>
<li>Qualsiasi valore intero accettabile per Accodamento messaggi per <em>un oggetto HashAlgorithm.</em></li>
</ul></td>
</tr>
<tr class="even">
<td>Rivista<br/></td>
<td>Specifica l'opzione journal del messaggio di accodamento messaggi. Valori accettabili:<br/>
<ul>
<li>MQMSG_JOURNAL_NONE,0</li>
<li>MQMSG_DEADLETTER,1</li>
<li>MQMSG_JOURNAL,2</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Etichetta</em><br/></td>
<td>Specifica una stringa di etichetta del messaggio con un massimo MQ_MAX_MSG_LABEL_LEN caratteri. <br/></td>
</tr>
<tr class="even">
<td><em>MaxTimeToReachQueue</em><br/></td>
<td>Specifica il tempo massimo, in secondi, per il quale il messaggio raggiunge la coda. <br/> Valori accettabili:<br/>
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
<td>Specifica un livello di priorità dei messaggi all'interno dei valori di Accodamento messaggi consentiti.<br/> Valori accettabili:<br/>
<ul>
<li>MQ_MIN_PRIORITY,0</li>
<li>MQ_MAX_PRIORITY,7</li>
<li>MQ_DEFAULT_PRIORITY,3</li>
<li>Numero compreso tra 0 e 7</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>PrivLevel</em><br/></td>
<td>Specifica un livello di privacy, usato per crittografare i messaggi.<br/> Valori accettabili:<br/>
<ul>
<li>MQMSG_PRIV_LEVEL_NONE, NESSUNO, 0</li>
<li>MQMSG_PRIV_LEVEL_BODY, BODY,</li>
<li>MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</li>
<li>MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</li>
</ul></td>
</tr>
<tr class="even">
<td><em>Traccia</em><br/></td>
<td>Specifica le opzioni di traccia, utilizzate nella traccia del routing di Accodamento messaggi.<br/> Valori accettabili:<br/>
<ul>
<li>MQMSG_TRACE_NONE,0</li>
<li>MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</li>
</ul></td>
</tr>
</tbody>
</table>



 

Il set completo di funzioni dell'SDK amministrativo COM+ è disponibile tramite oggetti COM. Ciò consente a qualsiasi programma di avviare e arrestare le applicazioni COM+ in base alle esigenze.

> [!Note]  
> Quando viene avviata un'applicazione COM+, è l'applicazione in esecuzione, non i singoli componenti all'interno dell'applicazione. Se un'applicazione chiama un componente non in coda, viene avviata l'applicazione COM+ che contiene il componente. Se la casella di controllo listener è abilitata, anche il listener avvia e avvia l'elaborazione dei messaggi per i componenti in coda. Anche se il servizio componenti in coda può essere avviato in questo modo, se si in pacchetto componenti in coda e non in coda in una singola applicazione COM+, assicurarsi di voler avviare effettivamente i componenti in coda se viene eseguito un componente non in coda. In caso contrario, creare un pacchetto dei componenti in coda in un'applicazione COM+ separata dagli altri componenti.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attivazione delle code dei componenti](activating-component-queues.md)
</dt> </dl>

 

 




