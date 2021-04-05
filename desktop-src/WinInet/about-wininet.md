---
title: Informazioni su WinINet
description: Windows Internet (WinINet) Application Programming Interface (API) consente all'applicazione di interagire con i protocolli FTP e HTTP per accedere alle risorse Internet.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- Informazioni su WinINet WinINet
- WinINet WinINet, informazioni
- WinInet WinINet, pagina iniziale
- Windows Internet WinINet
- Internet, Windows Internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103956226"
---
# <a name="about-wininet"></a><span data-ttu-id="bf4a5-108">Informazioni su WinINet</span><span class="sxs-lookup"><span data-stu-id="bf4a5-108">About WinINet</span></span>

> [!NOTE]
> <span data-ttu-id="bf4a5-109">Per i contenitori di app a partire da Windows 10, versione 1709, HTTP/2 (vedere [RFC7540](https://tools.ietf.org/html/rfc7540)) è attiva per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bf4a5-109">For app containers since Windows 10, version 1709, HTTP/2 (see [RFC7540](https://tools.ietf.org/html/rfc7540)) is on by default.</span></span>

<span data-ttu-id="bf4a5-110">Windows Internet (WinINet) Application Programming Interface (API) consente all'applicazione di interagire con i protocolli FTP e HTTP per accedere alle risorse Internet.</span><span class="sxs-lookup"><span data-stu-id="bf4a5-110">The Windows Internet (WinINet) application programming interface (API) enables your application to interact with FTP and HTTP protocols to access Internet resources.</span></span> <span data-ttu-id="bf4a5-111">Con l'evolversi degli standard, queste funzioni gestiscono le modifiche apportate ai protocolli sottostanti, consentendo loro di mantenere un comportamento coerente.</span><span class="sxs-lookup"><span data-stu-id="bf4a5-111">As standards evolve, these functions handle the changes in underlying protocols, enabling them to maintain consistent behavior.</span></span>

<span data-ttu-id="bf4a5-112">**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Inoltre, le applicazioni sono abilitate per interagire con gopher.</span><span class="sxs-lookup"><span data-stu-id="bf4a5-112">**Windows XP and Windows Server 2003 R2 and earlier:** Also enabled applications to interact with Gopher.</span></span>

<span data-ttu-id="bf4a5-113">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="bf4a5-113">For more information, see:</span></span>

-   [<span data-ttu-id="bf4a5-114">WinINet rispetto a WinHTTP</span><span class="sxs-lookup"><span data-stu-id="bf4a5-114">WinINet vs. WinHTTP</span></span>](wininet-vs-winhttp.md)
-   [<span data-ttu-id="bf4a5-115">Handle HINTERNET</span><span class="sxs-lookup"><span data-stu-id="bf4a5-115">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
-   [<span data-ttu-id="bf4a5-116">Supporto IP versione 6</span><span class="sxs-lookup"><span data-stu-id="bf4a5-116">IP Version 6 Support</span></span>](ip-version-6-support.md)
-   [<span data-ttu-id="bf4a5-117">Codifica del contenuto \_</span><span class="sxs-lookup"><span data-stu-id="bf4a5-117">Content\_Encoding</span></span>](content-encoding.md)
-   [<span data-ttu-id="bf4a5-118">Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="bf4a5-118">Caching</span></span>](caching.md)
-   [<span data-ttu-id="bf4a5-119">Funzioni comuni</span><span class="sxs-lookup"><span data-stu-id="bf4a5-119">Common Functions</span></span>](common-functions.md)
-   [<span data-ttu-id="bf4a5-120">Sessioni FTP</span><span class="sxs-lookup"><span data-stu-id="bf4a5-120">FTP Sessions</span></span>](ftp-sessions.md)
-   [<span data-ttu-id="bf4a5-121">Sessioni HTTP</span><span class="sxs-lookup"><span data-stu-id="bf4a5-121">HTTP Sessions</span></span>](http-sessions.md)
-   [<span data-ttu-id="bf4a5-122">Cookie HTTP</span><span class="sxs-lookup"><span data-stu-id="bf4a5-122">HTTP Cookies</span></span>](http-cookies.md)
-   [<span data-ttu-id="bf4a5-123">Operazione asincrona</span><span class="sxs-lookup"><span data-stu-id="bf4a5-123">Asynchronous Operation</span></span>](asynchronous-operation.md)
-   [<span data-ttu-id="bf4a5-124">Gestione dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="bf4a5-124">Handling Authentication</span></span>](handling-authentication.md)
-   [<span data-ttu-id="bf4a5-125">Gestione di localizzatori di risorse uniformi</span><span class="sxs-lookup"><span data-stu-id="bf4a5-125">Handling Uniform Resource Locators</span></span>](handling-uniform-resource-locators.md)
-   [<span data-ttu-id="bf4a5-126">\_Linee guida sulla sicurezza</span><span class="sxs-lookup"><span data-stu-id="bf4a5-126">Security\_Guideline</span></span>](security-guidelines.md)

## <a name="internet-protocols"></a><span data-ttu-id="bf4a5-127">Protocolli Internet</span><span class="sxs-lookup"><span data-stu-id="bf4a5-127">Internet Protocols</span></span>

<span data-ttu-id="bf4a5-128">I due protocolli Internet primari sono FTP e HTTP.</span><span class="sxs-lookup"><span data-stu-id="bf4a5-128">The two primary Internet protocols are FTP and HTTP.</span></span> <span data-ttu-id="bf4a5-129">Per ulteriori informazioni su questi protocolli, vedere i documenti RFC (Request for Comments) per FTP e HTTP:</span><span class="sxs-lookup"><span data-stu-id="bf4a5-129">For more information about these protocols, see the Request For Comments (RFC) documents for FTP and HTTP:</span></span>

-   <span data-ttu-id="bf4a5-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.</span><span class="sxs-lookup"><span data-stu-id="bf4a5-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.</span></span>
-   <span data-ttu-id="bf4a5-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol-HTTP/1.0*.</span><span class="sxs-lookup"><span data-stu-id="bf4a5-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol - HTTP/1.0*.</span></span>
-   <span data-ttu-id="bf4a5-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol-HTTP/1.1*.</span><span class="sxs-lookup"><span data-stu-id="bf4a5-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol - HTTP/1.1*.</span></span>

> [!NOTE]  
> <span data-ttu-id="bf4a5-133">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi.</span><span class="sxs-lookup"><span data-stu-id="bf4a5-133">(These resources may not be available in some languages and countries.)</span></span>

<span data-ttu-id="bf4a5-134">**Windows XP e Windows Server 2003 R2 e versioni precedenti:** È stato inoltre supportato il protocollo gopher.</span><span class="sxs-lookup"><span data-stu-id="bf4a5-134">**Windows XP and Windows Server 2003 R2 and earlier:** The Gopher protocol was also supported.</span></span> <span data-ttu-id="bf4a5-135">Vedere [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *il protocollo Internet Gopher*.</span><span class="sxs-lookup"><span data-stu-id="bf4a5-135">See [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *The Internet Gopher Protocol*.</span></span>
