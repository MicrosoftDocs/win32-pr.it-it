---
title: Elemento LOGURL
description: L'elemento LOGURL indica a Windows Media Player di inviare i dati di log all'URL specificato.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Finestra elementi LOGURL Media Player
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327718"
---
# <a name="logurl-element"></a><span data-ttu-id="ec0b1-104">Elemento LOGURL</span><span class="sxs-lookup"><span data-stu-id="ec0b1-104">LOGURL Element</span></span>

<span data-ttu-id="ec0b1-105">L'elemento **LogURL** indica a Windows Media Player di inviare i dati di log all'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-105">The **LOGURL** element instructs Windows Media Player to submit any log data to the specified URL.</span></span>

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="ec0b1-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="ec0b1-106">Attributes</span></span>

<span data-ttu-id="ec0b1-107">**Href** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="ec0b1-107">**HREF** (required)</span></span>

<span data-ttu-id="ec0b1-108">URL di un host in grado di elaborare le richieste di registrazione.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-108">URL to a host that is able to process logging requests.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="ec0b1-109">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="ec0b1-109">Parent/Child Elements</span></span>



| <span data-ttu-id="ec0b1-110">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="ec0b1-110">Hierarchy</span></span>       | <span data-ttu-id="ec0b1-111">Elementi</span><span class="sxs-lookup"><span data-stu-id="ec0b1-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="ec0b1-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ec0b1-112">Parent elements</span></span> | <span data-ttu-id="ec0b1-113">**ASX**, **voce**</span><span class="sxs-lookup"><span data-stu-id="ec0b1-113">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="ec0b1-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ec0b1-114">Child elements</span></span>  | <span data-ttu-id="ec0b1-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="ec0b1-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="ec0b1-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="ec0b1-116">Remarks</span></span>

<span data-ttu-id="ec0b1-117">L'elemento **LogURL** consente a una playlist del metafile client di inviare informazioni di registrazione aggiuntive ai server specificati.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-117">The **LOGURL** element enables a client metafile playlist to send additional logging information to specified servers.</span></span> <span data-ttu-id="ec0b1-118">Le informazioni di registrazione vengono inviate automaticamente al server di origine di una playlist quando viene aperto e a ogni **LogURL** specificato per l'elemento **ASX** , se presenti.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-118">Logging information is automatically sent to the origin server of a playlist when it is opened and to each **LOGURL** specified for the **ASX** element, if any are present.</span></span> <span data-ttu-id="ec0b1-119">Le informazioni di registrazione vengono inviate anche a ogni **LogURL** specificato per un elemento **entry** quando viene raggiunta tale voce.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-119">Logging information is also sent to each **LOGURL** specified for an **ENTRY** element when that entry is reached.</span></span> <span data-ttu-id="ec0b1-120">L'URL specificato nell'attributo **href** di un elemento **LogURL** deve essere l'indirizzo di un host in grado di elaborare le richieste di registrazione.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-120">The URL specified in the **HREF** attribute of a **LOGURL** element must be the address of a host that is able to process logging requests.</span></span> <span data-ttu-id="ec0b1-121">L'URL può essere qualsiasi URL HTTP valido.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-121">The URL can be any valid HTTP URL.</span></span> <span data-ttu-id="ec0b1-122">L'URL può anche indicare la posizione di uno script CGI.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-122">The URL can also indicate the location of a CGI script.</span></span>

<span data-ttu-id="ec0b1-123">Gli unici protocolli validi per un elemento **LogURL** sono http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-123">The only valid protocols for a **LOGURL** element are HTTP and HTTPS.</span></span>

<span data-ttu-id="ec0b1-124">Un elemento **LogURL** all'interno dell'ambito di un elemento **ASX** è applicabile solo al metafile in cui risiede, indipendentemente dal fatto che venga fatto riferimento a tale metafile da un altro metafile.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-124">A **LOGURL** element within the scope of an **ASX** element is applicable only to the metafile in which it resides, regardless of whether that metafile is referenced from another metafile.</span></span> <span data-ttu-id="ec0b1-125">Un elemento **LogURL** forza l'invio di dati di log per tutto il contenuto trasmesso dall'interno dell'ambito definito e solo per il contenuto trasmesso dall'interno dell'ambito definito.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-125">A **LOGURL** element forces the submission of log data for all content streamed from within its defined scope and only for content streamed from within its defined scope.</span></span> <span data-ttu-id="ec0b1-126">I dati di log verranno inviati al server di origine e a tutti gli URL elencati in ogni elemento **LogURL** nell'ambito.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-126">Log data will be submitted to the origin server and to all URLs listed in every **LOGURL** element in scope.</span></span> <span data-ttu-id="ec0b1-127">I dati del log verranno inviati solo una volta a ogni URL elencato, anche se lo stesso URL è elencato più di una volta in un determinato ambito.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-127">Log data will be submitted only once to each listed URL, even if the same URL is listed more than once in a given scope.</span></span> <span data-ttu-id="ec0b1-128">Una ripetizione di una **voce** comporterebbe un altro invio agli URL elencati.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-128">A repeat of an **ENTRY** would result in another submission to the listed URLs.</span></span>

<span data-ttu-id="ec0b1-129">Non esiste alcun limite al numero di elementi **LogURL** in una playlist del metafile.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-129">There is no limit to the number of **LOGURL** elements in a metafile playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="ec0b1-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="ec0b1-130">Examples</span></span>


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



<span data-ttu-id="ec0b1-131">Di seguito sono riportati alcuni esempi di URL validi.</span><span class="sxs-lookup"><span data-stu-id="ec0b1-131">The following are examples of valid URLs.</span></span>

<span data-ttu-id="ec0b1-132">URL di un'applicazione ISAPI:</span><span class="sxs-lookup"><span data-stu-id="ec0b1-132">URL of an ISAPI application:</span></span>


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



<span data-ttu-id="ec0b1-133">URL di uno script CGI:</span><span class="sxs-lookup"><span data-stu-id="ec0b1-133">URL of a CGI script:</span></span>


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



<span data-ttu-id="ec0b1-134">Un URL HTTP valido:</span><span class="sxs-lookup"><span data-stu-id="ec0b1-134">A valid HTTP URL:</span></span>


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a><span data-ttu-id="ec0b1-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec0b1-135">Requirements</span></span>



| <span data-ttu-id="ec0b1-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec0b1-136">Requirement</span></span> | <span data-ttu-id="ec0b1-137">Valore</span><span class="sxs-lookup"><span data-stu-id="ec0b1-137">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="ec0b1-138">Versione</span><span class="sxs-lookup"><span data-stu-id="ec0b1-138">Version</span></span><br/> | <span data-ttu-id="ec0b1-139">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="ec0b1-139">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec0b1-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec0b1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec0b1-141">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ec0b1-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="ec0b1-142">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ec0b1-142">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





