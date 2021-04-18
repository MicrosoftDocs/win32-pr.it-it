---
title: Registrazione degli errori in HTTP Server API
description: Alcuni tipi di errori vengono gestiti dall'API del server HTTP anziché essere passati di nuovo a un'applicazione per la gestione, perché la frequenza di tali errori potrebbe altrimenti comportare un registro eventi o un gestore dell'applicazione.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API del server HTTP, registrazione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988d87a65c914625623c3f55d33a7f8cc9a4f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297897"
---
# <a name="error-logging-in-the-http-server-api"></a><span data-ttu-id="7fd28-104">Registrazione degli errori in HTTP Server API</span><span class="sxs-lookup"><span data-stu-id="7fd28-104">Error Logging in the HTTP Server API</span></span>

<span data-ttu-id="7fd28-105">Alcuni tipi di errori vengono gestiti dall'API del server HTTP anziché essere passati di nuovo a un'applicazione per la gestione, perché la frequenza di tali errori potrebbe altrimenti comportare un registro eventi o un gestore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7fd28-105">Some kinds of errors are handled by the HTTP Server API rather than being passed back to an application for handling, because the frequency of such errors could otherwise flood an event log or application handler.</span></span>

<span data-ttu-id="7fd28-106">I tre argomenti seguenti descrivono i diversi aspetti della registrazione degli errori dell'API del server HTTP:</span><span class="sxs-lookup"><span data-stu-id="7fd28-106">The following three topics describe the different aspects of the HTTP Server API error logging:</span></span>

-   <span data-ttu-id="7fd28-107">[Configurazione](configuring-http-server-api-error-logging.md) di Le impostazioni del registro di sistema controllano se l'API del server HTTP registra gli errori, le dimensioni massime consentite dei file di log e i file di log salvati.</span><span class="sxs-lookup"><span data-stu-id="7fd28-107">[Configuration](configuring-http-server-api-error-logging.md) Registry settings control whether the HTTP Server API logs errors, the maximum allowable size of log files, and where log files are saved.</span></span>
-   <span data-ttu-id="7fd28-108">[Formato del file di log](format-of-the-http-server-api-error-logs.md) L'API server HTTP crea file di log conformi alle convenzioni dei file di log di World Wide Web Consortium (W3C) e può essere analizzato utilizzando gli strumenti standard.</span><span class="sxs-lookup"><span data-stu-id="7fd28-108">[Log File Format](format-of-the-http-server-api-error-logs.md) The HTTP Server API creates log files that comply with the World Wide Web Consortium (W3C) log file conventions, and can be parsed by using standard tools.</span></span> <span data-ttu-id="7fd28-109">Tuttavia, a differenza dei file di log W3C, i file di log dell'API del server HTTP non contengono i nomi delle colonne.</span><span class="sxs-lookup"><span data-stu-id="7fd28-109">However, unlike W3C log files, HTTP Server API log files do not contain names of the columns.</span></span>
-   <span data-ttu-id="7fd28-110">[Tipi di errori registrati](types-of-errors-logged-by-the-http-server-api.md) L'API server HTTP registra una serie di errori comuni.</span><span class="sxs-lookup"><span data-stu-id="7fd28-110">[Types of Errors Logged](types-of-errors-logged-by-the-http-server-api.md) The HTTP Server API logs a variety of common errors.</span></span>

 

 




