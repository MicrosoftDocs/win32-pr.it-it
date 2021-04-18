---
description: In questa esercitazione vengono evidenziati i diversi aspetti che gli sviluppatori Web devono considerare durante la progettazione di pagine per il flusso di autorizzazione Web per Windows 8. Questa sezione illustra un flusso di autorizzazione a due pagine.
ms.assetid: A26E09EF-6C7A-4F75-89A7-76086F63F3B1
title: Esercitazione per l'autenticazione di pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6fc6482c5e6dfaf89a9fc9732783f5f088b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315857"
---
# <a name="tutorial-for-authenticating-web-pages"></a><span data-ttu-id="c2c97-104">Esercitazione per l'autenticazione di pagine Web</span><span class="sxs-lookup"><span data-stu-id="c2c97-104">Tutorial for authenticating web pages</span></span>

<span data-ttu-id="c2c97-105">In questa esercitazione vengono evidenziati i diversi aspetti che gli sviluppatori Web devono considerare durante la progettazione di pagine per il flusso di autorizzazione Web per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c2c97-105">This tutorial highlights the different aspects that web developers should care about when designing pages for the web authorization flow for Windows 8.</span></span> <span data-ttu-id="c2c97-106">Questa sezione illustra un flusso di autorizzazione a due pagine.</span><span class="sxs-lookup"><span data-stu-id="c2c97-106">This section This sample demonstrates a two-page authorization flow.</span></span>

<span data-ttu-id="c2c97-107">**Obiettivo:** L'obiettivo dell'esempio non è quello di essere prescrittivo sul layout o sulla progettazione visiva che ciascun provider avrà certamente un punto di vista univoco, ma per richiamare alcune aree vale la pena investire in per avere un'esperienza di progettazione di Microsoft di prima classe per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c2c97-107">**Objective:** The goal of the sample is not to be prescriptive about the layout or visual design that each provider will certainly have a unique point of view on, but to call out a few areas worth investing in to have a first-class Microsoft design style experience for Windows 8.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c2c97-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c2c97-108">Prerequisites</span></span>

<span data-ttu-id="c2c97-109">Per usare le API del broker di autenticazione Web, è necessario quanto segue:</span><span class="sxs-lookup"><span data-stu-id="c2c97-109">In order to use web authentication broker APIs, you need:</span></span>

-   <span data-ttu-id="c2c97-110">Windows 8 (solo x86 o amd64)</span><span class="sxs-lookup"><span data-stu-id="c2c97-110">Windows 8 (x86 or amd64 only)</span></span>
-   <span data-ttu-id="c2c97-111">Microsoft Internet Information Services (IIS) deve essere installato dal pannello di controllo in "programmi e funzionalità" e utilizzando l'opzione "attivazione o disattivazione delle funzionalità Windows".</span><span class="sxs-lookup"><span data-stu-id="c2c97-111">Microsoft Internet Information Services (IIS) should be installed from the Control Panel under "Programs and Features" and using the "Turn Windows features on or off" option.</span></span>

<span data-ttu-id="c2c97-112">**Tempo totale per il completamento:** 2 minuti.</span><span class="sxs-lookup"><span data-stu-id="c2c97-112">**Total time to complete:** 2 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="c2c97-113">Dove proseguire</span><span class="sxs-lookup"><span data-stu-id="c2c97-113">Where to go from here</span></span>

<span data-ttu-id="c2c97-114">[Autenticazione successiva per le pagine Web](authentication-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="c2c97-114">Next [Authentication for web pages](authentication-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2c97-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2c97-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2c97-116">Considerazioni relative allo sviluppo di pagine Web</span><span class="sxs-lookup"><span data-stu-id="c2c97-116">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="c2c97-117">App di esempio SDK Web Authentication broker</span><span class="sxs-lookup"><span data-stu-id="c2c97-117">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="c2c97-118">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="c2c97-118">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
