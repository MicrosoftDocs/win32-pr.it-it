---
description: Creazione dell'oggetto Splitter ASF
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Creazione dell'oggetto Splitter ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42c8033a0861102f6d66b22e43516a616d6428b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878457"
---
# <a name="creating-the-asf-splitter-object"></a><span data-ttu-id="0f848-103">Creazione dell'oggetto Splitter ASF</span><span class="sxs-lookup"><span data-stu-id="0f848-103">Creating the ASF Splitter Object</span></span>

<span data-ttu-id="0f848-104">L'oggetto *splitter* ASF è un oggetto livello WMContainer che analizza l'oggetto dati ASF di un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="0f848-104">The ASF *splitter* object is a WMContainer layer object that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="0f848-105">Per creare una nuova istanza dell'oggetto Splitter ASF, chiamare la funzione [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="0f848-105">To create a new instance of the ASF splitter object, call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function.</span></span> <span data-ttu-id="0f848-106">Questa funzione restituisce un puntatore all'interfaccia [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) che rappresenta un oggetto Splitter vuoto.</span><span class="sxs-lookup"><span data-stu-id="0f848-106">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface that represents an empty splitter object.</span></span>

<span data-ttu-id="0f848-107">Prima che la barra di divisione possa iniziare l'analisi, l'applicazione deve inizializzare la barra di divisione con le informazioni dell'oggetto intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="0f848-107">Before the splitter can begin parsing, the application must initialize the splitter with information from the ASF Header Object.</span></span> <span data-ttu-id="0f848-108">Per inizializzare la barra di divisione, chiamare il metodo [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) .</span><span class="sxs-lookup"><span data-stu-id="0f848-108">To initialize the splitter, call the [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) method.</span></span> <span data-ttu-id="0f848-109">Questo metodo accetta un puntatore all' [oggetto ContentInfo ASF](asf-contentinfo-object.md) che contiene le informazioni di intestazione del file ASF da analizzare.</span><span class="sxs-lookup"><span data-stu-id="0f848-109">This method takes a pointer to the [ASF ContentInfo Object](asf-contentinfo-object.md) that contains header information of the ASF file to parse.</span></span> <span data-ttu-id="0f848-110">L'applicazione deve inizializzare l'oggetto ContentInfo prima di passarlo alla barra di divisione, in modo che le caratteristiche del file multimediale siano note all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0f848-110">The application must initialize the ContentInfo object before passing it to the splitter so that the characteristics of the media file are known to the application.</span></span> <span data-ttu-id="0f848-111">Il metodo **Initialize** della barra di divisione estrae le informazioni sul flusso dall'oggetto ContentInfo, ad esempio i numeri di flusso, in modo che la barra di divisione possa analizzare i pacchetti di dati.</span><span class="sxs-lookup"><span data-stu-id="0f848-111">The splitter's **Initialize** method extracts stream information from the ContentInfo object, such as stream numbers, so the splitter can parse the data packets.</span></span>

### <a name="example"></a><span data-ttu-id="0f848-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="0f848-112">Example</span></span>

<span data-ttu-id="0f848-113">Nell'esempio di codice seguente viene illustrato come creare una barra di divisione e inizializzarla con un oggetto ContentInfo esistente.</span><span class="sxs-lookup"><span data-stu-id="0f848-113">The following code example shows how to create a splitter and initialize it with an existing ContentInfo object.</span></span>


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="0f848-114">Questo esempio usa la funzione [SafeRelease](saferelease.md) per rilasciare i puntatori a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0f848-114">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0f848-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f848-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f848-116">Barra di divisione ASF</span><span class="sxs-lookup"><span data-stu-id="0f848-116">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



