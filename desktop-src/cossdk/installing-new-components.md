---
description: Per aggiungere componenti alla cartella componenti di un'applicazione COM+, è possibile utilizzare la procedura guidata di installazione dei componenti COM+ o trascinare i file dll che contengono i componenti da Esplora risorse e rilasciarli nell'applicazione.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Installazione di nuovi componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049224"
---
# <a name="installing-new-components"></a><span data-ttu-id="a06a8-103">Installazione di nuovi componenti</span><span class="sxs-lookup"><span data-stu-id="a06a8-103">Installing New Components</span></span>

<span data-ttu-id="a06a8-104">Per aggiungere componenti alla cartella **componenti** di un'applicazione com+, è possibile utilizzare la procedura guidata di installazione dei componenti com+ o trascinare i file dll che contengono i componenti da Esplora risorse e rilasciarli nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a06a8-104">To add components to the **Components** folder of a COM+ application, you can either use the COM+ Component Install Wizard or drag .dll files that contain the components from the Windows Explorer and drop them in the application.</span></span>

<span data-ttu-id="a06a8-105">Se si utilizza l'installazione guidata componenti COM+, è possibile installare un nuovo componente che registra il componente nel computer oppure importa i componenti che sono già stati registrati.</span><span class="sxs-lookup"><span data-stu-id="a06a8-105">If you use the COM+ Component Install Wizard, you can either install a new component, which registers the component on the computer, or import components that have already been registered.</span></span> <span data-ttu-id="a06a8-106">I componenti possono essere aggiunti a applicazioni vuote o a applicazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="a06a8-106">Components can be added to empty applications or existing applications.</span></span>

<span data-ttu-id="a06a8-107">**Per aggiungere un componente a un'applicazione COM+**</span><span class="sxs-lookup"><span data-stu-id="a06a8-107">**To add a component to a COM+ application**</span></span>

1.  <span data-ttu-id="a06a8-108">Nell'albero della console dello strumento di amministrazione Servizi componenti selezionare il computer che ospita l'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="a06a8-108">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="a06a8-109">Aprire la cartella **applicazioni com+** per il computer e selezionare l'applicazione in cui si desidera installare i componenti.</span><span class="sxs-lookup"><span data-stu-id="a06a8-109">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component(s).</span></span>

3.  <span data-ttu-id="a06a8-110">Aprire la cartella dell'applicazione e selezionare **componenti**.</span><span class="sxs-lookup"><span data-stu-id="a06a8-110">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="a06a8-111">Scegliere **nuovo** dal menu **azione** , quindi fare clic su **componente**.</span><span class="sxs-lookup"><span data-stu-id="a06a8-111">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="a06a8-112">È anche possibile fare clic con il pulsante destro del mouse sulla cartella **componenti** , scegliere **nuovo**, quindi fare clic su **componente**.</span><span class="sxs-lookup"><span data-stu-id="a06a8-112">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="a06a8-113">Nella pagina **iniziale** dell'installazione guidata dell'applicazione com+, fare clic su **Avanti**, quindi nella finestra di dialogo **Importa o installa componente** fare clic su **Installa nuovi componenti** .</span><span class="sxs-lookup"><span data-stu-id="a06a8-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Install new components** .</span></span>

6.  <span data-ttu-id="a06a8-114">Nella finestra di dialogo **Installa nuovi componenti** fare clic su **Aggiungi** per cercare il componente che si desidera aggiungere.</span><span class="sxs-lookup"><span data-stu-id="a06a8-114">In the **Install new components** dialog box, click **Add** to browse for the component you want to add.</span></span>

7.  <span data-ttu-id="a06a8-115">Nella finestra di dialogo **selezionare i file da installare** Digitare il nome del file del componente da installare o selezionare un nome di file nell'elenco visualizzato.</span><span class="sxs-lookup"><span data-stu-id="a06a8-115">In the **Select files to install** dialog box, type the filename of the component to install or select a filename from the displayed list.</span></span> <span data-ttu-id="a06a8-116">Fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="a06a8-116">Click **Open**.</span></span>

    <span data-ttu-id="a06a8-117">Dopo aver aggiunto i file, nella finestra di dialogo **Installa nuovi componenti** verranno visualizzati i file aggiunti e i componenti associati.</span><span class="sxs-lookup"><span data-stu-id="a06a8-117">After you add the files, the **Install new components** dialog box displays the files you have added and their associated components.</span></span> <span data-ttu-id="a06a8-118">Se si seleziona la casella di controllo **Dettagli** , vengono visualizzate ulteriori informazioni sul contenuto dei file e sui componenti trovati.</span><span class="sxs-lookup"><span data-stu-id="a06a8-118">If you select the **Details** check box, you will see more information about file contents and the components that were found.</span></span>

    > [!Note]  
    > <span data-ttu-id="a06a8-119">I componenti COM non configurati devono avere una libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="a06a8-119">Unconfigured COM components must have a type library.</span></span> <span data-ttu-id="a06a8-120">Se COM+ non riesce a trovare la libreria dei tipi del componente, il componente non verrà visualizzato nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a06a8-120">If COM+ cannot find your component's type library, your component will not appear in the list.</span></span> <span data-ttu-id="a06a8-121">È anche possibile rimuovere un file dall'elenco **file da installare** selezionandolo e facendo clic su **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="a06a8-121">You can also remove a file from the **Files to install** list by selecting it and clicking **Remove**.</span></span>

     

8.  <span data-ttu-id="a06a8-122">Fare clic su **Avanti** e quindi su **fine** per installare il componente.</span><span class="sxs-lookup"><span data-stu-id="a06a8-122">Click **Next**, and then click **Finish** to install the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a06a8-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a06a8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a06a8-124">Copia di componenti</span><span class="sxs-lookup"><span data-stu-id="a06a8-124">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="a06a8-125">Creazione di una nuova applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="a06a8-125">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="a06a8-126">Eliminazione di un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="a06a8-126">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="a06a8-127">Importazione di componenti</span><span class="sxs-lookup"><span data-stu-id="a06a8-127">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="a06a8-128">Spostamento dei componenti</span><span class="sxs-lookup"><span data-stu-id="a06a8-128">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="a06a8-129">Rimozione di un componente da un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="a06a8-129">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



