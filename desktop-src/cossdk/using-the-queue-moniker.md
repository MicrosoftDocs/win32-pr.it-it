---
description: Il moniker della coda viene usato per attivare un componente in coda a livello di codice.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Uso del moniker della coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938b4c0c8afc19e953d7f62f17f95bbd63f387e6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473687"
---
# <a name="using-the-queue-moniker"></a>Uso del moniker della coda

Il moniker della coda viene usato per attivare un componente in coda a livello di codice. Il moniker della coda richiede che riceva l'ID di classe (CLSID) dell'oggetto da richiamare dal nuovo moniker direttamente a destra. Con il prefisso a sinistra, il nuovo moniker passa il CLSID al moniker a sinistra.

## <a name="component-services-administrative-tool"></a>Strumento amministrativo servizi componenti

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

Il parametro del nome [**visualizzato CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) è "queue:/new:", seguito dall'ID programma o dal GUID in formato stringa, con o senza parentesi graffe, dell'oggetto server di cui creare un'istanza. Gli esempi seguenti illustrano tre attivazioni valide di un componente con il moniker della coda:

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

Il moniker della coda accetta parametri facoltativi che modificano le proprietà del messaggio inviato ad Accodamento messaggi. Ad esempio, per inviare il messaggio di Accodamento messaggi con priorità 6, il componente in coda viene attivato come segue:

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

Nella tabella seguente sono elencati i parametri del moniker della coda che influiscono sulla coda di destinazione.




| Parametro | Descrizione | 
|-----------|-------------|
| <em>NomeComputer</em><br /> | Specifica la parte del nome computer di un nome di percorso della coda di Accodamento messaggi. Il nome del percorso della coda di Accodamento messaggi è formattato come <em>ComputerName</em> \<em> QueueName </em> . Se non viene specificato, viene usato il nome del computer associato all'applicazione configurata.<br /> | 
| <em>Queuename</em><br /> | Specifica il nome della coda di Accodamento messaggi. Il nome del percorso della coda di Accodamento messaggi è formattato come <em>ComputerName</em> \<em> QueueName </em> . Se non viene specificato, viene usato il nome della coda associato all'applicazione configurata.<br /> Per ottenere una coda non transazionale, è possibile specificare prima il nome della coda e quindi creare un'applicazione COM+ con lo stesso nome.<br /> | 
| <em>PathName</em><br /> | Specifica il nome completo del percorso della coda di Accodamento messaggi. Se non viene specificato, viene usato il nome del percorso della coda di Accodamento messaggi associato all'applicazione configurata. Per eseguire l'override del nome di destinazione, è possibile specificare il percorso nel formato seguente per l'installazione di un gruppo di lavoro di Accodamento messaggi:<br /> Coda:<em>PathName</em> = <em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass<br /><blockquote>[!Note]<br />Entrambi i linguaggi di programmazione C e Microsoft Visual C++ richiedono due barre rovesciate per rappresentare una barra rovesciata all'interno di valori letterali stringa, ad esempio chicago \\ payroll.</blockquote><br /> | 
| <em>Formatname</em><br /> | Quando si contrassegna un'applicazione COM+ come in coda, COM+ crea una coda di Accodamento messaggi il cui nome è lo stesso dell'applicazione. Il nome di formato di Accodamento messaggi della coda si trova nel catalogo COM+, associato all'applicazione COM+. Per eseguire l'override del nome di destinazione, è possibile specificare il nome di formato nel formato seguente per l'installazione di un gruppo di lavoro di Accodamento messaggi:<br /> Coda:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId<br /> In una configurazione di Active Directory "PRIVATE$" non è specificato come parte del nome della coda. <br /> | 




 

> [!Note]  
> I parametri facoltativi del moniker della coda vengono elaborati da sinistra a destra. Specificare ogni parola chiave una sola volta. Se si specifica il *parametro PathName,* vengono sostituiti entrambi i *parametri ComputerName* *e QueueName.* Un parametro *FormatName* specifico elimina le conoscenze precedenti di *un parametro ComputerName,* *QueueName* *e PathName.*

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a>Associazione del listener dei componenti in coda a una coda privata specifica

Il listener com+ Queued Components riceve solo dalle code associate all'applicazione COM+ contrassegnata come in coda. Quando si contrassegna un'applicazione COM+ come in coda, COM+ crea una coda di Accodamento messaggi il cui nome è lo stesso dell'applicazione. Il nome di formato di Accodamento messaggi della coda si trova nel catalogo COM+, associato all'applicazione COM+. Quando l'applicazione COM+ viene avviata e contrassegnata come in ascolto, viene avviato un listener nel processo dell'applicazione COM+ e viene aperta la coda. Nella tabella seguente sono elencati i parametri del moniker della coda che influiscono sul messaggio di Accodamento messaggi.




