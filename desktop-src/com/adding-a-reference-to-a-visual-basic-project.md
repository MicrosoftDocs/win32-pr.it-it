---
title: Aggiunta di un riferimento a un progetto Visual Basic
description: Aggiunta di un riferimento a un progetto Visual Basic
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329383"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a><span data-ttu-id="9a9ee-103">Aggiunta di un riferimento a un progetto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9a9ee-103">Adding a Reference to a Visual Basic Project</span></span>

<span data-ttu-id="9a9ee-104">Nella procedura riportata di seguito viene descritto come aggiungere un riferimento a un oggetto COM a un progetto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9a9ee-104">The following procedure describes how to add a reference to a COM object to a Visual Basic project.</span></span> <span data-ttu-id="9a9ee-105">L'applicazione può quindi usare le classi di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="9a9ee-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="9a9ee-106">Quando si aggiunge un oggetto come riferimento, è possibile utilizzare solo la libreria dei tipi fornita dal controllo o la libreria dei tipi "Raw".</span><span class="sxs-lookup"><span data-stu-id="9a9ee-106">When you add an object as a reference, you can only use the type library provided by the control, or the "raw" type library.</span></span> <span data-ttu-id="9a9ee-107">Al contrario, l'aggiunta di un controllo come componente espone anche le proprietà e i metodi del Visual Basic Extender come se facessero parte del controllo.</span><span class="sxs-lookup"><span data-stu-id="9a9ee-107">In contrast, adding a control as a component also exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span>

<span data-ttu-id="9a9ee-108">**Per creare un riferimento Visual Basic a un componente**</span><span class="sxs-lookup"><span data-stu-id="9a9ee-108">**To make a Visual Basic reference to a component**</span></span>

1.  <span data-ttu-id="9a9ee-109">Nel menu **Progetto**, fare clic su **Riferimenti**.</span><span class="sxs-lookup"><span data-stu-id="9a9ee-109">On the **Project** menu, click **References**.</span></span>
2.  <span data-ttu-id="9a9ee-110">Fare clic per selezionare la casella di controllo accanto al componente che si desidera aggiungere.</span><span class="sxs-lookup"><span data-stu-id="9a9ee-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="9a9ee-111">Se il componente non è elencato, individuare il file con estensione dll o ocx utilizzando **Sfoglia**.</span><span class="sxs-lookup"><span data-stu-id="9a9ee-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="9a9ee-112">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a9ee-112">Click **OK**.</span></span>

<span data-ttu-id="9a9ee-113">Il componente fa ora parte del progetto.</span><span class="sxs-lookup"><span data-stu-id="9a9ee-113">The component is now part of the project.</span></span> <span data-ttu-id="9a9ee-114">L'applicazione può creare istanze di classe usando la parola chiave **New** .</span><span class="sxs-lookup"><span data-stu-id="9a9ee-114">Your application can create class instances using the **New** keyword.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a9ee-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a9ee-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a9ee-116">Aggiunta di un componente a un progetto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9a9ee-116">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="9a9ee-117">Conversione in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9a9ee-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




