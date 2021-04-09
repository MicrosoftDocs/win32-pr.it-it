---
title: Effettuare il provisioning di un profilo Wi-Fi tramite un sito Web
description: Consente agli utenti di scaricare un profilo da un sito Web ed eseguirne il provisioning.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963430"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a><span data-ttu-id="2a932-103">Effettuare il provisioning di un profilo Wi-Fi tramite un sito Web</span><span class="sxs-lookup"><span data-stu-id="2a932-103">Provision a Wi-Fi profile via a website</span></span>

<span data-ttu-id="2a932-104">Il flusso di lavoro descritto in questo argomento è stato introdotto in Windows 10, versione 2004.</span><span class="sxs-lookup"><span data-stu-id="2a932-104">The workflow described in this topic was introduced in Windows 10, version 2004.</span></span> <span data-ttu-id="2a932-105">In questo argomento viene illustrato come configurare un sito Web in modo che un utente possa eseguire il provisioning di un profilo per una rete Passpoint (o per una rete normale) prima di trasferirsi nell'intervallo dei corrispondenti punti di accesso Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="2a932-105">This topic shows how to configure a website so that a user can provision a profile for a Passpoint network (or for a normal network) prior to moving into range of the corresponding Wi-Fi access points.</span></span> <span data-ttu-id="2a932-106">Uno scenario di esempio è quello di un utente che può pianificare di visitare un aeroporto o una conferenza per la prima volta e vuole prepararsi in anticipo scaricando ed effettuando il provisioning di un profilo a casa.</span><span class="sxs-lookup"><span data-stu-id="2a932-106">An example scenario is that of a user who might be planning to visit an airport or a conference for the first time, and they want to prepare in advance by downloading and provisioning a profile at home.</span></span>

<span data-ttu-id="2a932-107">Gli sviluppatori abilitano il flusso di lavoro fornendo un profilo XML e configurando un sito Web.</span><span class="sxs-lookup"><span data-stu-id="2a932-107">As a developer, you enable the workflow by providing an XML profile, and configuring a website.</span></span> <span data-ttu-id="2a932-108">Gli utenti possono quindi effettuare il provisioning di un profilo di Wi-Fi eseguendone il download dal sito Web tramite un Web browser.</span><span class="sxs-lookup"><span data-stu-id="2a932-108">Your users can then provision a Wi-Fi profile by downloading it from your website via a web browser.</span></span> <span data-ttu-id="2a932-109">Sul dispositivo dell'utente, viene eseguito il provisioning del profilo di Wi-Fi usando l'attivazione dell'URI e l'app **Impostazioni** di Windows.</span><span class="sxs-lookup"><span data-stu-id="2a932-109">On the user's device, the Wi-Fi profile is then provisioned by using URI activation and the Windows **Settings** app.</span></span>

<span data-ttu-id="2a932-110">Questo flusso di lavoro sostituisce il meccanismo in Internet Explorer per il provisioning di Wi-Fi profili che si basa su API JavaScript specifiche di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a932-110">This workflow supersedes the mechanism in Internet Explorer for provisioning Wi-Fi profiles, which relies on Microsoft-specific JavaScript APIs.</span></span> <span data-ttu-id="2a932-111">Questo nuovo flusso di lavoro dovrebbe funzionare con tutti i browser principali.</span><span class="sxs-lookup"><span data-stu-id="2a932-111">This new workflow is expected to work with all major browsers.</span></span>

## <a name="the-workflow-in-more-detail"></a><span data-ttu-id="2a932-112">Il flusso di lavoro in modo più dettagliato</span><span class="sxs-lookup"><span data-stu-id="2a932-112">The workflow in more detail</span></span>

<span data-ttu-id="2a932-113">È possibile attivare questo flusso di lavoro da un collegamento ipertestuale che include come argomento l'URI di download del documento XML di provisioning.</span><span class="sxs-lookup"><span data-stu-id="2a932-113">You can activate this workflow from a hyperlink that includes as an argument the download URI of the provisioning XML document.</span></span>

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

