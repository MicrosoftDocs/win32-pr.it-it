---
description: È possibile utilizzare lo strumento di amministrazione Servizi componenti per importare in applicazioni componenti specifici che sono già stati registrati nel computer come componenti COM nel registro di sistema di Windows.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Importazione di componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483036"
---
# <a name="importing-components"></a><span data-ttu-id="0cc3f-103">Importazione di componenti</span><span class="sxs-lookup"><span data-stu-id="0cc3f-103">Importing Components</span></span>

<span data-ttu-id="0cc3f-104">È possibile utilizzare lo strumento di amministrazione Servizi componenti per importare in applicazioni componenti specifici che sono già stati registrati nel computer come componenti COM nel registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-104">You can use the Component Services administrative tool to import into applications specific components that have already been registered on your computer as COM components in the Windows registry.</span></span> <span data-ttu-id="0cc3f-105">L'importazione di un componente non comporta l'installazione delle informazioni sull'interfaccia o sul metodo necessarie per impostare le proprietà dell'interfaccia o per configurare l'accesso al componente da un client remoto.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-105">Importing a component does not install the interface or method information required to set interface properties or to configure access to the component from a remote client.</span></span> <span data-ttu-id="0cc3f-106">Pertanto, se possibile, è consigliabile installare anziché importare componenti non configurati.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-106">Therefore, if possible, you should install rather than import unconfigured components.</span></span>

> [!Note]  
> <span data-ttu-id="0cc3f-107">Quando si importa un componente in un'applicazione COM+, COM+ non popola le informazioni sul metodo e sull'interfaccia per il componente.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-107">When importing a component into a COM+ application, COM+ does not populate interface and method information for the component.</span></span> <span data-ttu-id="0cc3f-108">Durante l'esportazione di un proxy di applicazione, COM+ non fornirà informazioni di marshalling (librerie dei tipi o proxy/stub) per alcune o tutte le interfacce.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-108">During the export of an application proxy, COM+ will not provide marshaling information (type libraries or proxy/stubs) for some or all of the interfaces.</span></span> <span data-ttu-id="0cc3f-109">L'esportazione di proxy di applicazione contenenti componenti importati avrà esito negativo o verrà generato un avviso.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-109">Exporting application proxies that contain imported components will fail or cause a warning to be issued.</span></span>

 

<span data-ttu-id="0cc3f-110">**Per importare un componente in un'applicazione COM+**</span><span class="sxs-lookup"><span data-stu-id="0cc3f-110">**To import a component into a COM+ application**</span></span>

1.  <span data-ttu-id="0cc3f-111">Nell'albero della console dello strumento di amministrazione Servizi componenti selezionare il computer che ospita l'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-111">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="0cc3f-112">Aprire la cartella **applicazioni com+** per il computer e selezionare l'applicazione in cui si desidera installare il componente.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-112">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component.</span></span>

3.  <span data-ttu-id="0cc3f-113">Aprire la cartella dell'applicazione e selezionare **componenti**.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-113">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="0cc3f-114">Scegliere **nuovo** dal menu **azione** , quindi fare clic su **componente**.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-114">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="0cc3f-115">È anche possibile fare clic con il pulsante destro del mouse sulla cartella **componenti** , scegliere **nuovo**, quindi fare clic su **componente**.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-115">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="0cc3f-116">Nella pagina **iniziale** dell'installazione guidata dell'applicazione com+, fare clic su **Avanti**, quindi nella finestra di dialogo **Importa o installa componente** fare clic su **Importa componente/i che sono già registrati**.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-116">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Import component(s) that are already registered**.</span></span>

6.  <span data-ttu-id="0cc3f-117">Nella finestra di dialogo **scegliere i componenti da importare** , selezionare la casella di controllo **Dettagli** per visualizzare le informazioni complete sui componenti che sono già registrati.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-117">In the **Choose Components to Import** dialog box, select the **Details** check box to see complete information about the components that are already registered.</span></span> <span data-ttu-id="0cc3f-118">Selezionare i componenti che si desidera importare dall'elenco visualizzato, quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-118">Select the component(s) you want to import from the displayed list, and click **Next**.</span></span>

7.  <span data-ttu-id="0cc3f-119">Fare clic su **Fine**.</span><span class="sxs-lookup"><span data-stu-id="0cc3f-119">Click **Finish**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cc3f-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cc3f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cc3f-121">Copia di componenti</span><span class="sxs-lookup"><span data-stu-id="0cc3f-121">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="0cc3f-122">Creazione di una nuova applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="0cc3f-122">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="0cc3f-123">Eliminazione di un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="0cc3f-123">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="0cc3f-124">Installazione di nuovi componenti</span><span class="sxs-lookup"><span data-stu-id="0cc3f-124">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="0cc3f-125">Spostamento dei componenti</span><span class="sxs-lookup"><span data-stu-id="0cc3f-125">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="0cc3f-126">Rimozione di un componente da un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="0cc3f-126">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



