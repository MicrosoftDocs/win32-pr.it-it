---
description: Quando un'applicazione abilitata per SOAP è stata esportata da un server in modalità proxy, i client che lo importano possono accedere automaticamente ai metodi dei componenti che contiene, in modalità remota, come servizi Web offerti dal server in modalità oggetto attivato dal client. In questo modo è possibile distribuire con facilità la funzionalità di un'applicazione COM+ in una rete come un servizio Web XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importazione di un'applicazione SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9faca91a726caea765d4b2ca227ddba0ff3a2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524201"
---
# <a name="importing-a-soap-enabled-application"></a><span data-ttu-id="f6c92-104">Importazione di un'applicazione SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="f6c92-104">Importing a SOAP-Enabled Application</span></span>

<span data-ttu-id="f6c92-105">Quando un'applicazione abilitata per SOAP è stata [esportata](exporting-a-soap-enabled-application.md) da un server in modalità proxy, i client che lo importano possono accedere automaticamente ai metodi dei componenti che contiene, in modalità remota, come servizi Web offerti dal server in modalità oggetto attivato dal client.</span><span class="sxs-lookup"><span data-stu-id="f6c92-105">When a SOAP-enabled application has been [exported](exporting-a-soap-enabled-application.md) from a server in proxy mode, clients that import it can automatically access the methods of the components it contains, remotely, as web services offered by the server in client-activated object (CAO) mode.</span></span> <span data-ttu-id="f6c92-106">In questo modo è possibile distribuire con facilità la funzionalità di un'applicazione COM+ in una rete come un servizio Web XML.</span><span class="sxs-lookup"><span data-stu-id="f6c92-106">This allows you to very easily deploy the functionality of a COM+ application across a network as an XML web service.</span></span>

<span data-ttu-id="f6c92-107">Quando i componenti di un'applicazione importati in questo modo vengono utilizzati nel client, non vengono eseguiti sul client ma vengono invece accessibili in modalità remota utilizzando il servizio Web XML fornito dal server da cui è stata esportata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6c92-107">When the components of an application imported in this way are used on the client, they do not run on the client but instead are accessed remotely by using the XML web service provided by the server from which the application was exported.</span></span> <span data-ttu-id="f6c92-108">Per informazioni dettagliate sull'uso dei componenti di un'applicazione importata in questo modo, vedere [accesso ai servizi Web XML in modalità Cao](accessing-xml-web-services-in-cao-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f6c92-108">For details on using the components of an application imported in this way, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="f6c92-109">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="f6c92-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="f6c92-110">Per importare un'applicazione abilitata per SOAP in un client, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="f6c92-110">To import a SOAP-enabled application into a client, use the following steps:</span></span>

1.  <span data-ttu-id="f6c92-111">Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella associata al computer client in cui si desidera installare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6c92-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the folder associated with the client computer on which you want to install the application.</span></span>

2.  <span data-ttu-id="f6c92-112">Fare clic con il pulsante destro del mouse sulla cartella **applicazioni com+** del client, quindi scegliere **nuovo**.</span><span class="sxs-lookup"><span data-stu-id="f6c92-112">Right-click the client's **COM+ Applications** folder, and then choose **New**.</span></span> <span data-ttu-id="f6c92-113">Verrà visualizzata la **procedura guidata di installazione dell'applicazione com+** .</span><span class="sxs-lookup"><span data-stu-id="f6c92-113">The **COM+ Application Install Wizard** appears.</span></span>

3.  <span data-ttu-id="f6c92-114">Nella **procedura guidata di installazione dell'applicazione com+**, fare clic su **Installa applicazione**/e predefinita.</span><span class="sxs-lookup"><span data-stu-id="f6c92-114">In the **COM+ Application Install Wizard**, click **Install pre-built application(s)**.</span></span>

4.  <span data-ttu-id="f6c92-115">Esplorare la rete per individuare o specificare il percorso di rete del file MSI nel server da cui si desidera installare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6c92-115">Browse the network to locate or specify the network path of the MSI file on the server from which you want to install the application.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="f6c92-116">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f6c92-116">Visual Basic</span></span>

<span data-ttu-id="f6c92-117">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="f6c92-117">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="f6c92-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="f6c92-118">C/C++</span></span>

<span data-ttu-id="f6c92-119">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="f6c92-119">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6c92-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6c92-120">Remarks</span></span>

<span data-ttu-id="f6c92-121">I componenti COM sono identificati da un GUID, che cambia se i componenti vengono ricompilati.</span><span class="sxs-lookup"><span data-stu-id="f6c92-121">COM components are identified by a GUID, which changes if the components are recompiled.</span></span> <span data-ttu-id="f6c92-122">Se un componente COM configurato esposto come un servizio Web XML viene ricompilato, le applicazioni client che lo utilizzano si interromperanno.</span><span class="sxs-lookup"><span data-stu-id="f6c92-122">If a configured COM component that is exposed as an XML web service is recompiled, client applications that use it will break.</span></span> <span data-ttu-id="f6c92-123">Pertanto, quando un componente esposto come un servizio Web XML viene ricompilato, i client devono importare nuovamente le applicazioni che utilizzano il componente.</span><span class="sxs-lookup"><span data-stu-id="f6c92-123">Therefore, when a component that is exposed as an XML web service is recompiled, clients should re-import the applications that use the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6c92-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6c92-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6c92-125">Panoramica del servizio SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="f6c92-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="f6c92-126">Creazione di servizi Web XML</span><span class="sxs-lookup"><span data-stu-id="f6c92-126">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="f6c92-127">Esportazione di un'applicazione SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="f6c92-127">Exporting a SOAP-Enabled Application</span></span>](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



