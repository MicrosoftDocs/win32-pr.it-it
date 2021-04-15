---
description: Questa sezione descrive come usare sia l'API C/C++ per i servizi HTTP di Microsoft Windows (WinHTTP) che l'interfaccia COM esposta dall'oggetto WinHttpRequest.
ms.assetid: 16178bb8-5e95-46a5-825a-880edc402445
title: Uso di WinHTTP
ms.topic: article
ms.date: 07/22/2020
ms.openlocfilehash: cda0a7772b88dfd9c03675c522f4b7504ea00b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484997"
---
# <a name="using-winhttp"></a><span data-ttu-id="49bcd-103">Uso di WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-103">Using WinHTTP</span></span>

<span data-ttu-id="49bcd-104">Questa sezione descrive come usare sia l'API C/C++ per i servizi HTTP di Microsoft Windows (WinHTTP) che l'interfaccia COM esposta dall'oggetto **WinHttpRequest** .</span><span class="sxs-lookup"><span data-stu-id="49bcd-104">This section describes how to use both the C/C++ API for Microsoft Windows HTTP Services (WinHTTP) and the COM interface exposed by the **WinHttpRequest** Object.</span></span> <span data-ttu-id="49bcd-105">Vedere [scelta di un'interfaccia WinHTTP](choosing-a-winhttp-interface.md) per un confronto di queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="49bcd-105">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span> <span data-ttu-id="49bcd-106">Viene inoltre descritto come utilizzare gli strumenti di amministrazione inclusi in WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="49bcd-106">It also describes how to use the administrative tools included with WinHTTP.</span></span>

## <a name="how-to-topics"></a><span data-ttu-id="49bcd-107">Procedure</span><span class="sxs-lookup"><span data-stu-id="49bcd-107">How-To Topics</span></span>

[<span data-ttu-id="49bcd-108">Uso dell'API WinHTTP C/C++</span><span class="sxs-lookup"><span data-stu-id="49bcd-108">Using the WinHTTP C/C++ API</span></span>](using-the-winhttp-c-c---api.md)

-   [<span data-ttu-id="49bcd-109">Cenni preliminari sulle sessioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-109">WinHTTP Sessions Overview</span></span>](winhttp-sessions-overview.md)
-   [<span data-ttu-id="49bcd-110">Handle HINTERNET in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-110">HINTERNET Handles in WinHTTP</span></span>](hinternet-handles-in-winhttp.md)
-   [<span data-ttu-id="49bcd-111">Uniform Resource Locator (URL) in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-111">Uniform Resource Locators (URLs) in WinHTTP</span></span>](uniform-resource-locators--urls--in-winhttp.md)
-   [<span data-ttu-id="49bcd-112">Autenticazione in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-112">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
-   [<span data-ttu-id="49bcd-113">Autenticazione Passport in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-113">Passport Authentication in WinHTTP</span></span>](passport-authentication-in-winhttp.md)
-   [<span data-ttu-id="49bcd-114">SSL in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-114">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
-   [<span data-ttu-id="49bcd-115">Uso di WinHTTP come assembly affiancato</span><span class="sxs-lookup"><span data-stu-id="49bcd-115">Using WinHTTP as a Side-by-side Assembly</span></span>](using-winhttp-as-a-side-by-side-assembly.md)
-   [<span data-ttu-id="49bcd-116">Gestione dei cookie in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-116">Cookie Handling in WinHTTP</span></span>](cookie-handling-in-winhttp.md)
-   [<span data-ttu-id="49bcd-117">Gestione degli errori in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-117">Error Handling in WinHTTP</span></span>](error-handling-in-winhttp.md)
-   [<span data-ttu-id="49bcd-118">Supporto del proxy AutoProxy WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-118">WinHTTP AutoProxy Support</span></span>](winhttp-autoproxy-support.md)

[<span data-ttu-id="49bcd-119">Utilizzo dell'oggetto COM WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="49bcd-119">Using the WinHttpRequest COM Object</span></span>](using-the-winhttprequest-com-object.md)

-   [<span data-ttu-id="49bcd-120">Recupero di dati tramite script</span><span class="sxs-lookup"><span data-stu-id="49bcd-120">Retrieving Data Using Script</span></span>](retrieving-data-using-script.md)
-   [<span data-ttu-id="49bcd-121">Autenticazione tramite script</span><span class="sxs-lookup"><span data-stu-id="49bcd-121">Authentication Using Script</span></span>](authentication-using-script.md)

[<span data-ttu-id="49bcd-122">Uso degli strumenti WinHTTP</span><span class="sxs-lookup"><span data-stu-id="49bcd-122">Using WinHTTP Tools</span></span>](using-winhttp-tools.md)

-   [<span data-ttu-id="49bcd-123">WinHttpCfg.exe, uno strumento di configurazione del certificato</span><span class="sxs-lookup"><span data-stu-id="49bcd-123">WinHttpCfg.exe, a Certificate Configuration Tool</span></span>](winhttpcertcfg-exe--a-certificate-configuration-tool.md)
-   [<span data-ttu-id="49bcd-124">ProxyCfg.exe, uno strumento di configurazione proxy</span><span class="sxs-lookup"><span data-stu-id="49bcd-124">ProxyCfg.exe, a Proxy Configuration Tool</span></span>](proxycfg-exe--a-proxy-configuration-tool.md)
-   [<span data-ttu-id="49bcd-125">WinHttpTraceCfg, uno strumento di configurazione della traccia</span><span class="sxs-lookup"><span data-stu-id="49bcd-125">WinHttpTraceCfg, a Trace Configuration Tool</span></span>](winhttptracecfg-exe--a-trace-configuration-tool.md)

 

 



