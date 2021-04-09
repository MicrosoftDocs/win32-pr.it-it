---
description: Quando si utilizza COM+ per creare un servizio Web XML, tale servizio può essere utilizzato da qualsiasi client autorizzato, inclusi quelli che non utilizzano COM+ o anche Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Esportazione di un'applicazione SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c92029f431fc06964f233c5746c283821d11c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878017"
---
# <a name="exporting-a-soap-enabled-application"></a><span data-ttu-id="eff0b-103">Esportazione di un'applicazione SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="eff0b-103">Exporting a SOAP-Enabled Application</span></span>

<span data-ttu-id="eff0b-104">Quando si utilizza COM+ per creare un servizio Web XML, tale servizio può essere utilizzato da qualsiasi client autorizzato, inclusi quelli che non utilizzano COM+ o anche Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="eff0b-104">When you use COM+ to create an XML web service, that service can be used by any authorized client, including those not using COM+ or even Microsoft Windows.</span></span> <span data-ttu-id="eff0b-105">Tuttavia, l'utilizzo di un servizio Web COM+ in modalità oggetto attivato dal client da un'applicazione client COM+ è particolarmente semplice.</span><span class="sxs-lookup"><span data-stu-id="eff0b-105">However, using a COM+ web service in client-activated object (CAO) mode from a COM+ client application is especially easy.</span></span> <span data-ttu-id="eff0b-106">È sufficiente esportare l'applicazione abilitata per SOAP in modalità proxy e quindi [importarla](importing-a-soap-enabled-application.md) nel client per cui si desidera accedere al servizio Web XML corrispondente.</span><span class="sxs-lookup"><span data-stu-id="eff0b-106">Just export the SOAP-enabled application in proxy mode, and then [import](importing-a-soap-enabled-application.md) it into the client for which you want to access the corresponding XML web service.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="eff0b-107">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="eff0b-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="eff0b-108">Per esportare un'applicazione abilitata per SOAP da un server, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="eff0b-108">To export a SOAP-enabled application from a server, use the following steps:</span></span>

1.  <span data-ttu-id="eff0b-109">Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.</span><span class="sxs-lookup"><span data-stu-id="eff0b-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="eff0b-110">Fare clic con il pulsante destro del mouse sul componente che si desidera esporre come un servizio Web XML e scegliere **Esporta**.</span><span class="sxs-lookup"><span data-stu-id="eff0b-110">Right-click the component you want to expose as an XML web service, and choose **Export**.</span></span> <span data-ttu-id="eff0b-111">Verrà visualizzata l' **esportazione guidata dell'applicazione com+** .</span><span class="sxs-lookup"><span data-stu-id="eff0b-111">The **COM+ Application Export Wizard** appears.</span></span>

3.  <span data-ttu-id="eff0b-112">Nella casella di testo **immettere il percorso completo e il nome file per il file dell'applicazione da creare**, immettere il percorso completo e il nome file per il file MSI che conterrà l'applicazione esportata oppure fare clic su **Sfoglia** per selezionare il percorso completo e il nome file utilizzando una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="eff0b-112">In the text box labeled **Enter the full path and filename for the application file to be created**, enter the full path and filename for the MSI file that will contain the exported application, or click **Browse** to select the full path and filename using a dialog box.</span></span>

4.  <span data-ttu-id="eff0b-113">In **Esporta con nome** selezionare il **proxy di applicazione-installa in altri computer per abilitare l'accesso al pulsante di opzione computer** .</span><span class="sxs-lookup"><span data-stu-id="eff0b-113">Under **Export As**, select the **Application Proxy – Install on other machines to enable access to this machine** radio button.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="eff0b-114">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="eff0b-114">Visual Basic</span></span>

<span data-ttu-id="eff0b-115">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="eff0b-115">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="eff0b-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="eff0b-116">C/C++</span></span>

<span data-ttu-id="eff0b-117">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="eff0b-117">Does not apply.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eff0b-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eff0b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eff0b-119">Panoramica del servizio SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="eff0b-119">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="eff0b-120">Creazione di servizi Web XML</span><span class="sxs-lookup"><span data-stu-id="eff0b-120">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="eff0b-121">Importazione di un'applicazione SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="eff0b-121">Importing a SOAP-Enabled Application</span></span>](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