<span data-ttu-id="2a932-114">Il markup HTML seguente, ad esempio, fornisce un collegamento per installare i profili trovati in un documento ipotetico `http://contoso.com/ProvisioningDoc.xml` .</span><span class="sxs-lookup"><span data-stu-id="2a932-114">For example, the following HTML markup gives a link to install the profile(s) that are found in a hypothetical document `http://contoso.com/ProvisioningDoc.xml`.</span></span>

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

<span data-ttu-id="2a932-115">Il codice XML deve essere conforme allo schema di provisioning (vedere [provisioning dell'account](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span><span class="sxs-lookup"><span data-stu-id="2a932-115">Your XML must adhere to the provisioning schema (see [Account provisioning](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span></span> <span data-ttu-id="2a932-116">Il codice XML deve includere anche uno o più elementi [WLANProfile](./wlan-profileschema-wlanprofile-element.md)   .</span><span class="sxs-lookup"><span data-stu-id="2a932-116">Your XML must also include one or more [WLANProfile](./wlan-profileschema-wlanprofile-element.md) elements.</span></span><span data-ttu-id="2a932-117">Ogni profilo verrà visualizzato nella finestra di dialogo **Aggiungi** descritta di seguito.</span><span class="sxs-lookup"><span data-stu-id="2a932-117"> Each profile will be displayed in the **Add** dialog described next.</span></span>

<span data-ttu-id="2a932-118">Quando l'utente fa clic sul collegamento HTML, il flusso di lavoro di installazione viene richiamato nell'app **Impostazioni** .</span><span class="sxs-lookup"><span data-stu-id="2a932-118">When the user clicks your HTML link, the installation workflow is invoked in the **Settings** app.</span></span> <span data-ttu-id="2a932-119">Il documento XML di provisioning viene scaricato dall'app **Impostazioni** .</span><span class="sxs-lookup"><span data-stu-id="2a932-119">Your provisioning XML document is downloaded by the **Settings** app.</span></span> <span data-ttu-id="2a932-120">Una volta scaricato, vengono visualizzate le informazioni sui profili, sulla firma e sul firmatario (purché il documento rispetti lo schema).</span><span class="sxs-lookup"><span data-stu-id="2a932-120">Once it's downloaded, information about the profiles, signature, and signer are displayed (provided that the document adheres to the schema).</span></span>

![App impostazioni](images/install-dialog.png)

<span data-ttu-id="2a932-122">Il pulsante **Aggiungi** nella finestra di dialogo nell'app **Impostazioni** è abilitato solo se il file di provisioning è firmato e attendibile.</span><span class="sxs-lookup"><span data-stu-id="2a932-122">The **Add** button in the dialog in the **Settings** app is enabled only if the provisioning file is signed and trusted.</span></span>

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a><span data-ttu-id="2a932-123">Nella pagina Web determinare se questo flusso di lavoro è supportato</span><span class="sxs-lookup"><span data-stu-id="2a932-123">In your web page, determine whether this workflow is supported</span></span>

<span data-ttu-id="2a932-124">In JavaScript non esiste alcun modo per determinare la versione di build esatta di Windows.</span><span class="sxs-lookup"><span data-stu-id="2a932-124">There is no way in JavaScript to determine the exact build version of Windows.</span></span> <span data-ttu-id="2a932-125">Tuttavia, se l'utente usa il Web browser Microsoft Edge, è possibile determinare la versione di Edge controllando il valore dell' `User-agent` intestazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="2a932-125">But if your user is using the Microsoft Edge web browser, then you can determine the version of Edge by inspecting the value of the `User-agent` HTTP header.</span></span> <span data-ttu-id="2a932-126">Se la versione è maggiore o uguale a `18.nnnnn` , il flusso di lavoro è supportato.</span><span class="sxs-lookup"><span data-stu-id="2a932-126">If the version is greater than or equal to `18.nnnnn`, then the workflow is supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a932-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a932-127">Related topics</span></span>

* [<span data-ttu-id="2a932-128">Provisioning dell'account</span><span class="sxs-lookup"><span data-stu-id="2a932-128">Account provisioning</span></span>](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [<span data-ttu-id="2a932-129">Elemento WLANProfile</span><span class="sxs-lookup"><span data-stu-id="2a932-129">WLANProfile element</span></span>](./wlan-profileschema-wlanprofile-element.md)