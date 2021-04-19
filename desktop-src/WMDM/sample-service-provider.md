---
title: Provider di servizi di esempio
description: Provider di servizi di esempio
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Windows Media Gestione dispositivi, esempi
- Gestione dispositivi, esempi
- Windows Media Gestione dispositivi, esempio di provider di servizi
- Gestione dispositivi, esempio di provider di servizi
- provider di servizi, esempi
- esempi, provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298272"
---
# <a name="sample-service-provider"></a><span data-ttu-id="8af4d-109">Provider di servizi di esempio</span><span class="sxs-lookup"><span data-stu-id="8af4d-109">Sample Service Provider</span></span>

<span data-ttu-id="8af4d-110">Windows Media Gestione dispositivi SDK include un provider di servizi di esempio che è possibile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="8af4d-110">The Windows Media Device Manager SDK includes a sample service provider for you to use.</span></span> <span data-ttu-id="8af4d-111">Questo provider di servizi include una classe che segnala ogni disco rigido del computer come se fosse un dispositivo collegato.</span><span class="sxs-lookup"><span data-stu-id="8af4d-111">This service provider includes a class that reports each hard drive on the computer as if it were an attached device.</span></span> <span data-ttu-id="8af4d-112">L'unica applicazione che utilizzerà questo provider di servizi è l'applicazione di esempio; In Esplora risorse non vengono visualizzati i "dispositivi" segnalati da questo provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="8af4d-112">The only application that will use this service provider is the sample application; Windows Explorer will not see the "devices" reported by this service provider.</span></span> <span data-ttu-id="8af4d-113">Il provider di servizi di esempio è un oggetto COM basato su ATL.</span><span class="sxs-lookup"><span data-stu-id="8af4d-113">The service provider sample is a COM object built on ATL.</span></span> <span data-ttu-id="8af4d-114">Nei passaggi seguenti viene illustrato come utilizzare il provider di servizi di esempio:</span><span class="sxs-lookup"><span data-stu-id="8af4d-114">The following steps explain how to use the sample service provider:</span></span>

> [!Note]  
> <span data-ttu-id="8af4d-115">Il provider di servizi di esempio implementa pochissime funzionalità e pertanto non deve essere utilizzato per il test di applicazioni Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="8af4d-115">The sample service provider implements very few features, and so it should not be used for testing Windows Media Device Manager applications.</span></span> <span data-ttu-id="8af4d-116">Per testare un'applicazione, usare un provider di servizi completamente implementato.</span><span class="sxs-lookup"><span data-stu-id="8af4d-116">To test an application, use a fully-implemented service provider.</span></span>

 

-   <span data-ttu-id="8af4d-117">L'esempio è stato fornito con un errore di codifica che comporterebbe il malfunzionamento del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="8af4d-117">The sample was shipped with a coding error that will cause the service provider to malfunction.</span></span> <span data-ttu-id="8af4d-118">Per correggere l'errore, aprire il file MDSPEnumStorage. cpp installato nella cartella < *percorso di installazione di SDK*  > \\ WMFSDK95 \\ WMDM \\ MDSP \\ mshdsp, andare alla riga 185 e modificare la riga seguente:</span><span class="sxs-lookup"><span data-stu-id="8af4d-118">To correct this error, open the MDSPEnumStorage.cpp file installed in the folder < *SDK installation path* >\\WMFSDK95\\WMDM\\mdsp\\mshdsp, go to line 185, and change the following line:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

<span data-ttu-id="8af4d-119">A questo scopo:</span><span class="sxs-lookup"><span data-stu-id="8af4d-119">To this:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  <span data-ttu-id="8af4d-120">Compilare il file di MsHDSP.dll.</span><span class="sxs-lookup"><span data-stu-id="8af4d-120">Compile the MsHDSP.dll file.</span></span> <span data-ttu-id="8af4d-121">Questa operazione può essere eseguita tramite NMAKE o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8af4d-121">You can do this using either NMAKE or Visual Studio.</span></span> <span data-ttu-id="8af4d-122">Per informazioni su come compilare l'applicazione, vedere [compilazione del provider di servizi di esempio mediante NMAKE](compiling-the-sample-service-provider-using-nmake.md) o [compilazione del provider di servizi di esempio mediante Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) .</span><span class="sxs-lookup"><span data-stu-id="8af4d-122">See [Compiling the Sample Service Provider Using NMAKE](compiling-the-sample-service-provider-using-nmake.md) or [Compiling the Sample Service Provider Using Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) to learn how to compile the application.</span></span>
2.  <span data-ttu-id="8af4d-123">Registrare MsHDSP.dll usando Regsvr32.</span><span class="sxs-lookup"><span data-stu-id="8af4d-123">Register MsHDSP.dll using regsvr32.</span></span> <span data-ttu-id="8af4d-124">La riga seguente, digitata in una finestra del prompt dei comandi nella stessa cartella MsHDSP.dll, registrerà il provider di servizi di esempio:</span><span class="sxs-lookup"><span data-stu-id="8af4d-124">The following line, typed into a command-prompt window in the same folder as MsHDSP.dll, will register the sample service provider:</span></span>

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    <span data-ttu-id="8af4d-125">Per arrestare la rappresentazione di un dispositivo, immettere la riga seguente al prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="8af4d-125">To stop impersonating a device, enter the following line at the command prompt:</span></span>

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  <span data-ttu-id="8af4d-126">I dispositivi rimovibili rappresentati da questa DLL possono essere visualizzati solo dall'applicazione di esempio fornita con questo SDK.</span><span class="sxs-lookup"><span data-stu-id="8af4d-126">The removable devices impersonated by this DLL can only be seen by the sample application shipped with this SDK.</span></span> <span data-ttu-id="8af4d-127">Compilare l'applicazione di esempio usando uno dei metodi descritti in [esempio di applicazione desktop](sample-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="8af4d-127">Compile the sample application using one of the methods described in [Sample Desktop Application](sample-desktop-application.md).</span></span>
4.  <span data-ttu-id="8af4d-128">Per eseguire il debug del provider di servizi con Visual Studio, aprire il provider di servizi in Visual Studio e scegliere **Avvia** dal menu **debug** .</span><span class="sxs-lookup"><span data-stu-id="8af4d-128">To debug the service provider with Visual Studio, open the service provider in Visual Studio and select **Start** on the **Debug** menu.</span></span> <span data-ttu-id="8af4d-129">Nella finestra di dialogo popup passare all'applicazione di esempio compilata nel passaggio precedente, fare clic su **OK** e il provider di servizi inizierà l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="8af4d-129">In the popup dialog box, browse to the sample application you built in the preceding step, and click **OK**, and the service provider will begin running in debug mode.</span></span>

    <span data-ttu-id="8af4d-130">Per eseguire il provider di servizi senza eseguire il debug in Visual Studio, è sufficiente registrare il msdhsp.dll ed eseguire l'applicazione desktop di esempio fornita con l'SDK.</span><span class="sxs-lookup"><span data-stu-id="8af4d-130">To run the service provider without debugging in Visual Studio, simply register the msdhsp.dll and run the sample desktop application that ships with the SDK.</span></span> <span data-ttu-id="8af4d-131">L'applicazione desktop di esempio esegue il provider di servizi di esempio automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8af4d-131">The sample desktop application runs the sample service provider automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8af4d-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8af4d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8af4d-133">**Esempi**</span><span class="sxs-lookup"><span data-stu-id="8af4d-133">**Samples**</span></span>](samples.md)
</dt> </dl>

 

 




