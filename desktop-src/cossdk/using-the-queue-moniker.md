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
# <a name="using-the-queue-moniker"></a><span data-ttu-id="02b91-103">Utilizzo del moniker della coda</span><span class="sxs-lookup"><span data-stu-id="02b91-103">Using the Queue Moniker</span></span>

<span data-ttu-id="02b91-104">Il moniker della coda viene utilizzato per attivare un componente in coda a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="02b91-104">The queue moniker is used to activate a queued component programmatically.</span></span> <span data-ttu-id="02b91-105">Il moniker della coda richiede la ricezione dell'ID di classe (CLSID) dell'oggetto da richiamare direttamente dal nuovo moniker.</span><span class="sxs-lookup"><span data-stu-id="02b91-105">The queue moniker requires that it receive the class ID (CLSID) of the object to be invoked from the new moniker directly to the right of it.</span></span> <span data-ttu-id="02b91-106">Quando il prefisso è a sinistra, il nuovo moniker passa il CLSID al moniker alla sua sinistra.</span><span class="sxs-lookup"><span data-stu-id="02b91-106">When left-prefixed, the new moniker passes the CLSID to the moniker to the left of it.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="02b91-107">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="02b91-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="02b91-108">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="02b91-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="02b91-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="02b91-109">Visual Basic</span></span>

<span data-ttu-id="02b91-110">Il parametro del nome visualizzato GetObject è "queue:/New:", seguito dall'ID del programma o dal GUID del formato stringa, con o senza parentesi graffe, dell'oggetto server di cui creare un'istanza.</span><span class="sxs-lookup"><span data-stu-id="02b91-110">The GetObject display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="02b91-111">Gli esempi seguenti illustrano tre attivazioni valide di un componente con il moniker della coda:</span><span class="sxs-lookup"><span data-stu-id="02b91-111">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a><span data-ttu-id="02b91-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="02b91-112">C/C++</span></span>

<span data-ttu-id="02b91-113">Il parametro del nome visualizzato [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) è "queue:/New:", seguito dall'ID del programma o dal GUID del formato stringa, con o senza parentesi graffe, dell'oggetto server per cui creare un'istanza.</span><span class="sxs-lookup"><span data-stu-id="02b91-113">The [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="02b91-114">Gli esempi seguenti illustrano tre attivazioni valide di un componente con il moniker della coda:</span><span class="sxs-lookup"><span data-stu-id="02b91-114">The following examples show three valid activations of a component with the queue moniker:</span></span>

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

## <a name="remarks"></a><span data-ttu-id="02b91-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="02b91-115">Remarks</span></span>

<span data-ttu-id="02b91-116">Il moniker della coda accetta parametri facoltativi che modificano le proprietà del messaggio inviato a Accodamento messaggi.</span><span class="sxs-lookup"><span data-stu-id="02b91-116">The queue moniker accepts optional parameters that alter the properties of the message sent to Message Queuing.</span></span> <span data-ttu-id="02b91-117">Ad esempio, per fare in modo che il messaggio di Accodamento messaggi venga inviato con una priorità 6, il componente in coda verrebbe attivato come segue:</span><span class="sxs-lookup"><span data-stu-id="02b91-117">For example, to cause the Message Queuing message to be sent with a priority 6, the queued component would be activated as follows:</span></span>

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

