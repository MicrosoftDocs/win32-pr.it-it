---
title: Aggiunta di un componente a un progetto Visual Basic
description: Aggiunta di un componente a un progetto Visual Basic
ms.assetid: 7e78853a-b134-46d7-a230-3ee8d80d05c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd64b8367b33590b972adc2439af3a2479ee920e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329388"
---
# <a name="adding-a-component-to-a-visual-basic-project"></a><span data-ttu-id="fa077-103">Aggiunta di un componente a un progetto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fa077-103">Adding a Component to a Visual Basic Project</span></span>

<span data-ttu-id="fa077-104">Nella procedura riportata di seguito viene descritto come aggiungere un oggetto COM come componente a un progetto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fa077-104">The following procedure describes how to add a COM object as a component to a Visual Basic project.</span></span> <span data-ttu-id="fa077-105">L'applicazione può quindi usare le classi di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="fa077-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="fa077-106">L'aggiunta di un controllo come componente espone le proprietà e i metodi di estensione Visual Basic come se facessero parte del controllo.</span><span class="sxs-lookup"><span data-stu-id="fa077-106">Adding a control as a component exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span> <span data-ttu-id="fa077-107">Al contrario, quando si aggiunge un oggetto come riferimento, è possibile utilizzare solo la libreria dei tipi fornita dal controllo o la libreria dei tipi "Raw".</span><span class="sxs-lookup"><span data-stu-id="fa077-107">In contrast, when you add an object as a reference you can only use the type library provided by the control, or the "raw" type library.</span></span>

<span data-ttu-id="fa077-108">**Per inserire un controllo in un progetto Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="fa077-108">**To insert a control into a Visual Basic project**</span></span>

1.  <span data-ttu-id="fa077-109">Scegliere **componenti** dal menu **progetto** .</span><span class="sxs-lookup"><span data-stu-id="fa077-109">On the **Project** menu, click **Components**.</span></span>
2.  <span data-ttu-id="fa077-110">Fare clic per selezionare la casella di controllo accanto al componente che si desidera aggiungere.</span><span class="sxs-lookup"><span data-stu-id="fa077-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="fa077-111">Se il componente non è elencato, individuare il file con estensione dll o ocx utilizzando **Sfoglia**.</span><span class="sxs-lookup"><span data-stu-id="fa077-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="fa077-112">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa077-112">Click **OK**.</span></span>

<span data-ttu-id="fa077-113">Il componente fa ora parte del progetto e viene visualizzato nella barra degli strumenti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fa077-113">The component is now part of the project and appears in the object toolbar.</span></span> <span data-ttu-id="fa077-114">L'applicazione può creare istanze del controllo trascinando il controllo dalla barra degli strumenti e rilasciandolo in un form o in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="fa077-114">Your application can create instances of the control by dragging the control from the toolbar and dropping it onto a form or dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa077-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa077-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa077-116">Aggiunta di un riferimento a un progetto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fa077-116">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="fa077-117">Conversione in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fa077-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




