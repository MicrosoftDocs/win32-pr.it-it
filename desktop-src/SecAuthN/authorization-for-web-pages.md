---
description: Autorizzazione consente di impostare le risorse a cui si ha accesso.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorizzazione per le pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c26e9bc8333d74d18989c5c581cc54054a29ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880178"
---
# <a name="authorization-for-web-pages"></a><span data-ttu-id="96a99-103">Autorizzazione per le pagine Web</span><span class="sxs-lookup"><span data-stu-id="96a99-103">Authorization for web pages</span></span>

<span data-ttu-id="96a99-104">Autorizzazione consente di impostare le risorse a cui si ha accesso.</span><span class="sxs-lookup"><span data-stu-id="96a99-104">Authorization sets what resources you have access to.</span></span>

<span data-ttu-id="96a99-105">**Obiettivo:** Per consentire agli utenti di accedere all'app.</span><span class="sxs-lookup"><span data-stu-id="96a99-105">**Objective:** To allow users access to your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="96a99-106">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="96a99-106">Prerequisites</span></span>

<span data-ttu-id="96a99-107">nessuno</span><span class="sxs-lookup"><span data-stu-id="96a99-107">None</span></span>

<span data-ttu-id="96a99-108">**Tempo necessario per il completamento:** 2 minuti.</span><span class="sxs-lookup"><span data-stu-id="96a99-108">**Time to complete:** 2 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="96a99-109">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="96a99-109">Instructions</span></span>

### <a name="1-authorization"></a><span data-ttu-id="96a99-110">1. autorizzazione</span><span class="sxs-lookup"><span data-stu-id="96a99-110">1. Authorization</span></span>

<span data-ttu-id="96a99-111">Quando l'utente immette le credenziali e fa clic sul pulsante di accesso, viene visualizzata la pagina autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="96a99-111">When the user enters their credentials and clicks the Login button, the permissions page is shown.</span></span> <span data-ttu-id="96a99-112">Questa pagina è ideale per consentire agli utenti di controllare le autorizzazioni granulari per concedere all'app l'accesso ai dati di contoso.</span><span class="sxs-lookup"><span data-stu-id="96a99-112">This page is best at allowing users to control granular permissions in granting the app to access to Contoso’s data.</span></span> ![pagina autorizzazioni di contoso](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a><span data-ttu-id="96a99-114">2. come utilizzare l'esempio</span><span class="sxs-lookup"><span data-stu-id="96a99-114">2. How to use the sample</span></span>

<span data-ttu-id="96a99-115">È necessario conoscere i seguenti file HTML e CSS.</span><span class="sxs-lookup"><span data-stu-id="96a99-115">You need to know about the following HTML and CSS files.</span></span>

1.  <span data-ttu-id="96a99-116">I file HTML seguenti corrispondono alle due pagine del flusso di autorizzazione Web</span><span class="sxs-lookup"><span data-stu-id="96a99-116">The following HTML files correspond to the two pages in the web authorization flow</span></span>
    -   <span data-ttu-id="96a99-117">WebAuthLogin.html-HTML di esempio per la pagina di accesso</span><span class="sxs-lookup"><span data-stu-id="96a99-117">WebAuthLogin.html – sample HTML for the login page</span></span>
    -   <span data-ttu-id="96a99-118">WebAuthPermissions.html-HTML di esempio per la pagina autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="96a99-118">WebAuthPermissions.html – sample HTML for the permissions page</span></span>
2.  <span data-ttu-id="96a99-119">I file CSS contengono gli stili di Windows 8 per facilitare la creazione di una pagina Web dell'app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="96a99-119">The CSS files contain Windows 8 styles to help create a Windows Store app web page.</span></span>
    -   <span data-ttu-id="96a99-120">UI-Light. CSS: è stato derivato dal foglio di stile di base per i controlli di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="96a99-120">ui-light.css – this has been derived from the base style sheet for Windows 8 controls.</span></span>
    -   <span data-ttu-id="96a99-121">UI-WebAuth. CSS: fornisce lo stile incrementale per l'ottimizzazione del layout per le pagine di autenticazione Web.</span><span class="sxs-lookup"><span data-stu-id="96a99-121">ui-webauth.css – this provides incremental styling for optimizing layout for web auth pages.</span></span>
    -   <span data-ttu-id="96a99-122">Theme-Colors. CSS: fornisce lo stile incrementale per l'override dei colori accentati predefiniti dei controlli con il colore del marchio del provider.</span><span class="sxs-lookup"><span data-stu-id="96a99-122">theme-colors.css – this provides the incremental styling to override default accent colors of controls with the provider’s brand color.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="96a99-123">Riepilogo e passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="96a99-123">Summary and next steps</span></span>

<span data-ttu-id="96a99-124">[Esercitazione di riepilogo per l'autenticazione di pagine Web](tutorial-for-authenticating-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="96a99-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="96a99-125">[Procedure consigliate successive per la progettazione di pagine Web di autenticazione](best-practices-for-designing-authentication-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="96a99-125">Next [Best practices for designing authentication web pages](best-practices-for-designing-authentication-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="96a99-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="96a99-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96a99-127">Considerazioni relative allo sviluppo di pagine Web</span><span class="sxs-lookup"><span data-stu-id="96a99-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="96a99-128">App di esempio SDK Web Authentication broker</span><span class="sxs-lookup"><span data-stu-id="96a99-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="96a99-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="96a99-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
