---
title: Conversione in Visual Basic
description: Conversione in Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856401"
---
# <a name="translating-to-visual-basic"></a><span data-ttu-id="b9cc5-103">Conversione in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b9cc5-103">Translating to Visual Basic</span></span>

<span data-ttu-id="b9cc5-104">È possibile aggiungere un oggetto COM al progetto Visual Basic come riferimento o come componente.</span><span class="sxs-lookup"><span data-stu-id="b9cc5-104">You can add a COM object to your Visual Basic project either as a reference or a component.</span></span> <span data-ttu-id="b9cc5-105">Una volta che l'oggetto è stato aggiunto al progetto, l'applicazione può accedere alle classi e alle interfacce.</span><span class="sxs-lookup"><span data-stu-id="b9cc5-105">Once the object is added to your project, your application can access its classes and interfaces.</span></span> <span data-ttu-id="b9cc5-106">È quindi possibile usare il Visualizzatore oggetti Visual Basic per visualizzare le informazioni sulla libreria dei tipi dell'oggetto nella sintassi Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b9cc5-106">You can then use the Visual Basic Object Browser to view the object's type library information in Visual Basic syntax.</span></span>

<span data-ttu-id="b9cc5-107">I controlli vengono in genere aggiunti a un progetto in quanto i componenti e i non controlli vengono aggiunti come riferimenti.</span><span class="sxs-lookup"><span data-stu-id="b9cc5-107">Typically, controls are added to a project as a components and noncontrols are added as references.</span></span> <span data-ttu-id="b9cc5-108">Quando un oggetto COM viene aggiunto come componente, viene visualizzato nella casella degli strumenti Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b9cc5-108">When a COM object is added as a component, it appears in the Visual Basic toolbox.</span></span> <span data-ttu-id="b9cc5-109">Le nuove istanze di tale oggetto vengono create trascinando l'icona dell'oggetto dalla casella degli strumenti in un form Visual Basic o in un altro tipo di contenitore.</span><span class="sxs-lookup"><span data-stu-id="b9cc5-109">New instances of that object are created by dragging the object icon from the toolbox onto a Visual Basic form or other type of container.</span></span> <span data-ttu-id="b9cc5-110">Le nuove istanze di oggetti COM aggiunti come riferimenti vengono create utilizzando la parola chiave **New** .</span><span class="sxs-lookup"><span data-stu-id="b9cc5-110">New instances of COM objects added as references are created using the **new** keyword.</span></span>

<span data-ttu-id="b9cc5-111">La differenza tra l'uso di una classe come riferimento rispetto a un componente è sottile ma importante.</span><span class="sxs-lookup"><span data-stu-id="b9cc5-111">The distinction between using a class as a reference versus a component is subtle but important.</span></span> <span data-ttu-id="b9cc5-112">Quando si aggiunge un oggetto come riferimento, è possibile utilizzare solo la libreria dei tipi fornita dal controllo o la libreria dei tipi "Raw".</span><span class="sxs-lookup"><span data-stu-id="b9cc5-112">When you add an object as a reference, you can use only the type library that the control provides, or the "raw" type library.</span></span>

<span data-ttu-id="b9cc5-113">Se si aggiunge un controllo come componente, Visual Basic unisce le proprietà e i metodi di estensione del form in cui il controllo è incorporato con la libreria dei tipi del controllo, fornendo in tal modo una versione estesa e con wrapper della libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="b9cc5-113">If you add a control as a component, Visual Basic merges the extender properties and methods of the form in which the control is embedded with the control's type library, thus providing a wrapped, extended version of the type library.</span></span> <span data-ttu-id="b9cc5-114">Con questa versione della libreria dei tipi, è possibile usare proprietà Extender come top e Left come se facessero parte del controllo anziché il contenitore del controllo.</span><span class="sxs-lookup"><span data-stu-id="b9cc5-114">With this version of the type library, you can use extender properties such as Top and Left as if they were part of the control, instead of the control's container.</span></span>

<span data-ttu-id="b9cc5-115">Visual Basic attualmente non supporta più librerie dei tipi compilate in un unico file con estensione dll.</span><span class="sxs-lookup"><span data-stu-id="b9cc5-115">Visual Basic does not currently support multiple type libraries built into a single .dll file.</span></span> <span data-ttu-id="b9cc5-116">Se si esegue una DLL che incorpora più librerie dei tipi, è necessario ottenere copie autonome delle librerie dei tipi dall'origine che ha fornito l'oggetto per poter utilizzare l'oggetto con Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b9cc5-116">If you run into a DLL that incorporates multiple type libraries, you should get stand-alone copies of the type libraries from the source that supplied the object in order to use the object with Visual Basic.</span></span>

<span data-ttu-id="b9cc5-117">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="b9cc5-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b9cc5-118">Conversione in Visual Basic da C++</span><span class="sxs-lookup"><span data-stu-id="b9cc5-118">Translating to Visual Basic from C++</span></span>](translating-to-visual-basic-from-c--.md)
-   [<span data-ttu-id="b9cc5-119">Conversione in Visual Basic da Java</span><span class="sxs-lookup"><span data-stu-id="b9cc5-119">Translating to Visual Basic from Java</span></span>](translating-to-visual-basic-from-java.md)
-   [<span data-ttu-id="b9cc5-120">Aggiunta di un componente a un progetto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b9cc5-120">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
-   [<span data-ttu-id="b9cc5-121">Aggiunta di un riferimento a un progetto Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b9cc5-121">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
-   [<span data-ttu-id="b9cc5-122">Visual Basic Visualizzatore oggetti</span><span class="sxs-lookup"><span data-stu-id="b9cc5-122">Visual Basic Object Browser</span></span>](visual-basic-object-browser.md)

## <a name="related-topics"></a><span data-ttu-id="b9cc5-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9cc5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9cc5-124">Conversione in C++</span><span class="sxs-lookup"><span data-stu-id="b9cc5-124">Translating to C++</span></span>](translating-to-c--.md)
</dt> <dt>

[<span data-ttu-id="b9cc5-125">Conversione in Java</span><span class="sxs-lookup"><span data-stu-id="b9cc5-125">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




