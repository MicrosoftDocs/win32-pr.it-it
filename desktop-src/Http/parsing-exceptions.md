---
title: Analisi delle eccezioni
description: L'API server HTTP fornisce le chiavi del registro di sistema per supportare l'analisi delle eccezioni alla specifica HTTP/1.1 per la compatibilità con le versioni precedenti.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Analisi delle eccezioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa071f141539a159d09f6a53f2e78a81bf75327b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955578"
---
# <a name="parsing-exceptions"></a><span data-ttu-id="a8978-104">Analisi delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="a8978-104">Parsing Exceptions</span></span>

<span data-ttu-id="a8978-105">L'API server HTTP fornisce le chiavi del registro di sistema per supportare l'analisi delle eccezioni alla specifica HTTP/1.1 per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="a8978-105">HTTP Server API provides registry keys to support parsing exceptions to the HTTP/1.1 specification for backward compatibility.</span></span> <span data-ttu-id="a8978-106">Queste eccezioni non sono abilitate per impostazione predefinita e devono essere abilitate solo per caso, quando il server riscontra problemi di compatibilità con i client HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8978-106">These exceptions are not enabled by default and should be enabled only on a case-by-case basis, when the server experiences compatibility issues with HTTP clients.</span></span> <span data-ttu-id="a8978-107">Questi valori vengono creati nel seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="a8978-107">These values are created under the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

<span data-ttu-id="a8978-108">Nella tabella seguente sono elencate le chiavi del registro di sistema fornite per supportare le eccezioni elencate.</span><span class="sxs-lookup"><span data-stu-id="a8978-108">The following table lists registry keys provided to support the exceptions listed.</span></span> <span data-ttu-id="a8978-109">Per abilitare un'eccezione, impostare il valore di chiave corrispondente su 1 e riavviare il servizio HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8978-109">To enable an exception set the corresponding key value to 1 and restart the HTTP service.</span></span>



| <span data-ttu-id="a8978-110">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="a8978-110">Key name</span></span>                              | <span data-ttu-id="a8978-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8978-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8978-112">AllowWeakHeaderNameSyntax (DWORD)</span><span class="sxs-lookup"><span data-stu-id="a8978-112">AllowWeakHeaderNameSyntax (DWORD)</span></span>     | <span data-ttu-id="a8978-113">Consente al parser HTTP di accettare i nomi di intestazione con caratteri separatori, ad esempio '?'.</span><span class="sxs-lookup"><span data-stu-id="a8978-113">Allows the HTTP parser to accept header names with separator characters such as '?'.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a8978-114">AllowWeakHeaderValueSyntax (DWORD)</span><span class="sxs-lookup"><span data-stu-id="a8978-114">AllowWeakHeaderValueSyntax (DWORD)</span></span>    | <span data-ttu-id="a8978-115">Consente al parser HTTP di accettare i valori di intestazione con caratteri di controllo non elaborati (senza escape).</span><span class="sxs-lookup"><span data-stu-id="a8978-115">Allows the HTTP parser to accept header values with raw (unescaped) control characters in it.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a8978-116">AllowCaseInsensitiveVerbs (DWORD)</span><span class="sxs-lookup"><span data-stu-id="a8978-116">AllowCaseInsensitiveVerbs (DWORD)</span></span>     | <span data-ttu-id="a8978-117">Consente al parser HTTP di accettare verbi o metodi HTTP minuscoli come "Get".</span><span class="sxs-lookup"><span data-stu-id="a8978-117">Allows the HTTP parser to accept lowercase HTTP methods/verbs such as "get".</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a8978-118">AllowUnEscapedRestrictedChars (DWORD)</span><span class="sxs-lookup"><span data-stu-id="a8978-118">AllowUnEscapedRestrictedChars (DWORD)</span></span> | <span data-ttu-id="a8978-119">Consente al parser HTTP di accettare i caratteri di controllo in absPath e le stringhe di query dell'URL.</span><span class="sxs-lookup"><span data-stu-id="a8978-119">Allows the HTTP parser to accept control characters in abspath and query strings of the URL.</span></span> <span data-ttu-id="a8978-120">Nel caso di un URL assoluto, i caratteri di controllo non saranno consentiti nel nome host.</span><span class="sxs-lookup"><span data-stu-id="a8978-120">In case of an absolute URL, control characters will not be allowed in the hostname.</span></span> <span data-ttu-id="a8978-121">Tutte le versioni degli URL, ovvero UTF8, DBCS e ANSI, consentiranno caratteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="a8978-121">All flavors of URLs, namely UTF8, DBCS and ANSI, will allow control characters.</span></span> <span data-ttu-id="a8978-122">Verranno consentiti tutti i caratteri di controllo ASCII tranne NUL (0x00), LF (0x0A), CR (0x0D) e la scheda orizzontale (0x09).</span><span class="sxs-lookup"><span data-stu-id="a8978-122">All ASCII control characters except NUL (0x00), LF (0x0a), CR (0x0d) and Horizontal Tab(0x09) will be allowed.</span></span> |



 

 

 




