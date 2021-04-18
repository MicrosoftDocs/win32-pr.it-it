---
description: Uso di Windows Media con i servizi di modifica DirectShow
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Uso di Windows Media con i servizi di modifica DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320455"
---
# <a name="using-windows-media-with-directshow-editing-services"></a><span data-ttu-id="5529c-103">Uso di Windows Media con i servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="5529c-103">Using Windows Media With DirectShow Editing Services</span></span>

<span data-ttu-id="5529c-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="5529c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5529c-105">In questa sezione viene descritto come utilizzare il contenuto basato su Windows Media in un'applicazione di [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="5529c-105">This section describes how to use Windows Media–based content in a [DirectShow Editing Services](directshow-editing-services.md) (DES) application.</span></span> <span data-ttu-id="5529c-106">Esistono due scenari principali:</span><span class="sxs-lookup"><span data-stu-id="5529c-106">There are two main scenarios:</span></span>

-   <span data-ttu-id="5529c-107">Clip di origine.</span><span class="sxs-lookup"><span data-stu-id="5529c-107">Source clips.</span></span> <span data-ttu-id="5529c-108">Un progetto DES può contenere clip audio e video da file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5529c-108">A DES project can contain audio and video clips from Windows Media files.</span></span>
-   <span data-ttu-id="5529c-109">Formato di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5529c-109">Target format.</span></span> <span data-ttu-id="5529c-110">Windows Media è un formato ideale per l'output finale di un progetto di modifica video.</span><span class="sxs-lookup"><span data-stu-id="5529c-110">Windows Media is an ideal format for the final output of a video editing project.</span></span>

<span data-ttu-id="5529c-111">Per lavorare con i file di Windows Media, l'applicazione deve fornire un certificato software, detto anche chiave.</span><span class="sxs-lookup"><span data-stu-id="5529c-111">To work with Windows Media files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="5529c-112">Questa operazione viene eseguita implementando un oggetto provider di chiavi.</span><span class="sxs-lookup"><span data-stu-id="5529c-112">It does this by implementing a key provider object.</span></span> <span data-ttu-id="5529c-113">Il provider di chiavi è un oggetto COM che espone l'interfaccia **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="5529c-113">The key provider is a COM object the exposes the **IServiceProvider** interface.</span></span> <span data-ttu-id="5529c-114">Per informazioni sull'implementazione del provider di chiavi, vedere [sblocco di Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="5529c-114">For information about implementing the key provider, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="5529c-115">Per usare DES con i file di Windows Media, gli oggetti DES seguenti richiedono la chiave software:</span><span class="sxs-lookup"><span data-stu-id="5529c-115">To use DES with Windows Media files, the following DES objects require the software key:</span></span>

-   <span data-ttu-id="5529c-116">Motore di rendering, per l'anteprima o la scrittura di file.</span><span class="sxs-lookup"><span data-stu-id="5529c-116">The render engine, for previewing or file writing.</span></span>
-   <span data-ttu-id="5529c-117">Oggetto MediaDet, per ottenere i frame video o i tipi di supporto da file ASF.</span><span class="sxs-lookup"><span data-stu-id="5529c-117">The MediaDet object, to get video frames or media types from ASF files.</span></span>
-   <span data-ttu-id="5529c-118">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="5529c-118">\[!Important\]</span></span>  
    > <span data-ttu-id="5529c-119">Non usare il motore di rendering intelligente per leggere o scrivere file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5529c-119">Do not use the Smart Render Engine to read or write Windows Media files.</span></span> <span data-ttu-id="5529c-120">Usare sempre il motore di rendering di base (CLSID \_ RenderEngine).</span><span class="sxs-lookup"><span data-stu-id="5529c-120">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

     

<span data-ttu-id="5529c-121">Per assegnare a un oggetto la chiave software, eseguire una query sull'oggetto per l'interfaccia **IObjectWithSite** e chiamare **IObjectWithSite:: SESITE** con un puntatore al provider di chiavi.</span><span class="sxs-lookup"><span data-stu-id="5529c-121">To give an object the software key, query that object for the **IObjectWithSite** interface and call **IObjectWithSite::SetSite** with a pointer to your key provider.</span></span> <span data-ttu-id="5529c-122">Il codice seguente, ad esempio, fornisce la chiave software al motore di rendering:</span><span class="sxs-lookup"><span data-stu-id="5529c-122">For example, the following code provides the software key to the render engine:</span></span>


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



<span data-ttu-id="5529c-123">Per usare le clip di origine di Windows Media in un progetto DES, è sufficiente chiamare **IObjectWithSite:: SESITE** nel motore di rendering con un puntatore al provider di chiavi.</span><span class="sxs-lookup"><span data-stu-id="5529c-123">To use Windows Media source clips in a DES project, simply call **IObjectWithSite::SetSite** on the render engine with a pointer to your key provider.</span></span>

<span data-ttu-id="5529c-124">Per informazioni sulla scrittura di file Windows Media, vedere [scrittura di un file Windows Media in des](writing-a-windows-media-file-in-des.md).</span><span class="sxs-lookup"><span data-stu-id="5529c-124">For information about writing Windows Media files, see [Writing a Windows Media File in DES](writing-a-windows-media-file-in-des.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5529c-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5529c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5529c-126">Uso dei servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="5529c-126">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



