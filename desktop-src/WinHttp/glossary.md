---
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 08951f9f-d03d-4720-8f18-1413ba72e93d
title: Glossario (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74d707c828a9eeb5f07ebf3ec3c1ca92a9d2b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882873"
---
# <a name="glossary-winhttp"></a><span data-ttu-id="f1e81-103">Glossario (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="f1e81-103">Glossary (WinHTTP)</span></span>

<dl> <dt>

<span data-ttu-id="f1e81-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**dati di autenticazione**</span><span class="sxs-lookup"><span data-stu-id="f1e81-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**authentication data**</span></span>
</dt> <dd>

<span data-ttu-id="f1e81-105">Blocco di dati specifico dello schema scambiato tra il server e il client durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f1e81-105">Scheme-specific block of data that is exchanged between the server and client during authentication.</span></span> <span data-ttu-id="f1e81-106">Per dimostrare la propria identità, il client crittografa alcuni o tutti i dati con un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="f1e81-106">To prove its identity, the client encrypts some or all of this data with a user name and password.</span></span> <span data-ttu-id="f1e81-107">Il client invia i dati crittografati al server, che li decrittografa e li confronta con quelli originali.</span><span class="sxs-lookup"><span data-stu-id="f1e81-107">The client sends the encrypted data to the server, which decrypts the data and compares it to the original.</span></span> <span data-ttu-id="f1e81-108">Se i dati decrittografati corrispondono ai dati originali, il client viene autenticato.</span><span class="sxs-lookup"><span data-stu-id="f1e81-108">If the decrypted data matches the original data, the client is authenticated.</span></span>

</dd> <dt>

<span data-ttu-id="f1e81-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**codifica Base64**</span><span class="sxs-lookup"><span data-stu-id="f1e81-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**base64 encoding**</span></span>
</dt> <dd>

<span data-ttu-id="f1e81-110">Schema utilizzato per la trasmissione di dati binari.</span><span class="sxs-lookup"><span data-stu-id="f1e81-110">Scheme used to transmit binary data.</span></span> <span data-ttu-id="f1e81-111">Base64 elabora i dati come gruppi a 24 bit, eseguendo il mapping di questi dati a quattro caratteri codificati.</span><span class="sxs-lookup"><span data-stu-id="f1e81-111">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="f1e81-112">Viene talvolta definito codifica da 3 a 4.</span><span class="sxs-lookup"><span data-stu-id="f1e81-112">It is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="f1e81-113">Ogni 6 bit del gruppo a 24 bit viene utilizzato come indice in una tabella di mapping (alfabeto Base64) per ottenere un carattere per i dati codificati.</span><span class="sxs-lookup"><span data-stu-id="f1e81-113">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="f1e81-114">I dati codificati hanno lunghezze di riga limitate a 76 caratteri.</span><span class="sxs-lookup"><span data-stu-id="f1e81-114">The encoded data has line lengths limited to 76 characters.</span></span>

</dd> <dt>

<span data-ttu-id="f1e81-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**Archivio certificati**</span><span class="sxs-lookup"><span data-stu-id="f1e81-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="f1e81-116">In genere, archiviazione permanente in cui vengono archiviati i certificati, gli elenchi di revoche di certificati (CRL) e gli elenchi di certificati attendibili (CTL).</span><span class="sxs-lookup"><span data-stu-id="f1e81-116">Typically, permanent storage where certificates, certificate revocation lists (CRL), and certificate trust lists (CTL) are stored.</span></span> <span data-ttu-id="f1e81-117">Un archivio certificati può essere anche temporaneo quando si utilizzano certificati basati sulla sessione.</span><span class="sxs-lookup"><span data-stu-id="f1e81-117">A certificate store can also be temporary when working with session-based certificates.</span></span>

</dd> <dt>

<span data-ttu-id="f1e81-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**</span><span class="sxs-lookup"><span data-stu-id="f1e81-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**</span></span>
</dt> <dd>

<span data-ttu-id="f1e81-119">Possibilità per un sito di Microsoft Passport partecipante di fornire i propri elementi di personalizzazione e spiegazioni nelle pagine del servizio di rete Passport.</span><span class="sxs-lookup"><span data-stu-id="f1e81-119">Ability for a Microsoft Passport participant site to provide its own branding elements and explanations on the Passport network service pages.</span></span> <span data-ttu-id="f1e81-120">Il cobranding include la personalizzazione dell'aspetto, del testo specifico e del comportamento specifico nelle pagine della rete Passport.</span><span class="sxs-lookup"><span data-stu-id="f1e81-120">Cobranding includes customizing the look and feel, specific text, and specific behavior on Passport network pages.</span></span>

</dd> <dt>

<span data-ttu-id="f1e81-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**tabella codici**</span><span class="sxs-lookup"><span data-stu-id="f1e81-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**code page**</span></span>
</dt> <dd>

<span data-ttu-id="f1e81-122">Tabella che mette in correlazione i codici carattere binario utilizzati da un programma ai tasti della tastiera o all'aspetto dei caratteri sul monitor.</span><span class="sxs-lookup"><span data-stu-id="f1e81-122">Table that relates the binary character codes used by a program to keys on the keyboard or to the appearance of characters on the monitor.</span></span> <span data-ttu-id="f1e81-123">L'utilizzo di tabelle codici è un modo per fornire supporto per i set di caratteri e i layout di tastiera utilizzati in paesi e aree diverse.</span><span class="sxs-lookup"><span data-stu-id="f1e81-123">Using code pages is a way to provide support for character sets and keyboard layouts used in different countries and regions.</span></span> <span data-ttu-id="f1e81-124">È possibile configurare dispositivi quali il monitoraggio e la tastiera per l'utilizzo di una tabella codici specifica e per passare da una tabella codici (ad esempio Stati Uniti) a un'altra (ad esempio, Portogallo) in base alla richiesta dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f1e81-124">You can configure devices such as the monitor and the keyboard to use a specific code page and to switch from one code page (such as United States) to another (such as Portugal) at the user's request.</span></span>

</dd> <dt>

<span data-ttu-id="f1e81-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**Verbo HTTP**</span><span class="sxs-lookup"><span data-stu-id="f1e81-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**HTTP verb**</span></span>
</dt> <dd>

<span data-ttu-id="f1e81-126">Il verbo HTTP (o il metodo HTTP) è un'istruzione inviata in un messaggio di richiesta che notifica a un server HTTP l'azione da eseguire sulla risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="f1e81-126">The HTTP verb (or HTTP method) is an instruction sent in a request message that notifies an HTTP server of the action to perform on the specified resource.</span></span> <span data-ttu-id="f1e81-127">Ad esempio, "GET" specifica che una risorsa viene recuperata dal server.</span><span class="sxs-lookup"><span data-stu-id="f1e81-127">For example, "GET" specifies that a resource is being retrieved from the server.</span></span> <span data-ttu-id="f1e81-128">I verbi comuni includono "GET", "POST" e "HEAD".</span><span class="sxs-lookup"><span data-stu-id="f1e81-128">Common verbs include "GET", "POST", and "HEAD".</span></span> <span data-ttu-id="f1e81-129">Per ulteriori informazioni e per un elenco completo dei verbi HTTP standard, vedere la specifica HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="f1e81-129">For more information and a complete list of standard HTTP verbs, see the HTTP/1.1 specification.</span></span>

</dd> <dt>

<span data-ttu-id="f1e81-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**ticket**</span><span class="sxs-lookup"><span data-stu-id="f1e81-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**ticket**</span></span>
</dt> <dd>

<span data-ttu-id="f1e81-131">Cookie che contiene un profilo utente per l'autenticazione Passport.</span><span class="sxs-lookup"><span data-stu-id="f1e81-131">Cookie that contains a user profile for Passport authentication.</span></span> <span data-ttu-id="f1e81-132">Ogni ticket corrisponde a un solo URL.</span><span class="sxs-lookup"><span data-stu-id="f1e81-132">Each ticket corresponds to one URL.</span></span> <span data-ttu-id="f1e81-133">Il server di accesso di un'autorità di dominio Passport fornisce i ticket inviati dal client a un membro Passport per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f1e81-133">The logon server of a Passport Domain Authority provides tickets that the client sends to a Passport member for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="f1e81-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**agente utente**</span><span class="sxs-lookup"><span data-stu-id="f1e81-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**user agent**</span></span>
</dt> <dd>

<span data-ttu-id="f1e81-135">L'agente utente è l'applicazione client che richiede un documento da un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="f1e81-135">The user agent is the client application that requests a document from an HTTP server.</span></span> <span data-ttu-id="f1e81-136">Quando il client invia una richiesta a un server HTTP, in genere invia il nome dell'agente utente con l'intestazione della richiesta, in modo che il server possa determinare le funzionalità del software client.</span><span class="sxs-lookup"><span data-stu-id="f1e81-136">When the client sends a request to an HTTP server, typically it sends the name of the user agent with the request header so that the server can determine the capabilities of the client software.</span></span>

</dd> </dl>

 

 



