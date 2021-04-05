---
description: L'autenticazione sta dimostrando chi sei.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Autenticazione per le pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7c7bd37334f345ae16074c050b6b06c5fd644f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968142"
---
# <a name="authentication-for-web-pages"></a><span data-ttu-id="51a4d-103">Autenticazione per le pagine Web</span><span class="sxs-lookup"><span data-stu-id="51a4d-103">Authentication for web pages</span></span>

<span data-ttu-id="51a4d-104">L'autenticazione sta dimostrando chi sei.</span><span class="sxs-lookup"><span data-stu-id="51a4d-104">Authentication is proving who you are.</span></span>

<span data-ttu-id="51a4d-105">**Obiettivo:** Per far apparire il broker di autenticazione Web come parte dell'app.</span><span class="sxs-lookup"><span data-stu-id="51a4d-105">**Objective:** To have the web authentication broker appear as part of your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="51a4d-106">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="51a4d-106">Prerequisites</span></span>

<span data-ttu-id="51a4d-107">nessuno</span><span class="sxs-lookup"><span data-stu-id="51a4d-107">None</span></span>

<span data-ttu-id="51a4d-108">**Tempo necessario per il completamento:** 15 minuti.</span><span class="sxs-lookup"><span data-stu-id="51a4d-108">**Time to complete:** 15 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="51a4d-109">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="51a4d-109">Instructions</span></span>

### <a name="1-getting-started"></a><span data-ttu-id="51a4d-110">1. Guida introduttiva</span><span class="sxs-lookup"><span data-stu-id="51a4d-110">1. Getting started</span></span>

<span data-ttu-id="51a4d-111">Avviare il file di installazione per installare un sito Web contoso in Internet Information Services 8 nel computer locale per ospitare i file HTML e CSS di esempio.</span><span class="sxs-lookup"><span data-stu-id="51a4d-111">Launch the setup file to install a Contoso website in Internet Information Services 8 on the local machine to host the sample HTML and CSS files.</span></span>

1.  <span data-ttu-id="51a4d-112">I file HTML e CSS di esempio verranno installati nella directory programmi in Microsoft \\ contoso.</span><span class="sxs-lookup"><span data-stu-id="51a4d-112">Sample HTML and CSS files will be installed to the program files directory under Microsoft\\Contoso.</span></span>
2.  <span data-ttu-id="51a4d-113">Inoltre, un'app di Windows Store "Fabrikam social" verrà disimballata sul desktop.</span><span class="sxs-lookup"><span data-stu-id="51a4d-113">In addition a "Fabrikam Social"Windows Store app will be unpackaged to the desktop.</span></span>

### <a name="2-getting-familiar"></a><span data-ttu-id="51a4d-114">2. acquisire familiarità</span><span class="sxs-lookup"><span data-stu-id="51a4d-114">2. Getting familiar</span></span>

<span data-ttu-id="51a4d-115">Per avere un'idea dell'aspetto delle pagine di esempio nel gestore di autenticazione Web, aprire il file di soluzione di Visual Studio 11 per Fabrikam social Visual Studio 11 nella cartella "Fabrikam social" sul desktop.</span><span class="sxs-lookup"><span data-stu-id="51a4d-115">To get a feel for what the sample pages look like in the Web Authentication Broker, open the Fabrikam Social Visual Studio 11 solution file in the "Fabrikam Social" folder on the desktop.</span></span>

1.  <span data-ttu-id="51a4d-116">Eseguire l'applicazione e fare clic su "Launch" (Avvia) per visualizzare le pagine di esempio nel gestore di autenticazione Web.</span><span class="sxs-lookup"><span data-stu-id="51a4d-116">Run the application and hit "Launch" to bring up the sample pages in the Web Authentication Broker.</span></span>
2.  <span data-ttu-id="51a4d-117">L'app può essere ridimensionata in un lato o attivata condividendo alcuni dati nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="51a4d-117">The app can be resized to one side or activated by sharing some data to the application.</span></span>

### <a name="3-authentication"></a><span data-ttu-id="51a4d-118">3. autenticazione</span><span class="sxs-lookup"><span data-stu-id="51a4d-118">3. Authentication</span></span>

<span data-ttu-id="51a4d-119">Quando l'API di autenticazione Web viene richiamata dall'app sottostante per connettersi al provider, ovvero "contoso social", viene visualizzata la pagina di accesso.</span><span class="sxs-lookup"><span data-stu-id="51a4d-119">When the Web Auth API is invoked by the underlying app to connect to the provider, "Contoso Social", the login page is shown.</span></span> <span data-ttu-id="51a4d-120">Questa pagina è progettata per essere ottimale in un'esperienza di accesso veloce e fluida.</span><span class="sxs-lookup"><span data-stu-id="51a4d-120">This page is designed to be best at a fast and fluid login experience.</span></span> <span data-ttu-id="51a4d-121">Fornisce inoltre punti di ingresso ad altre azioni utente comuni, ad esempio il recupero dei dettagli della password, l'iscrizione a un account e la lettura di istruzioni sulla privacy e i termini e le condizioni completati nel browser.</span><span class="sxs-lookup"><span data-stu-id="51a4d-121">It also provides entry points to some other common user actions such as retrieving password details, signing up for an account, and reading statements on privacy and terms and conditions that are completed in the browser.</span></span> ![pagina di accesso di contoso](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a><span data-ttu-id="51a4d-123">Riepilogo e passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="51a4d-123">Summary and next steps</span></span>

<span data-ttu-id="51a4d-124">[Esercitazione di riepilogo per l'autenticazione di pagine Web](tutorial-for-authenticating-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="51a4d-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="51a4d-125">[Autorizzazione successiva per le pagine Web](authorization-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="51a4d-125">Next [Authorization for web pages](authorization-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="51a4d-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51a4d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51a4d-127">Considerazioni relative allo sviluppo di pagine Web</span><span class="sxs-lookup"><span data-stu-id="51a4d-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="51a4d-128">App di esempio SDK Web Authentication broker</span><span class="sxs-lookup"><span data-stu-id="51a4d-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="51a4d-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="51a4d-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
