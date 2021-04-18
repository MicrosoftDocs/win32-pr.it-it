---
description: Questo esempio illustra come creare un controllo abilitato per l'input penna da usare in un Web browser. L'esempio accetta il modulo di attestazione automatica originale e lo trasforma in un controllo inserito in una pagina Web.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Esempio di controllo Web Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101537c4cc7b42181cf8d9ff177a5854c5b84054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306744"
---
# <a name="ink-web-control-sample"></a><span data-ttu-id="43079-104">Esempio di controllo Web Ink</span><span class="sxs-lookup"><span data-stu-id="43079-104">Ink Web Control Sample</span></span>

<span data-ttu-id="43079-105">Questo esempio illustra come creare un controllo abilitato per l'input penna da usare in un Web browser.</span><span class="sxs-lookup"><span data-stu-id="43079-105">This sample shows how to create an ink-enabled control for use in a Web browser.</span></span> <span data-ttu-id="43079-106">L'esempio accetta il [modulo di attestazione automatica](auto-claims-form-sample.md) originale e lo trasforma in un controllo inserito in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="43079-106">The sample takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span>

<span data-ttu-id="43079-107">Per ulteriori informazioni sull'utilizzo di input penna sul Web, vedere [input penna sul Web](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="43079-107">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

## <a name="modifications-to-the-original-sample-project"></a><span data-ttu-id="43079-108">Modifiche al progetto di esempio originale</span><span class="sxs-lookup"><span data-stu-id="43079-108">Modifications to the Original Sample Project</span></span>

<span data-ttu-id="43079-109">Questo esempio è costituito da una soluzione che include due progetti e un file HTML.</span><span class="sxs-lookup"><span data-stu-id="43079-109">This sample consists of a solution that includes two projects and an HTML file.</span></span> <span data-ttu-id="43079-110">Il primo progetto, autoclaims, è un progetto di libreria di controlli Microsoft Visual C \# (un controllo utente).</span><span class="sxs-lookup"><span data-stu-id="43079-110">The first project, AutoClaims, is a Microsoft Visual C\# Control Library project (a User Control).</span></span> <span data-ttu-id="43079-111">Il codice sorgente per questo controllo è quasi identico a quello dell'esempio autoclaims con due differenze:</span><span class="sxs-lookup"><span data-stu-id="43079-111">The source code for this control is almost identical to that of the AutoClaims sample with two differences:</span></span>