<span data-ttu-id="02b91-118">Nella tabella seguente sono elencati i parametri del moniker della coda che interessano la coda di destinazione.</span><span class="sxs-lookup"><span data-stu-id="02b91-118">The following table lists the queue moniker parameters that affect the destination queue.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02b91-119">Parametro</span><span class="sxs-lookup"><span data-stu-id="02b91-119">Parameter</span></span></th>
<th><span data-ttu-id="02b91-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02b91-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02b91-121"><em>NomeComputer</em></span><span class="sxs-lookup"><span data-stu-id="02b91-121"><em>ComputerName</em></span></span><br/></td>
<td><span data-ttu-id="02b91-122">Specifica la parte relativa al nome del computer di un nome di percorso della coda di Accodamento messaggi.</span><span class="sxs-lookup"><span data-stu-id="02b91-122">Specifies the computer name portion of a Message Queuing queue path name.</span></span> <span data-ttu-id="02b91-123">Il nome del percorso della coda di Accodamento messaggi è formattato come <em>nomecomputer</em> \ <em>QueueName</em>.</span><span class="sxs-lookup"><span data-stu-id="02b91-123">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="02b91-124">Se non specificato, viene usato il nome computer associato all'applicazione configurata.</span><span class="sxs-lookup"><span data-stu-id="02b91-124">If not specified, the computer name associated with the configured application is used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02b91-125"><em>QueueName</em></span><span class="sxs-lookup"><span data-stu-id="02b91-125"><em>QueueName</em></span></span><br/></td>
<td><span data-ttu-id="02b91-126">Specifica il nome della coda di Accodamento messaggi.</span><span class="sxs-lookup"><span data-stu-id="02b91-126">Specifies the Message Queuing queue name.</span></span> <span data-ttu-id="02b91-127">Il nome del percorso della coda di Accodamento messaggi è formattato come <em>nomecomputer</em> \ <em>QueueName</em>.</span><span class="sxs-lookup"><span data-stu-id="02b91-127">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="02b91-128">Se non specificato, viene usato il nome della coda associato all'applicazione configurata.</span><span class="sxs-lookup"><span data-stu-id="02b91-128">If not specified, the queue name associated with the configured application is used.</span></span><br/> <span data-ttu-id="02b91-129">Per ottenere una coda non transazionale, è possibile specificare prima il nome della coda, quindi creare un'applicazione COM+ con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="02b91-129">To get a non-transactional queue, you can specify the queue name first and then create a COM+ application of the same name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02b91-130"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="02b91-130"><em>PathName</em></span></span><br/></td>
<td><span data-ttu-id="02b91-131">Specifica il nome completo del percorso della coda di Accodamento messaggi.</span><span class="sxs-lookup"><span data-stu-id="02b91-131">Specifies the complete Message Queuing queue path name.</span></span> <span data-ttu-id="02b91-132">Se non specificato, viene utilizzato il nome del percorso della coda di Accodamento messaggi associato all'applicazione configurata.</span><span class="sxs-lookup"><span data-stu-id="02b91-132">If not specified, the Message Queuing queue path name associated with the configured application is used.</span></span> <span data-ttu-id="02b91-133">Per eseguire l'override del nome di destinazione, è possibile specificare il percorso nel formato seguente per l'installazione di un gruppo di lavoro di Accodamento messaggi:</span><span class="sxs-lookup"><span data-stu-id="02b91-133">To override the destination name, the path can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="02b91-134">Queue:<em>pathname</em> = <em>nomecomputer</em>\Private $ \ AppName/New: MyProject. CMyClass</span><span class="sxs-lookup"><span data-stu-id="02b91-134">Queue:<em>PathName</em>=<em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="02b91-135">Per entrambi i linguaggi di programmazione C e Microsoft Visual C++ sono necessarie due barre rovesciate per rappresentare una barra rovesciata nei valori letterali stringa, ad esempio la \\ retribuzione di Chicago.</span><span class="sxs-lookup"><span data-stu-id="02b91-135">Both the C and Microsoft Visual C++ programming languages require two backslashes to represent one backslash within string literals for example, chicago\\payroll.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02b91-136"><em>FormatName</em></span><span class="sxs-lookup"><span data-stu-id="02b91-136"><em>FormatName</em></span></span><br/></td>
<td><span data-ttu-id="02b91-137">Quando si contrassegna un'applicazione COM+ come accodata, COM+ crea una coda di Accodamento messaggi il cui nome corrisponde a quello dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="02b91-137">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="02b91-138">Il nome del formato di Accodamento messaggi della coda si trova nel catalogo COM+, associato all'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="02b91-138">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="02b91-139">Per eseguire l'override del nome di destinazione, il nome del formato può essere specificato nel formato seguente per l'installazione di un gruppo di lavoro di Accodamento messaggi:</span><span class="sxs-lookup"><span data-stu-id="02b91-139">To override the destination name, the format name can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="02b91-140">Queue:<em>FormatName</em>= Direct = OS:<em>nomecomputer</em>\Private $ \ AppName/New: ProgID</span><span class="sxs-lookup"><span data-stu-id="02b91-140">Queue:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId</span></span><br/> <span data-ttu-id="02b91-141">In una configurazione di Active Directory, &quot; private $ &quot; non è specificato come parte del nome della coda.</span><span class="sxs-lookup"><span data-stu-id="02b91-141">In an Active Directory configuration, &quot;PRIVATE$&quot; is not specified as part of the queue name.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="02b91-142">I parametri facoltativi del moniker della coda vengono elaborati da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="02b91-142">Optional queue moniker parameters are processed left-to-right.</span></span> <span data-ttu-id="02b91-143">Specificare ogni parola chiave solo una volta.</span><span class="sxs-lookup"><span data-stu-id="02b91-143">Specify each keyword only one time.</span></span> <span data-ttu-id="02b91-144">La specifica del parametro *pathname* sostituisce i parametri *ComputerName* e *QueueName*.</span><span class="sxs-lookup"><span data-stu-id="02b91-144">Specifying the *PathName* parameter replaces both the *ComputerName* and *QueueName* parameters.</span></span> <span data-ttu-id="02b91-145">Un parametro *FormatName* specifico Elimina la conoscenza precedente di un parametro *ComputerName*, *QueueName* e *pathname* .</span><span class="sxs-lookup"><span data-stu-id="02b91-145">A specific *FormatName* parameter deletes prior knowledge of a *ComputerName*, *QueueName*, and *PathName* parameter.</span></span>

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a><span data-ttu-id="02b91-146">Associazione del listener dei componenti in coda a una coda privata specifica</span><span class="sxs-lookup"><span data-stu-id="02b91-146">Associating the Queued Components Listener with a Specific Private Queue</span></span>

