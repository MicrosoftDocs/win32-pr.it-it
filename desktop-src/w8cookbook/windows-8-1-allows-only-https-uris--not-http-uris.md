---
title: URI in Windows 8.1
description: Windows 8.1 consente solo URI https, non URI http
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399565"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a><span data-ttu-id="63d4c-103">Windows 8.1 consente solo URI https, non URI http</span><span class="sxs-lookup"><span data-stu-id="63d4c-103">Windows 8.1 allows only https URIs, not http URIs</span></span>

## <a name="platforms"></a><span data-ttu-id="63d4c-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="63d4c-104">Platforms</span></span>

<dl> <span data-ttu-id="63d4c-105">Client-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="63d4c-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="63d4c-106">Server-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="63d4c-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="63d4c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63d4c-107">Description</span></span>

<span data-ttu-id="63d4c-108">Mentre le app compilate per Windows 8 possono includere URI http e HTTPS negli URI del contenuto dell'applicazione, le app create per Windows 8.1 possono includere solo URI https.</span><span class="sxs-lookup"><span data-stu-id="63d4c-108">While apps built for Windows 8 can include http and https URIs in their application content URIs, apps built for Windows 8.1 may include only https URIs.</span></span>

<span data-ttu-id="63d4c-109">L'unica eccezione è per ContentUriRules dinamici specificati nel file di AppxManifest.xml dell'app.</span><span class="sxs-lookup"><span data-stu-id="63d4c-109">The only exception is for dynamic ContentUriRules that are specified in the app’s AppxManifest.xml file.</span></span> <span data-ttu-id="63d4c-110">Con ContentUriRules dinamici, le app possono accedere ad altri domini o risorse di rete forniti dall'amministratore, ad esempio gli URI Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="63d4c-110">With dynamic ContentUriRules, apps can access additional domains or network resources that are provided by the admin, such as Group Policy URIs.</span></span> <span data-ttu-id="63d4c-111">Tuttavia, i ContentUriRules dinamici sono disponibili solo per le app di Windows Store se soddisfano le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="63d4c-111">However, dynamic ContentUriRules are only available to Windows Store apps if they meet these conditions:</span></span>

-   <span data-ttu-id="63d4c-112">Il Criteri di gruppo è abilitato</span><span class="sxs-lookup"><span data-stu-id="63d4c-112">The Group Policy is enabled</span></span>
-   <span data-ttu-id="63d4c-113">Il pacchetto ha specificato la funzionalità enterpriseAuthentication</span><span class="sxs-lookup"><span data-stu-id="63d4c-113">The package has specified the enterpriseAuthentication capability</span></span>
-   <span data-ttu-id="63d4c-114">Il OSMaxVersionTested del pacchetto è Windows 8.1 o superiore</span><span class="sxs-lookup"><span data-stu-id="63d4c-114">The package’s OSMaxVersionTested is Windows 8.1 or greater</span></span>

<span data-ttu-id="63d4c-115">Le nuove limitazioni in Windows 8.1 fanno parte delle restrizioni di sicurezza avanzate per proteggere ulteriormente la piattaforma.</span><span class="sxs-lookup"><span data-stu-id="63d4c-115">The new restrictions in Windows 8.1 are part of enhanced security restrictions to further protect the platform.</span></span>

## <a name="manifestations"></a><span data-ttu-id="63d4c-116">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="63d4c-116">Manifestations</span></span>

<span data-ttu-id="63d4c-117">Quando si esegue un'app compilata per Windows 8 in Windows 8.1, è consentito l'uso degli URI http nella [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) .</span><span class="sxs-lookup"><span data-stu-id="63d4c-117">When running an app built for Windows 8 on Windows 8.1, the use of http URIs in the [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) is allowed.</span></span>

## <a name="mitigations"></a><span data-ttu-id="63d4c-118">Soluzioni di prevenzione</span><span class="sxs-lookup"><span data-stu-id="63d4c-118">Mitigations</span></span>

<span data-ttu-id="63d4c-119">È consigliabile che gli sviluppatori WWA passino da [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) al controllo [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-ms-webview>).</span><span class="sxs-lookup"><span data-stu-id="63d4c-119">We recommend that WWA developers switch from [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) to the [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) control (<x-ms-webview>).</span></span> <span data-ttu-id="63d4c-120">Tuttavia, se è necessario il supporto per AppCache, IndexedDB, la georilevazione o l'accesso agli Appunti a livello di codice, sarà necessario continuare a usare</span><span class="sxs-lookup"><span data-stu-id="63d4c-120">However, if you need support for AppCache, IndexedDB, geolocation, or programmatic clipboard access, you will need to continue using</span></span> <iframe> <span data-ttu-id="63d4c-121">per Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="63d4c-121">for Windows 8.1.</span></span>

<span data-ttu-id="63d4c-122">Utilizzo continuo di</span><span class="sxs-lookup"><span data-stu-id="63d4c-122">Continued usage of</span></span> <iframe> <span data-ttu-id="63d4c-123">per il contenuto remoto è necessaria una nuova voce in ApplicationContentUriRules per l'app.</span><span class="sxs-lookup"><span data-stu-id="63d4c-123">for remote content will require a new entry in the ApplicationContentUriRules for the app.</span></span> <span data-ttu-id="63d4c-124">Le app con WebView richiedono nuove voci in ApplicationContentUriRules se il contenuto Web deve richiamare Window. External. Notify per la generazione di un evento [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="63d4c-124">Apps with WebView require new entries in the ApplicationContentUriRules if the web content needs to invoke window.external.notify for generating a [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) event.</span></span> <span data-ttu-id="63d4c-125">Se non si dispone di Visual Studio, è possibile aggiornare il manifesto dell'applicazione aggiungendo il codice XML seguente, inclusi i caratteri jolly per i sottodomini, ad esempio https:// \* . Microsoft.com:</span><span class="sxs-lookup"><span data-stu-id="63d4c-125">If you do not have Visual Studio, you can update the app manifest by adding the following XML, including wildcards for subdomains (e.g. https://\*.microsoft.com):</span></span>


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a><span data-ttu-id="63d4c-126">Risorse</span><span class="sxs-lookup"><span data-stu-id="63d4c-126">Resources</span></span>

-   [<span data-ttu-id="63d4c-127">ApplicationContentUriRules</span><span class="sxs-lookup"><span data-stu-id="63d4c-127">ApplicationContentUriRules</span></span>](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<span data-ttu-id="63d4c-128"><iframe>\| <iframe> oggetto elemento</span><span class="sxs-lookup"><span data-stu-id="63d4c-128"><iframe> element \| <iframe> object</span></span>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [<span data-ttu-id="63d4c-129">Classe WebView</span><span class="sxs-lookup"><span data-stu-id="63d4c-129">Webview class</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [<span data-ttu-id="63d4c-130">Evento WebView. ScriptNotify</span><span class="sxs-lookup"><span data-stu-id="63d4c-130">WebView.ScriptNotify event</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 