-   <span data-ttu-id="43079-112">La `AutoClaims` classe in questo esempio eredita dalla classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) anziché dalla classe del [form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="43079-112">The `AutoClaims` class in this sample inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class rather than the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class.</span></span>

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   <span data-ttu-id="43079-113">La classe autoclaims in questo esempio dispone di un metodo pubblico aggiunto, `DisposeResources` che elimina i controlli figlio interni utilizzati per la raccolta di input penna.</span><span class="sxs-lookup"><span data-stu-id="43079-113">The AutoClaims Class in this sample has an added public method, `DisposeResources` that disposes of the internal child controls used for collecting ink.</span></span> <span data-ttu-id="43079-114">Questo metodo deve essere chiamato da thewebpageon, che viene utilizzato dal controllo al termine dell'utilizzo del controllo da parte della pagina.</span><span class="sxs-lookup"><span data-stu-id="43079-114">This method must be called by thewebpageon which the control is used when that page is finished using the control.</span></span>

## <a name="referencing-the-control-in-html"></a><span data-ttu-id="43079-115">Riferimento al controllo in HTML</span><span class="sxs-lookup"><span data-stu-id="43079-115">Referencing the Control in HTML</span></span>

<span data-ttu-id="43079-116">La soluzione include un file HTML, default.htm.</span><span class="sxs-lookup"><span data-stu-id="43079-116">The solution includes an HTML file, default.htm.</span></span> <span data-ttu-id="43079-117">Questo file è la pagina a cui viene spostato il browser per caricare il controllo.</span><span class="sxs-lookup"><span data-stu-id="43079-117">This file is the page that the browser navigates to in order to load the control.</span></span> <span data-ttu-id="43079-118">Il file contiene un <object> tag che fa riferimento al controllo.</span><span class="sxs-lookup"><span data-stu-id="43079-118">The file contains an <object> tag that references the control.</span></span> <span data-ttu-id="43079-119">Include anche uno script che viene chiamato quando la pagina viene scaricata, come indicato dalla presenza dell'attributo onload = " `OnUnload()` " nel</span><span class="sxs-lookup"><span data-stu-id="43079-119">It also includes a script that is called when the page unloads, as indicated by the presence of the onload=" `OnUnload()` " attribute in the</span></span> <body> <span data-ttu-id="43079-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="43079-120">tag.</span></span> <span data-ttu-id="43079-121">Questa funzione chiama il `DisposeResources` metodo sul controllo per assicurarsi che tutte le risorse vengano rilasciate correttamente al momento dell'arresto.</span><span class="sxs-lookup"><span data-stu-id="43079-121">This function calls the `DisposeResources` method on the control to make sure that all resources are properly released at shutdown.</span></span>


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



<span data-ttu-id="43079-122">Si noti il formato del valore dell'attributo ClassID per il <object> tag.</span><span class="sxs-lookup"><span data-stu-id="43079-122">Notice the format of the classid attribute value for the <object> tag.</span></span> <span data-ttu-id="43079-123">Assegna un nome all'assembly, seguito da un \# separatore di segno, quindi dallo spazio dei nomi che contiene il controllo e quindi dal nome della classe del controllo.</span><span class="sxs-lookup"><span data-stu-id="43079-123">It names the assembly, followed with a \# sign separator, and then the namespace that contains the control and then the class name of the control.</span></span>

<span data-ttu-id="43079-124">Un controllo utente reale può probabilmente includere metodi aggiuntivi usati per salvare in modo permanente o inviare i dati raccolti nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="43079-124">A real-world user control would likely include additional methods used to persist or send the data collected in the application.</span></span>

## <a name="the-autoclaims_webcontrol-project"></a><span data-ttu-id="43079-125">Il progetto WebControl autoclaims \_</span><span class="sxs-lookup"><span data-stu-id="43079-125">The AutoClaims\_WebControl Project</span></span>

<span data-ttu-id="43079-126">Il progetto WebControl autoclaims \_ è un progetto di distribuzione che crea un'installazione che aggiunge una radice virtuale, ovvero Autoclaims \_ WebControl, nel server Web al momento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="43079-126">The AutoClaims\_WebControl project is a Deployment Project that creates a setup that adds a virtual root, AutoClaims\_WebControl, on the Web server when installed.</span></span> <span data-ttu-id="43079-127">Il controllo e il file HTML vengono inseriti in questa radice virtuale.</span><span class="sxs-lookup"><span data-stu-id="43079-127">The control and the HTML file are placed in this virtual root.</span></span>

> [!Note]  
> <span data-ttu-id="43079-128">Gli esempi Web compilati non vengono installati tramite l'opzione di installazione predefinita per l'SDK.</span><span class="sxs-lookup"><span data-stu-id="43079-128">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="43079-129">È necessario completare un'installazione personalizzata e selezionare l'opzione secondaria "esempi Web precompilati" per installarli.</span><span class="sxs-lookup"><span data-stu-id="43079-129">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="43079-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43079-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43079-131">Esempio di modulo Claims automatico</span><span class="sxs-lookup"><span data-stu-id="43079-131">Auto Claims Form Sample</span></span>](auto-claims-form-sample.md)
</dt> <dt>

[<span data-ttu-id="43079-132">Input penna sul Web</span><span class="sxs-lookup"><span data-stu-id="43079-132">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> </dl>

 

 