| Parametro | Descrizione | 
|-----------|-------------|
| <em>AppSpecific</em><br /> | Specifica un intero senza segno, ad esempio AppSpecific=12345.<br /> | 
| <em>AuthLevel</em><br /> | Specifica il livello di autenticazione del messaggio. Un messaggio autenticato è firmato digitalmente e richiede un certificato per l'utente che invia il messaggio. Valori accettabili:<br /><ul><li>MQMSG_AUTH_LEVEL_NONE,0</li><li>MQMSG_AUTH_LEVEL_ALWAYS,1</li></ul> | 
| <em>Recapito</em><br /> | Specifica l'opzione di recapito dei messaggi. Questo valore viene ignorato per le code transazionali. Valori accettabili:<br /><ul><li>MQMSG_DELIVERY_EXPRESS,0</li><li>MQMSG_DELIVERY_RECOVERABLE,1</li></ul> | 
| <em>EncryptAlgorithm</em><br /> | Specifica l'algoritmo di crittografia che verrà utilizzato da Accodamento messaggi per crittografare e decrittografare il messaggio. Valori accettabili:<br /><ul><li>CALG_RC2, CALG_RC4</li><li>Qualsiasi valore intero accettabile per Accodamento messaggi per <em>encryptAlgorithm</em>.</li></ul> | 
| <em>Hashalgorithm</em><br /> | Specifica una funzione hash crittografica. Valori accettabili:<br /><ul><li>CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</li><li>Qualsiasi valore intero accettabile per Accodamento messaggi per <em>un oggetto HashAlgorithm</em>.</li></ul> | 
| Rivista<br /> | Specifica l'opzione journal dei messaggi di Accodamento messaggi. Valori accettabili:<br /><ul><li>MQMSG_JOURNAL_NONE,0</li><li>MQMSG_DEADLETTER,1</li><li>MQMSG_JOURNAL,2</li></ul> | 
| <em>Etichetta</em><br /> | Specifica una stringa di etichetta del messaggio fino MQ_MAX_MSG_LABEL_LEN caratteri. <br /> | 
| <em>MaxTimeToReachQueue</em><br /> | Specifica il tempo massimo, in secondi, per il quale il messaggio raggiunge la coda. <br /> Valori accettabili:<br /><ul><li>INFINITE</li><li>LONG_LIVED</li><li>Numero di secondi</li></ul> | 
| <em>MaxTimeToReceive</em><br /> | Specifica il tempo massimo, in secondi, per la ricezione del messaggio da parte dell'applicazione di destinazione. Valori accettabili:<br /><ul><li>INFINITE</li><li>LONG_LIVED</li><li>Numero di secondi</li></ul> | 
| <em>Priorità</em><br /> | Specifica un livello di priorità del messaggio, all'interno dei valori consentiti di Accodamento messaggi.<br /> Valori accettabili:<br /><ul><li>MQ_MIN_PRIORITY,0</li><li>MQ_MAX_PRIORITY,7</li><li>MQ_DEFAULT_PRIORITY,3</li><li>Numero compreso tra 0 e 7</li></ul> | 
| <em>PrivLevel</em><br /> | Specifica un livello di privacy, utilizzato per crittografare i messaggi.<br /> Valori accettabili:<br /><ul><li>MQMSG_PRIV_LEVEL_NONE, NONE, 0</li><li>MQMSG_PRIV_LEVEL_BODY, BODY,</li><li>MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</li><li>MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</li></ul> | 
| <em>Trace</em><br /> | Specifica le opzioni di traccia utilizzate nella traccia del routing di Accodamento messaggi.<br /> Valori accettabili:<br /><ul><li>MQMSG_TRACE_NONE,0</li><li>MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</li></ul> | 




 

Il set completo di funzioni di COM+ Administrative SDK è disponibile tramite oggetti COM. Ciò consente a qualsiasi programma di avviare e arrestare le applicazioni COM+ in base alle esigenze.

> [!Note]  
> Quando viene avviata un'applicazione COM+, è l'applicazione in esecuzione, non i singoli componenti all'interno dell'applicazione. Se un'applicazione chiama un componente non in coda, viene avviata l'applicazione COM+ che contiene il componente. Se la casella di controllo del listener è abilitata, il listener avvia e avvia anche l'elaborazione dei messaggi per i componenti in coda. Anche se il servizio dei componenti in coda può essere avviato in questo modo, se si insaccoderanno i componenti in coda e non in coda in una singola applicazione COM+, assicurarsi di voler avviare effettivamente i componenti in coda se viene eseguito un componente non in coda. In caso contrario, creare un pacchetto dei componenti in coda in un'applicazione COM+ separata dagli altri componenti.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attivazione delle code dei componenti](activating-component-queues.md)
</dt> </dl>

 

 