<span data-ttu-id="02b91-147">Il listener dei componenti in coda COM+ riceve solo dalle code associate all'applicazione COM+ contrassegnata come accodata.</span><span class="sxs-lookup"><span data-stu-id="02b91-147">The COM+ Queued Components listener receives only from queues associated with the COM+ application marked queued.</span></span> <span data-ttu-id="02b91-148">Quando si contrassegna un'applicazione COM+ come accodata, COM+ crea una coda di Accodamento messaggi il cui nome corrisponde a quello dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="02b91-148">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="02b91-149">Il nome del formato di Accodamento messaggi della coda si trova nel catalogo COM+, associato all'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="02b91-149">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="02b91-150">Quando l'applicazione COM+ viene avviata e contrassegnata come Listen, viene avviato un listener nel processo dell'applicazione COM+ e viene aperta la coda.</span><span class="sxs-lookup"><span data-stu-id="02b91-150">When the COM+ application is started and marked as listen, a listener in the COM+ application process is started and the queue is opened.</span></span> <span data-ttu-id="02b91-151">Nella tabella seguente sono elencati i parametri del moniker della coda che influiscono sul messaggio di Accodamento messaggi.</span><span class="sxs-lookup"><span data-stu-id="02b91-151">The following table lists the queue moniker parameters that affect the Message Queuing message.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02b91-152">Parametro</span><span class="sxs-lookup"><span data-stu-id="02b91-152">Parameter</span></span></th>
<th><span data-ttu-id="02b91-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02b91-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02b91-154"><em>AppSpecific</em></span><span class="sxs-lookup"><span data-stu-id="02b91-154"><em>AppSpecific</em></span></span><br/></td>
<td><span data-ttu-id="02b91-155">Specifica un Unsigned Integer ad esempio, AppSpecific = 12345.</span><span class="sxs-lookup"><span data-stu-id="02b91-155">Specifies an unsigned integer for example, AppSpecific=12345.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02b91-156"><em>AuthLevel</em></span><span class="sxs-lookup"><span data-stu-id="02b91-156"><em>AuthLevel</em></span></span><br/></td>
<td><span data-ttu-id="02b91-157">Specifica il livello di autenticazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="02b91-157">Specifies the message authentication level.</span></span> <span data-ttu-id="02b91-158">Un messaggio autenticato è firmato digitalmente e richiede un certificato per l'utente che invia il messaggio.</span><span class="sxs-lookup"><span data-stu-id="02b91-158">An authenticated message is digitally signed and requires a certificate for the user sending the message.</span></span> <span data-ttu-id="02b91-159">Valori accettabili:</span><span class="sxs-lookup"><span data-stu-id="02b91-159">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="02b91-160">MQMSG_AUTH_LEVEL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="02b91-160">MQMSG_AUTH_LEVEL_NONE,0</span></span></li>
<li><span data-ttu-id="02b91-161">MQMSG_AUTH_LEVEL_ALWAYS, 1</span><span class="sxs-lookup"><span data-stu-id="02b91-161">MQMSG_AUTH_LEVEL_ALWAYS,1</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02b91-162"><em>Recapito</em></span><span class="sxs-lookup"><span data-stu-id="02b91-162"><em>Delivery</em></span></span><br/></td>
<td><span data-ttu-id="02b91-163">Specifica l'opzione di recapito dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="02b91-163">Specifies the message delivery option.</span></span> <span data-ttu-id="02b91-164">Questo valore viene ignorato per le code transazionali.</span><span class="sxs-lookup"><span data-stu-id="02b91-164">This value is ignored for transactional queues.</span></span> <span data-ttu-id="02b91-165">Valori accettabili:</span><span class="sxs-lookup"><span data-stu-id="02b91-165">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="02b91-166">MQMSG_DELIVERY_EXPRESS, 0</span><span class="sxs-lookup"><span data-stu-id="02b91-166">MQMSG_DELIVERY_EXPRESS,0</span></span></li>
<li><span data-ttu-id="02b91-167">MQMSG_DELIVERY_RECOVERABLE, 1</span><span class="sxs-lookup"><span data-stu-id="02b91-167">MQMSG_DELIVERY_RECOVERABLE,1</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02b91-168"><em>EncryptAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="02b91-168"><em>EncryptAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="02b91-169">Specifica l'algoritmo di crittografia che verrà utilizzato da Accodamento messaggi per crittografare e decrittografare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="02b91-169">Specifies the encryption algorithm to be used by Message Queuing to encrypt and decrypt the message.</span></span> <span data-ttu-id="02b91-170">Valori accettabili:</span><span class="sxs-lookup"><span data-stu-id="02b91-170">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="02b91-171">CALG_RC2, CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="02b91-171">CALG_RC2, CALG_RC4</span></span></li>
<li><span data-ttu-id="02b91-172">Qualsiasi valore intero accettabile per l'accodamento dei messaggi per un <em>EncryptAlgorithm</em>.</span><span class="sxs-lookup"><span data-stu-id="02b91-172">Any integer value that is acceptable to Message Queuing for an <em>EncryptAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02b91-173"><em>HashAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="02b91-173"><em>HashAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="02b91-174">Specifica una funzione hash crittografica.</span><span class="sxs-lookup"><span data-stu-id="02b91-174">Specifies a cryptographic hash function.</span></span> <span data-ttu-id="02b91-175">Valori accettabili:</span><span class="sxs-lookup"><span data-stu-id="02b91-175">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="02b91-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="02b91-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span></span></li>
<li><span data-ttu-id="02b91-177">Qualsiasi valore intero accettabile per l'accodamento dei messaggi per un oggetto <em>HashAlgorithm</em>.</span><span class="sxs-lookup"><span data-stu-id="02b91-177">Any integer value that is acceptable to Message Queuing for a <em>HashAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02b91-178">Rivista</span><span class="sxs-lookup"><span data-stu-id="02b91-178">Journal</span></span><br/></td>
<td><span data-ttu-id="02b91-179">Specifica l'opzione del journal dei messaggi di Accodamento messaggi.</span><span class="sxs-lookup"><span data-stu-id="02b91-179">Specifies the Message Queuing message journal option.</span></span> <span data-ttu-id="02b91-180">Valori accettabili:</span><span class="sxs-lookup"><span data-stu-id="02b91-180">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="02b91-181">MQMSG_JOURNAL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="02b91-181">MQMSG_JOURNAL_NONE,0</span></span></li>
<li><span data-ttu-id="02b91-182">MQMSG_DEADLETTER, 1</span><span class="sxs-lookup"><span data-stu-id="02b91-182">MQMSG_DEADLETTER,1</span></span></li>
<li><span data-ttu-id="02b91-183">MQMSG_JOURNAL, 2</span><span class="sxs-lookup"><span data-stu-id="02b91-183">MQMSG_JOURNAL,2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02b91-184"><em>Etichetta</em></span><span class="sxs-lookup"><span data-stu-id="02b91-184"><em>Label</em></span></span><br/></td>
<td><span data-ttu-id="02b91-185">Specifica una stringa di etichetta del messaggio fino a MQ_MAX_MSG_LABEL_LEN caratteri.</span><span class="sxs-lookup"><span data-stu-id="02b91-185">Specifies a message label string up to MQ_MAX_MSG_LABEL_LEN characters.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02b91-186"><em>MaxTimeToReachQueue</em></span><span class="sxs-lookup"><span data-stu-id="02b91-186"><em>MaxTimeToReachQueue</em></span></span><br/></td>
<td><span data-ttu-id="02b91-187">Specifica il tempo massimo, in secondi, per il raggiungimento della coda da parte del messaggio.</span><span class="sxs-lookup"><span data-stu-id="02b91-187">Specifies a maximum time, in seconds, for the message to reach the queue.</span></span> <br/> <span data-ttu-id="02b91-188">Valori accettabili:</span><span class="sxs-lookup"><span data-stu-id="02b91-188">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="02b91-189">INFINITE</span><span class="sxs-lookup"><span data-stu-id="02b91-189">INFINITE</span></span></li>
<li><span data-ttu-id="02b91-190">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="02b91-190">LONG_LIVED</span></span></li>
<li><span data-ttu-id="02b91-191">Numero di secondi</span><span class="sxs-lookup"><span data-stu-id="02b91-191">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02b91-192"><em>MaxTimeToReceive</em></span><span class="sxs-lookup"><span data-stu-id="02b91-192"><em>MaxTimeToReceive</em></span></span><br/></td>
<td><span data-ttu-id="02b91-193">Specifica il tempo massimo, in secondi, per la ricezione del messaggio da parte dell'applicazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="02b91-193">Specifies a maximum time, in seconds, for the message to be received by the target application.</span></span> <span data-ttu-id="02b91-194">Valori accettabili:</span><span class="sxs-lookup"><span data-stu-id="02b91-194">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="02b91-195">INFINITE</span><span class="sxs-lookup"><span data-stu-id="02b91-195">INFINITE</span></span></li>
<li><span data-ttu-id="02b91-196">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="02b91-196">LONG_LIVED</span></span></li>
<li><span data-ttu-id="02b91-197">Numero di secondi</span><span class="sxs-lookup"><span data-stu-id="02b91-197">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02b91-198"><em>Priorità</em></span><span class="sxs-lookup"><span data-stu-id="02b91-198"><em>Priority</em></span></span><br/></td>
<td><span data-ttu-id="02b91-199">Specifica un livello di priorità del messaggio, all'interno dei valori di Accodamento messaggi consentiti.</span><span class="sxs-lookup"><span data-stu-id="02b91-199">Specifies a message priority level, within the Message Queuing values permitted.</span></span><br/> <span data-ttu-id="02b91-200">Valori accettabili:</span><span class="sxs-lookup"><span data-stu-id="02b91-200">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="02b91-201">MQ_MIN_PRIORITY, 0</span><span class="sxs-lookup"><span data-stu-id="02b91-201">MQ_MIN_PRIORITY,0</span></span></li>
<li><span data-ttu-id="02b91-202">MQ_MAX_PRIORITY, 7</span><span class="sxs-lookup"><span data-stu-id="02b91-202">MQ_MAX_PRIORITY,7</span></span></li>
<li><span data-ttu-id="02b91-203">MQ_DEFAULT_PRIORITY, 3</span><span class="sxs-lookup"><span data-stu-id="02b91-203">MQ_DEFAULT_PRIORITY,3</span></span></li>
<li><span data-ttu-id="02b91-204">Numero compreso tra 0 e 7</span><span class="sxs-lookup"><span data-stu-id="02b91-204">Number between 0 and 7</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02b91-205"><em>PrivLevel</em></span><span class="sxs-lookup"><span data-stu-id="02b91-205"><em>PrivLevel</em></span></span><br/></td>
<td><span data-ttu-id="02b91-206">Specifica un livello di privacy utilizzato per crittografare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="02b91-206">Specifies a privacy level, used to encrypt messages.</span></span><br/> <span data-ttu-id="02b91-207">Valori accettabili:</span><span class="sxs-lookup"><span data-stu-id="02b91-207">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="02b91-208">MQMSG_PRIV_LEVEL_NONE, NESSUNA, 0</span><span class="sxs-lookup"><span data-stu-id="02b91-208">MQMSG_PRIV_LEVEL_NONE, NONE, 0</span></span></li>
<li><span data-ttu-id="02b91-209">MQMSG_PRIV_LEVEL_BODY, CORPO,</span><span class="sxs-lookup"><span data-stu-id="02b91-209">MQMSG_PRIV_LEVEL_BODY, BODY,</span></span></li>
<li><span data-ttu-id="02b91-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span><span class="sxs-lookup"><span data-stu-id="02b91-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span></span></li>
<li><span data-ttu-id="02b91-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span><span class="sxs-lookup"><span data-stu-id="02b91-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02b91-212"><em>Trace</em></span><span class="sxs-lookup"><span data-stu-id="02b91-212"><em>Trace</em></span></span><br/></td>
<td><span data-ttu-id="02b91-213">Specifica le opzioni di traccia utilizzate nella traccia del routing di Accodamento messaggi.</span><span class="sxs-lookup"><span data-stu-id="02b91-213">Specifies trace options, used in tracing Message Queuing routing.</span></span><br/> <span data-ttu-id="02b91-214">Valori accettabili:</span><span class="sxs-lookup"><span data-stu-id="02b91-214">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="02b91-215">MQMSG_TRACE_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="02b91-215">MQMSG_TRACE_NONE,0</span></span></li>
<li><span data-ttu-id="02b91-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE, 1</span><span class="sxs-lookup"><span data-stu-id="02b91-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="02b91-217">Il set completo di funzioni SDK di amministrazione COM+ è disponibile tramite oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="02b91-217">The complete set of COM+ Administrative SDK functions is available by using COM objects.</span></span> <span data-ttu-id="02b91-218">Ciò consente a qualsiasi programma di avviare e arrestare le applicazioni COM+ secondo necessità.</span><span class="sxs-lookup"><span data-stu-id="02b91-218">This allows any program to start and stop COM+ applications as required.</span></span>

