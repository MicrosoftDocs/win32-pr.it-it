---
title: Elenchi di stampa e comandi
description: Direct2D \ 32; il controllo di stampa è un nuovo componente del modulo Direct2D in Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399148"
---
# <a name="printing-and-command-lists"></a><span data-ttu-id="be9f6-103">Elenchi di stampa e comandi</span><span class="sxs-lookup"><span data-stu-id="be9f6-103">Printing and command lists</span></span>

<span data-ttu-id="be9f6-104">Il [](./direct2d-portal.md) [**controllo di stampa**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) Direct2D è un nuovo componente del modulo Direct2D in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="be9f6-104">The [Direct2D](./direct2d-portal.md) [**print control**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) is a new component in the Direct2D module in Windows 8.</span></span> <span data-ttu-id="be9f6-105">Questo componente consente alle app Direct2D di riutilizzare le chiamate di disegno Direct2D (in termini di modifiche di stato e primitive di rendering) per fornire risultati di stampa simili a quelli visualizzati sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="be9f6-105">This component lets Direct2D apps reuse their Direct2D drawing calls (in terms of state changes and rending primitives) to deliver printing results that are similar to what you see on the screen.</span></span>

<span data-ttu-id="be9f6-106">L'interfaccia [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) rappresenta un processo di stampa virtuale: è possibile creare un controllo di stampa [Direct2D](./direct2d-portal.md) per avviare un nuovo processo di stampa, passare il contenuto Direct2D per ogni pagina che si desidera stampare, quindi chiudere il controllo di stampa per completare un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="be9f6-106">The [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) interface represents a virtual print job: you can create a [Direct2D](./direct2d-portal.md) print control to initiate a new print job, pass in Direct2D contents for each page you want to print, then close the print control to complete a print job.</span></span>

> [!Note]  
> <span data-ttu-id="be9f6-107">Un controllo di stampa viene mappato a un solo processo di stampa e non può essere riutilizzato.</span><span class="sxs-lookup"><span data-stu-id="be9f6-107">A print control maps to one and exactly one print job, and you can't reuse it.</span></span>

<span data-ttu-id="be9f6-108">Il controllo di stampa [Direct2D](./direct2d-portal.md) converte e ottimizza il contenuto Direct2D passato per il sottosistema di stampa, che funziona con le stampanti reali per fornire la stampa effettiva.</span><span class="sxs-lookup"><span data-stu-id="be9f6-108">The [Direct2D](./direct2d-portal.md) print control converts and optimizes the passed in Direct2D contents for the print sub-system, which works with the real printers to deliver the actual printout.</span></span> <span data-ttu-id="be9f6-109">Tutti i dettagli specifici della stampa sono nascosti dalle app Direct2D, il che significa che le app Direct2D possono stampare senza sapere quali dispositivi stanno disegnando o come i disegni vengono convertiti in stampa.</span><span class="sxs-lookup"><span data-stu-id="be9f6-109">All print-specific details are hidden from Direct2D apps, which means Direct2D apps can print without knowing what devices they are drawing to, or how the drawings are translated to printing.</span></span>

<span data-ttu-id="be9f6-110">Per stampare con [Direct2D](./direct2d-portal.md), è necessario preparare un elenco di comandi Direct2D per ogni pagina che si desidera stampare, quindi passare l'elenco dei comandi al controllo di stampa Direct2D.</span><span class="sxs-lookup"><span data-stu-id="be9f6-110">To print with [Direct2D](./direct2d-portal.md), you need to prepare one Direct2D command list for each page you want to print, then pass that command list to the Direct2D print control.</span></span> <span data-ttu-id="be9f6-111">Per preparare l'elenco dei comandi Direct2D, è sufficiente creare e impostare un elenco di comandi come destinazione del disegno del contesto di dispositivo corrente, quindi disegnarlo nel contesto di dispositivo, esattamente come se si sta disegnando in una destinazione bitmap per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="be9f6-111">To prepare that Direct2D command list, you simply create and set a command list as the drawing target of the current device context, and then draw to that device context, exactly as if you are drawing to a bitmap target for display.</span></span> <span data-ttu-id="be9f6-112">Per altre informazioni su dispositivi e destinazioni, vedere [dispositivi e contesti di dispositivo](devices-and-device-contexts.md) .</span><span class="sxs-lookup"><span data-stu-id="be9f6-112">See [Devices and Device Contexts](devices-and-device-contexts.md) for more info on devices and targets.</span></span>

<span data-ttu-id="be9f6-113">Il diagramma seguente illustra l'interazione tra l'app, il contesto di dispositivo, la destinazione bitmap, la destinazione dell'elenco di comandi e il controllo di stampa.</span><span class="sxs-lookup"><span data-stu-id="be9f6-113">The diagram here illustrates the interaction between the app, device context, bitmap target, command list target, and the print control.</span></span>

> [!Note]  
> <span data-ttu-id="be9f6-114">I componenti di stampa Sub-System e stampante di Windows sono in grigio perché sono completamente nascosti dalle app [Direct2D](./direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="be9f6-114">The Windows Print Sub-System and Printer components are in gray because they are completely hidden from [Direct2D](./direct2d-portal.md) apps.</span></span>

![diagramma che mostra il modo in cui il comando e la stampa interagiscono con un'applicazione e Direct2D.](images/d2dprintcontroldiagram.png)

## <a name="example"></a><span data-ttu-id="be9f6-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="be9f6-116">Example</span></span>

<span data-ttu-id="be9f6-117">Il processo completo di stampa del contenuto Direct2D include i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="be9f6-117">The complete process of printing Direct2D content includes the following steps.</span></span>

1.  <span data-ttu-id="be9f6-118">Creare un controllo di stampa per avviare un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="be9f6-118">Create a print control to initiate a print job.</span></span>
2.  <span data-ttu-id="be9f6-119">Aggiungere una pagina al controllo di stampa passando un elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="be9f6-119">Add a page to the print control by passing in a command list.</span></span>
3.  <span data-ttu-id="be9f6-120">Ripetere il passaggio 2 per ogni pagina nel resto del documento</span><span class="sxs-lookup"><span data-stu-id="be9f6-120">Repeat step 2 for each page in the rest of the document</span></span>
4.  <span data-ttu-id="be9f6-121">Chiudere il controllo di stampa per completare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="be9f6-121">Close the print control to complete the print job.</span></span>

<span data-ttu-id="be9f6-122">Di seguito è riportato un esempio di codice che illustra il processo.</span><span class="sxs-lookup"><span data-stu-id="be9f6-122">Here is a code example showing the process.</span></span>

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a><span data-ttu-id="be9f6-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be9f6-123">Related topics</span></span>

[<span data-ttu-id="be9f6-124">**ID2D1CommandList**</span><span class="sxs-lookup"><span data-stu-id="be9f6-124">**ID2D1CommandList**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[<span data-ttu-id="be9f6-125">**ID2D1PrintControl**</span><span class="sxs-lookup"><span data-stu-id="be9f6-125">**ID2D1PrintControl**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[<span data-ttu-id="be9f6-126">Miglioramento delle prestazioni delle applicazioni e della stampa Direct2D</span><span class="sxs-lookup"><span data-stu-id="be9f6-126">Improving the Performance of Direct2D Applications and Printing</span></span>](improving-direct2d-performance.md)