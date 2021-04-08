---
title: Chiamata di WDS da pagine Web
description: È possibile chiamare Microsoft Windows Desktop Search (WDS) da qualsiasi pagina Web che si crea o si gestisce utilizzando l'oggetto browser helper (BHO) e Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "104046416"
---
# <a name="calling-wds-from-web-pages"></a><span data-ttu-id="66baf-103">Chiamata di WDS da pagine Web</span><span class="sxs-lookup"><span data-stu-id="66baf-103">Calling WDS from Web Pages</span></span>

> [!NOTE]
> <span data-ttu-id="66baf-104">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="66baf-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="66baf-105">Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="66baf-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="66baf-106">È possibile chiamare Microsoft Windows Desktop Search (WDS) da qualsiasi pagina Web che si crea o si gestisce utilizzando l'oggetto browser helper (BHO) e Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="66baf-106">You can call Microsoft Windows Desktop Search (WDS) from any webpage you create or maintain using the Browser Helper Object (BHO) and Windows Internet Explorer.</span></span> <span data-ttu-id="66baf-107">È possibile vedere come funziona nella pagina Web MSN.</span><span class="sxs-lookup"><span data-stu-id="66baf-107">You can see how this works on the MSN webpage.</span></span> <span data-ttu-id="66baf-108">Sopra la casella di ricerca in https://www.msn.com sono disponibili diversi tipi di ricerca: Web, News, images, desktop, Encarta e local.</span><span class="sxs-lookup"><span data-stu-id="66baf-108">Above the search box on https://www.msn.com are several search types: Web, News, Images, Desktop, Encarta, and Local.</span></span> <span data-ttu-id="66baf-109">Se si fa clic su desktop, i parametri di ricerca vengono passati a Windows Desktop Search, che cerca nel catalogo e Visualizza i risultati nell'interfaccia utente di WDS.</span><span class="sxs-lookup"><span data-stu-id="66baf-109">If you click Desktop, the search parameters are passed to Windows Desktop Search, which searches the catalog and displays results in the WDS user interface.</span></span> <span data-ttu-id="66baf-110">Per consentire agli utenti di avviare una ricerca desktop dalle pagine Web, WDSBHO deve essere installato e abilitato nei sistemi, le pagine Web devono essere registrate con WDS come URL consentito ed è necessario creare un collegamento per passare la query utente-inserisce a WDS.</span><span class="sxs-lookup"><span data-stu-id="66baf-110">For users to start a desktop search from your webpage(s), the WDSBHO must be installed and enabled on their systems, your webpage(s) must be registered with WDS as an allowed URL, and you must create a link to pass the user-enetered query to WDS.</span></span>

## <a name="enabling-the-wds-browser-help-object"></a><span data-ttu-id="66baf-111">Abilitazione dell'oggetto guida del browser WDS</span><span class="sxs-lookup"><span data-stu-id="66baf-111">Enabling the WDS Browser Help Object</span></span>

<span data-ttu-id="66baf-112">Per impostazione predefinita, la funzionalità BHO viene installata e abilitata in Internet Explorer quando si installa WDS, ma è possibile verificare facilmente che non sia stata disabilitata o disinstallata.</span><span class="sxs-lookup"><span data-stu-id="66baf-112">The BHO is installed and enabled within Internet Explorer by default when you install WDS, but you can easily verify that it hasn't been disabled or uninstalled.</span></span> <span data-ttu-id="66baf-113">Nel sistema di un utente aprire Internet Explorer, scegliere **Opzioni Internet** dal menu **strumenti** , fare clic sulla scheda **programmi** e quindi fare clic su **Gestisci componenti** aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="66baf-113">On a user's system, open Internet Explorer , select **Internet Options** from the **Tools** menu, click the **Programs** tab, and then click **Manage Add-Ons**.</span></span> <span data-ttu-id="66baf-114">Nell'elenco dei componenti aggiuntivi, cercare la classe dsWebAllowBHO e verificare che sia abilitata.</span><span class="sxs-lookup"><span data-stu-id="66baf-114">In your list of add-ons, look for the dsWebAllowBHO Class and make sure it is enabled.</span></span> <span data-ttu-id="66baf-115">Quando il BHO è disabilitato, WDS continuerà a funzionare normalmente. Tuttavia, non sarà possibile eseguire ricerche sul desktop da una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="66baf-115">When the BHO is disabled, WDS will continue to work normally; however, you will not be able to search the desktop from a webpage.</span></span>