> [!Note]  
> <span data-ttu-id="02b91-219">Quando un'applicazione COM+ viene avviata, è l'applicazione in esecuzione, non i singoli componenti all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="02b91-219">When a COM+ application is started, it is the application that is running, not the individual components within the application.</span></span> <span data-ttu-id="02b91-220">Se un'applicazione chiama un componente non in coda, viene avviata l'applicazione COM+ che contiene il componente.</span><span class="sxs-lookup"><span data-stu-id="02b91-220">If an application calls a non-queued component, the COM+ application that contains the component is started.</span></span> <span data-ttu-id="02b91-221">Se la casella di controllo listener è abilitata, il listener avvia e inizia l'elaborazione dei messaggi per i componenti in coda.</span><span class="sxs-lookup"><span data-stu-id="02b91-221">If the listener check box is enabled, the listener also starts and begins processing for messages for queued components.</span></span> <span data-ttu-id="02b91-222">Sebbene il servizio componenti in coda possa essere avviato in questo modo, se i componenti accodati e non accodati vengono inseriti in una singola applicazione COM+, assicurarsi che i componenti accodati vengano avviati se viene eseguito un componente non accodato.</span><span class="sxs-lookup"><span data-stu-id="02b91-222">While the queued components service can be started in this way, if you package queued and non-queued components into a single COM+ application, be sure that you really want queued components to start if a non-queued component is executed.</span></span> <span data-ttu-id="02b91-223">In caso contrario, creare un pacchetto dei componenti in coda in un'applicazione COM+ separata dagli altri componenti.</span><span class="sxs-lookup"><span data-stu-id="02b91-223">If this is not the case, package the queued components into a COM+ application that is separate from the other components.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="02b91-224">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02b91-224">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02b91-225">Attivazione di code di componenti</span><span class="sxs-lookup"><span data-stu-id="02b91-225">Activating Component Queues</span></span>](activating-component-queues.md)
</dt> </dl>

 

 




