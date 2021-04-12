---
title: Registrazione client (Windows Media Format 11 SDK)
description: Registrazione client
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media Format SDK, registrazione client
- Windows Media Format SDK, registrazione
- ASF (Advanced Systems Format), registrazione client
- ASF (formato avanzato dei sistemi), registrazione client
- ASF (Advanced Systems Format), registrazione
- ASF (formato avanzato dei sistemi), registrazione
- registrazione client
- registrazione dei client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856f2df4c2377b94edc40574c3e2efcced34aa81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118735"
---
# <a name="client-logging-windows-media-format-11-sdk"></a><span data-ttu-id="5d2b9-111">Registrazione client (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="5d2b9-111">Client Logging (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="5d2b9-112">Quando l'oggetto Reader legge i dati da un server, invia le informazioni di registrazione al server.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-112">When the reader object reads data from a server, it sends logging information to the server.</span></span> <span data-ttu-id="5d2b9-113">I provider di contenuti usano in genere queste informazioni per misurare la qualità del servizio, generare informazioni di fatturazione o tenere traccia degli annunci.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-113">Content providers typically use this information to measure quality of service, generate billing information, or track advertising.</span></span> <span data-ttu-id="5d2b9-114">Le informazioni di registrazione non contengono dati personali.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-114">The logging information contains no personal data.</span></span>

<span data-ttu-id="5d2b9-115">L'applicazione può specificare alcune delle informazioni registrate, chiamando il metodo [**IWMReaderAdvanced:: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) sull'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-115">The application can specify some of the information that is logged, by calling the [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) method on the reader object.</span></span> <span data-ttu-id="5d2b9-116">Ad esempio, è possibile specificare la stringa dell'agente utente, il nome dell'applicazione lettore o la pagina Web che ospita il lettore.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-116">For example, you can specify the user-agent string, the name of the player application, or the Web page that hosts the player.</span></span>

<span data-ttu-id="5d2b9-117">Le informazioni di registrazione includono un GUID che identifica la sessione.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-117">The logging information includes a GUID that identifies the session.</span></span> <span data-ttu-id="5d2b9-118">Per impostazione predefinita, il lettore genera un ID di sessione anonimo.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-118">By default, the reader generates an anonymous session ID.</span></span> <span data-ttu-id="5d2b9-119">Facoltativamente, il lettore può invece inviare un ID che identifica in modo univoco l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-119">Optionally, the reader can instead send an ID that uniquely identifies the current user.</span></span> <span data-ttu-id="5d2b9-120">Per abilitare questa funzionalità, chiamare il metodo [**IWMReaderAdvanced2:: SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-120">To enable this feature, call the [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) method with the value **TRUE**.</span></span>

<span data-ttu-id="5d2b9-121">È possibile configurare l'oggetto Reader per inviare le informazioni di registrazione a un altro server, oltre al server di origine.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-121">You can configure the reader object to send the logging information to another server, in addition to the originating server.</span></span> <span data-ttu-id="5d2b9-122">A tale scopo, chiamare il metodo [**IWMReaderNetworkConfig:: AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) con l'URL del server.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-122">To do so, call the [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) method with the URL of the server.</span></span> <span data-ttu-id="5d2b9-123">Questo URL deve puntare a uno script o un eseguibile in grado di gestire richieste HTTP GET e POST.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-123">This URL should point to a script or executable that can handle HTTP GET and POST requests.</span></span> <span data-ttu-id="5d2b9-124">È possibile utilizzare l'agente di annuncio multicast e di registrazione (wmsiislog.dll) oppure è possibile scrivere uno script ASP o CGI personalizzato per ricevere i dati di log.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-124">You can use the Multicast and Logging Advertisement Agent (wmsiislog.dll), or you can write a custom ASP or CGI script to receive the log data.</span></span>

> [!Note]  
> <span data-ttu-id="5d2b9-125">Per ottenere la stessa funzionalità, è possibile creare una playlist sul lato server con un attributo **LogURL** .</span><span class="sxs-lookup"><span data-stu-id="5d2b9-125">You can get the same functionality by creating a server-side playlist with a **logURL** attribute.</span></span>

 

<span data-ttu-id="5d2b9-126">Quando l'oggetto Reader invia il log, esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5d2b9-126">When the reader object sends the log, it does the following:</span></span>

1.  <span data-ttu-id="5d2b9-127">Invia una richiesta GET vuota al server.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-127">Sends an empty GET request to the server.</span></span>
2.  <span data-ttu-id="5d2b9-128">Analizza la risposta del server per una delle stringhe seguenti:</span><span class="sxs-lookup"><span data-stu-id="5d2b9-128">Parses the server response for one of the following strings:</span></span>
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   <span data-ttu-id="5d2b9-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` dove "0.0.0.0" è un numero di versione valido.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` where "0.0.0.0" is any valid version number.</span></span>
3.  <span data-ttu-id="5d2b9-130">Invia una richiesta POST con le informazioni sul log.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-130">Sends a POST request with the log information.</span></span>

<span data-ttu-id="5d2b9-131">Il codice seguente mostra uno script ASP di esempio che riceve le informazioni di registrazione e le scrive in un file:</span><span class="sxs-lookup"><span data-stu-id="5d2b9-131">The following code shows an example ASP script that receives the logging information and writes it to a file:</span></span>


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



<span data-ttu-id="5d2b9-132">È possibile specificare più server per ricevere le informazioni di registrazione; è sufficiente chiamare **AddLoggingUrl** una volta con ogni URL.</span><span class="sxs-lookup"><span data-stu-id="5d2b9-132">You can specify multiple servers to receive logging information; just call **AddLoggingUrl** once with each URL.</span></span> <span data-ttu-id="5d2b9-133">Per cancellare l'elenco dei server che ricevono i log, chiamare il metodo [**IWMReaderNetworkConfig:: ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) .</span><span class="sxs-lookup"><span data-stu-id="5d2b9-133">To clear the list of servers that receive logs, call the [**IWMReaderNetworkConfig::ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d2b9-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d2b9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d2b9-135">**Implementazione della funzionalità di rete**</span><span class="sxs-lookup"><span data-stu-id="5d2b9-135">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="5d2b9-136">**Interfaccia IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="5d2b9-136">**IWMReaderAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[<span data-ttu-id="5d2b9-137">**Interfaccia IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="5d2b9-137">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




