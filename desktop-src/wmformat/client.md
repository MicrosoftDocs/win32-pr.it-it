---
title: Registrazione client (Windows Media Format 11 SDK)
description: Informazioni sulla registrazione client per Windows Media Format 11 SDK. La registrazione consente al server multimediale di tenere traccia dell'attività dei client che si connettono a esso.
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media Format SDK, registrazione client
- Windows Media Format SDK, registrazione
- Advanced Systems Format (ASF), registrazione client
- ASF (Advanced Systems Format), registrazione client
- Advanced Systems Format (ASF), registrazione
- ASF (Advanced Systems Format), registrazione
- registrazione client
- client di registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095e01fcf0730fdec8d06a931a9a988ca79ea77f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406264"
---
# <a name="client-logging-windows-media-format-11-sdk"></a><span data-ttu-id="6bc2d-112">Registrazione client (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="6bc2d-112">Client Logging (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="6bc2d-113">Quando l'oggetto lettore legge i dati da un server, invia le informazioni di registrazione al server.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-113">When the reader object reads data from a server, it sends logging information to the server.</span></span> <span data-ttu-id="6bc2d-114">I provider di contenuti usano in genere queste informazioni per misurare la qualità del servizio, generare informazioni di fatturazione o tenere traccia della pubblicità.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-114">Content providers typically use this information to measure quality of service, generate billing information, or track advertising.</span></span> <span data-ttu-id="6bc2d-115">Le informazioni di registrazione non contengono dati personali.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-115">The logging information contains no personal data.</span></span>

<span data-ttu-id="6bc2d-116">L'applicazione può specificare alcune delle informazioni registrate chiamando il metodo [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) sull'oggetto lettore.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-116">The application can specify some of the information that is logged, by calling the [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) method on the reader object.</span></span> <span data-ttu-id="6bc2d-117">Ad esempio, è possibile specificare la stringa agente utente, il nome dell'applicazione lettore o la pagina Web che ospita il lettore.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-117">For example, you can specify the user-agent string, the name of the player application, or the Web page that hosts the player.</span></span>

<span data-ttu-id="6bc2d-118">Le informazioni di registrazione includono un GUID che identifica la sessione.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-118">The logging information includes a GUID that identifies the session.</span></span> <span data-ttu-id="6bc2d-119">Per impostazione predefinita, il lettore genera un ID sessione anonimo.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-119">By default, the reader generates an anonymous session ID.</span></span> <span data-ttu-id="6bc2d-120">Facoltativamente, il lettore può invece inviare un ID che identifica in modo univoco l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-120">Optionally, the reader can instead send an ID that uniquely identifies the current user.</span></span> <span data-ttu-id="6bc2d-121">Per abilitare questa funzionalità, chiamare il metodo [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) con il valore **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="6bc2d-121">To enable this feature, call the [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) method with the value **TRUE**.</span></span>

<span data-ttu-id="6bc2d-122">È possibile configurare l'oggetto lettore per inviare le informazioni di registrazione a un altro server, oltre al server di origine.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-122">You can configure the reader object to send the logging information to another server, in addition to the originating server.</span></span> <span data-ttu-id="6bc2d-123">A tale scopo, chiamare il [**metodo IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) con l'URL del server.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-123">To do so, call the [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) method with the URL of the server.</span></span> <span data-ttu-id="6bc2d-124">Questo URL deve puntare a uno script o a un eseguibile in grado di gestire le richieste HTTP GET e POST.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-124">This URL should point to a script or executable that can handle HTTP GET and POST requests.</span></span> <span data-ttu-id="6bc2d-125">È possibile usare Multicast e Logging Advertisement Agent (wmsiislog.dll) oppure scrivere uno script ASP o CGI personalizzato per ricevere i dati di log.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-125">You can use the Multicast and Logging Advertisement Agent (wmsiislog.dll), or you can write a custom ASP or CGI script to receive the log data.</span></span>

> [!Note]  
> <span data-ttu-id="6bc2d-126">È possibile ottenere la stessa funzionalità creando una playlist sul lato server con un **attributo logURL.**</span><span class="sxs-lookup"><span data-stu-id="6bc2d-126">You can get the same functionality by creating a server-side playlist with a **logURL** attribute.</span></span>

 

<span data-ttu-id="6bc2d-127">Quando l'oggetto lettore invia il log, esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6bc2d-127">When the reader object sends the log, it does the following:</span></span>

1.  <span data-ttu-id="6bc2d-128">Invia una richiesta GET vuota al server.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-128">Sends an empty GET request to the server.</span></span>
2.  <span data-ttu-id="6bc2d-129">Analizza la risposta del server per una delle stringhe seguenti:</span><span class="sxs-lookup"><span data-stu-id="6bc2d-129">Parses the server response for one of the following strings:</span></span>
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   <span data-ttu-id="6bc2d-130">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` dove "0.0.0.0" è qualsiasi numero di versione valido.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-130">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` where "0.0.0.0" is any valid version number.</span></span>
3.  <span data-ttu-id="6bc2d-131">Invia una richiesta POST con le informazioni di log.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-131">Sends a POST request with the log information.</span></span>

<span data-ttu-id="6bc2d-132">Il codice seguente illustra uno script ASP di esempio che riceve le informazioni di registrazione e le scrive in un file:</span><span class="sxs-lookup"><span data-stu-id="6bc2d-132">The following code shows an example ASP script that receives the logging information and writes it to a file:</span></span>


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



<span data-ttu-id="6bc2d-133">È possibile specificare più server per ricevere le informazioni di registrazione. è sufficiente chiamare **Una sola volta AddLoggingUrl** con ogni URL.</span><span class="sxs-lookup"><span data-stu-id="6bc2d-133">You can specify multiple servers to receive logging information; just call **AddLoggingUrl** once with each URL.</span></span> <span data-ttu-id="6bc2d-134">Per cancellare l'elenco dei server che ricevono i log, chiamare il [**metodo IWMReaderNetworkConfig::ResetLoggingUrlList.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist)</span><span class="sxs-lookup"><span data-stu-id="6bc2d-134">To clear the list of servers that receive logs, call the [**IWMReaderNetworkConfig::ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bc2d-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6bc2d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bc2d-136">**Implementazione della funzionalità di rete**</span><span class="sxs-lookup"><span data-stu-id="6bc2d-136">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="6bc2d-137">**Interfaccia IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="6bc2d-137">**IWMReaderAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[<span data-ttu-id="6bc2d-138">**Interfaccia IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="6bc2d-138">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




