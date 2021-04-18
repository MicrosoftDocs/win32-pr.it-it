---
description: Qualsiasi applicazione COM+ può essere esposta come un servizio Web XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Creazione di servizi Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304827"
---
# <a name="creating-xml-web-services"></a><span data-ttu-id="690b1-103">Creazione di servizi Web XML</span><span class="sxs-lookup"><span data-stu-id="690b1-103">Creating XML Web Services</span></span>

<span data-ttu-id="690b1-104">Qualsiasi applicazione COM+ può essere esposta come un servizio Web XML.</span><span class="sxs-lookup"><span data-stu-id="690b1-104">Any COM+ application can be exposed as an XML web service.</span></span> <span data-ttu-id="690b1-105">I metodi nelle interfacce predefinite dei componenti configurati per le applicazioni (componenti nel catalogo COM+ Server) possono essere chiamati in remoto.</span><span class="sxs-lookup"><span data-stu-id="690b1-105">The methods in the default interfaces of the applications configured components (components in the servers COM+ catalog) can then be called remotely.</span></span> <span data-ttu-id="690b1-106">È possibile utilizzare lo strumento di amministrazione Servizi componenti per creare una directory radice virtuale IIS dalla quale è possibile chiamare i metodi dei componenti utilizzando SOAP.</span><span class="sxs-lookup"><span data-stu-id="690b1-106">You can use the Component Services administrative tool to create an IIS virtual root directory from which the component methods can be called by using SOAP.</span></span>

> [!Note]  
> <span data-ttu-id="690b1-107">Per esporre un'applicazione COM+ come un servizio Web XML, è necessario che nel computer sia installato il .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="690b1-107">The .NET Framework must be installed on your computer in order to expose a COM+ application as an XML web service.</span></span>

 

<span data-ttu-id="690b1-108">**Per esporre un'applicazione COM+ come un servizio Web XML**</span><span class="sxs-lookup"><span data-stu-id="690b1-108">**To expose a COM+ application as an XML web service**</span></span>

1.  <span data-ttu-id="690b1-109">Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.</span><span class="sxs-lookup"><span data-stu-id="690b1-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="690b1-110">Fare clic con il pulsante destro del mouse sull'applicazione che si desidera esporre come un servizio Web XML e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="690b1-110">Right-click the application you want to expose as an XML web service, and choose **Properties**.</span></span>

3.  <span data-ttu-id="690b1-111">Fare clic sulla scheda **attivazione** nella finestra di dialogo Proprietà.</span><span class="sxs-lookup"><span data-stu-id="690b1-111">Click the **Activation** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="690b1-112">Selezionare la casella di controllo **USA SOAP** .</span><span class="sxs-lookup"><span data-stu-id="690b1-112">Select the **Uses SOAP** check box.</span></span>

5.  <span data-ttu-id="690b1-113">Nella casella di testo **SOAP vroot** immettere il nome della directory radice virtuale di IIS da cui è possibile accedere in remoto ai metodi dei componenti.</span><span class="sxs-lookup"><span data-stu-id="690b1-113">In the **SOAP VRoot** text box, enter the name of the IIS virtual root directory from which the components methods can be accessed remotely.</span></span> <span data-ttu-id="690b1-114">Si noti che un VRoot SOAP non può essere una sottodirectory di un'altra directory VRoot SOAP.</span><span class="sxs-lookup"><span data-stu-id="690b1-114">Note that a SOAP VRoot cannot be a subdirectory of another SOAP VRoot directory.</span></span>

6.  <span data-ttu-id="690b1-115">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="690b1-115">Click **OK**.</span></span>

    <span data-ttu-id="690b1-116">Se si specifica la directory radice virtuale IIS come *VRoot* e il nome di dominio completo del server è *ServerName*, l'URL in cui il componente viene esposto come un servizio Web XML è https://*nomeserver* / *VRoot*/.</span><span class="sxs-lookup"><span data-stu-id="690b1-116">If you specify the IIS virtual root directory as *vroot* and if your servers fully qualified domain name is *servername*, the URL where your component is exposed as an XML web service is https://*servername*/*vroot*/.</span></span>

    <span data-ttu-id="690b1-117">La directory corrispondente nella file system è \\ Windows \\ system32 \\ com \\ SoapVRoots \\ *VRoot* \\ ; COM+ inserisce diversi file di configurazione e programmi ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="690b1-117">The corresponding directory in your file system is \\windows\\system32\\com\\SoapVRoots\\*vroot*\\; COM+ places several configuration files and ASP.NET programs there.</span></span> <span data-ttu-id="690b1-118">Per un servizio Web XML in condizioni di carico elevato, è consigliabile modificare i parametri archiviati nel file web.config. Per informazioni su questo file, vedere la documentazione di IIS.</span><span class="sxs-lookup"><span data-stu-id="690b1-118">For an XML web service under heavy load, you may want to adjust the parameters stored in the file web.config. For information about this file, consult the IIS documentation.</span></span>

    <span data-ttu-id="690b1-119">Le impostazioni di sicurezza predefinite per un'applicazione COM+ esposte come servizio Web XML variano a seconda della versione del .NET Framework installata.</span><span class="sxs-lookup"><span data-stu-id="690b1-119">The default security settings for a COM+ application exposed as an XML web service differ depending on which version of the .NET Framework is installed.</span></span> <span data-ttu-id="690b1-120">Se è installata la versione 1,0, i servizi Web XML non sono protetti per impostazione predefinita. tutte le chiamate vengono accettate e non viene utilizzata alcuna crittografia.</span><span class="sxs-lookup"><span data-stu-id="690b1-120">If version 1.0 is installed, XML web services are nonsecure by default; all calls are accepted and no encryption is used.</span></span> <span data-ttu-id="690b1-121">Se è installata la versione 1,1 o una versione successiva, i servizi Web XML sono protetti per impostazione predefinita. i chiamanti devono essere autenticati e la crittografia è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="690b1-121">If version 1.1 or later is installed, XML web services are secure by default; callers must be authenticated and encryption is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="690b1-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="690b1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="690b1-123">Accesso ai servizi Web XML in modalità CAO</span><span class="sxs-lookup"><span data-stu-id="690b1-123">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="690b1-124">Accesso ai servizi Web XML in modalità WKO</span><span class="sxs-lookup"><span data-stu-id="690b1-124">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="690b1-125">Panoramica del servizio SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="690b1-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="690b1-126">Protezione dei servizi Web XML</span><span class="sxs-lookup"><span data-stu-id="690b1-126">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 



