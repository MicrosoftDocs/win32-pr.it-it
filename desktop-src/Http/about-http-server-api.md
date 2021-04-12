---
title: Informazioni sull'API server HTTP
description: L'API server HTTP fornisce agli sviluppatori un'interfaccia di basso livello per il lato server della funzionalità HTTP, come definito nella specifica RFC 2616.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- API server HTTP, panoramica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e00fcfe6527b77be32a849f00f62222396f42b5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398655"
---
# <a name="about-http-server-api"></a><span data-ttu-id="668b8-104">Informazioni sull'API server HTTP</span><span class="sxs-lookup"><span data-stu-id="668b8-104">About HTTP Server API</span></span>

<span data-ttu-id="668b8-105">L'API server HTTP fornisce agli sviluppatori un'interfaccia di basso livello per il lato server della funzionalità HTTP, come definito nella [specifica RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="668b8-105">The HTTP Server API provides developers with a low-level interface to the server side of the HTTP functionality as defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="668b8-106">L'API consente a un'applicazione di ricevere richieste HTTP indirizzate agli URL e di inviare risposte HTTP.</span><span class="sxs-lookup"><span data-stu-id="668b8-106">The API enables an application to receive HTTP requests directed to URLs and send HTTP responses.</span></span> <span data-ttu-id="668b8-107">Per l'invio di risposte dinamiche, sono consigliate le interfacce ISAPI o ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="668b8-107">For sending dynamic responses, the ISAPI or ASP.NET interfaces are recommended.</span></span>

<span data-ttu-id="668b8-108">L'API server HTTP consente la coesistenza di più applicazioni in un sistema, la condivisione della stessa porta TCP (ad esempio, la porta 80 per HTTP o la porta 443 per HTTPS) e la conservazione di parti diverse dello spazio dei nomi URL.</span><span class="sxs-lookup"><span data-stu-id="668b8-108">The HTTP Server API enables multiple applications to coexist on a system, sharing the same TCP port (for example, port 80 for HTTP or port 443 for HTTPS) and serving different parts of the URL namespace.</span></span>

<span data-ttu-id="668b8-109">L'API server HTTP richiede la conoscenza del linguaggio di programmazione C e una certa familiarità con la programmazione dell'API Windows.</span><span class="sxs-lookup"><span data-stu-id="668b8-109">The HTTP Server API requires knowledge of the C programming language and a familiarity with Windows API programming.</span></span> <span data-ttu-id="668b8-110">Le applicazioni che non richiedono l'accesso di basso livello a HTTP devono usare l'ISAPI IIS o le classi .NET Framework per le soluzioni basate su HTTP.</span><span class="sxs-lookup"><span data-stu-id="668b8-110">Applications that do not require low-level access to HTTP should use the IIS ISAPI or the .NET Framework classes for HTTP-based solutions.</span></span>

 

 