<span data-ttu-id="66baf-116">Entrambe le opzioni seguenti per consentire a una ricerca desktop eseguiranno la ricerca localmente con l'applicazione di ricerca registrata.</span><span class="sxs-lookup"><span data-stu-id="66baf-116">Both of the following options for allowing a desktop search will execute the search locally with the registered search application.</span></span>

## <a name="registering-web-page-urls"></a><span data-ttu-id="66baf-117">Registrazione degli URL della pagina Web</span><span class="sxs-lookup"><span data-stu-id="66baf-117">Registering Web Page URLs</span></span>

<span data-ttu-id="66baf-118">Il registro di sistema include un elenco di URL di dominio "consentiti" da cui è possibile chiamare WDS.</span><span class="sxs-lookup"><span data-stu-id="66baf-118">The Registry includes a list of "allowed" domain URLs from which WDS can be called.</span></span> <span data-ttu-id="66baf-119">Per includere le pagine Web, è necessario elencare gli URL di dominio come REG \_ SZ nel registro di sistema come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="66baf-119">To include your webpage(s), you need to list your domain URL(s) as REG\_SZ in the Registry as follows:</span></span>

<span data-ttu-id="66baf-120">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **consentito**\\*<number>* = <domainURL></span><span class="sxs-lookup"><span data-stu-id="66baf-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows Desktop Search**\\**DSW**\\**Allowed**\\*<number>* = <domainURL></span></span>

<span data-ttu-id="66baf-121">Dove **<number>** è numerato in sequenza e **<domainURL>** è l'URL della pagina Web da cui si desidera consentire la ricerca di WDS.</span><span class="sxs-lookup"><span data-stu-id="66baf-121">Where **<number>** is sequentially numbered, and **<domainURL>** is the URL of the Web Page you want to allow WDS searches from.</span></span> <span data-ttu-id="66baf-122">Questa stringa URL può includere l'asterisco con caratteri jolly \* all'inizio o alla fine dell'URL.</span><span class="sxs-lookup"><span data-stu-id="66baf-122">This URL string can include the wildcard asterisk \* at the beginning or end of the URL.</span></span> <span data-ttu-id="66baf-123">Ad esempio, se la stringa è " \* . mydomain.com", è possibile avviare una ricerca WDS sia da https://www.mydomain.com che da https://mydomain.com .</span><span class="sxs-lookup"><span data-stu-id="66baf-123">For example, if the string is "\*.mydomain.com", then you can start a WDS search from both https://www.mydomain.com and https://mydomain.com.</span></span>

## <a name="enabling-desktop-search-by-url"></a><span data-ttu-id="66baf-124">Abilitazione della ricerca desktop per URL</span><span class="sxs-lookup"><span data-stu-id="66baf-124">Enabling Desktop Search by URL</span></span>

<span data-ttu-id="66baf-125">Un'altra opzione che non richiede l'accesso al registro di sistema consiste nell'usare l'URL seguente nelle pagine Web:</span><span class="sxs-lookup"><span data-stu-id="66baf-125">Another option that does not require access to the Registry is to use the following URL on your webpage(s):</span></span>

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

<span data-ttu-id="66baf-126">dove **query** è la stringa codificata in URL su cui l'utente esegue la ricerca, inclusi eventuali termini della [sintassi di query avanzati](-search-2x-wds-aqsreference.md) .</span><span class="sxs-lookup"><span data-stu-id="66baf-126">where **QUERY** is the URL-encoded string the user is searching on, including any [Advanced Query Syntax](-search-2x-wds-aqsreference.md) terms.</span></span>

 

 




