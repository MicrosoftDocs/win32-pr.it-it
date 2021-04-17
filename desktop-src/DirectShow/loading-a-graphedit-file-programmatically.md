---
description: Caricamento di un file GraphEdit a livello di codice
ms.assetid: 0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a
title: Caricamento di un file GraphEdit a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a4780ead7b65d883bdd48917c6372425612435
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481748"
---
# <a name="loading-a-graphedit-file-programmatically"></a><span data-ttu-id="396b6-103">Caricamento di un file GraphEdit a livello di codice</span><span class="sxs-lookup"><span data-stu-id="396b6-103">Loading a GraphEdit File Programmatically</span></span>

<span data-ttu-id="396b6-104">Un'applicazione può usare l'interfaccia **IPersistStream** per caricare un file GraphEdit (GRF).</span><span class="sxs-lookup"><span data-stu-id="396b6-104">An application can use the **IPersistStream** interface to load a GraphEdit (.grf) file.</span></span> <span data-ttu-id="396b6-105">Usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="396b6-105">Use the following code:</span></span>


```C++
HRESULT LoadGraphFile(IGraphBuilder *pGraph, const WCHAR* wszName)
{
    IStorage *pStorage = 0;
    if (S_OK != StgIsStorageFile(wszName))
    {
        return E_FAIL;
    }
    HRESULT hr = StgOpenStorage(wszName, 0, 
        STGM_TRANSACTED | STGM_READ | STGM_SHARE_DENY_WRITE, 
        0, 0, &pStorage);
    if (FAILED(hr))
    {
        return hr;
    }
    IPersistStream *pPersistStream = 0;
    hr = pGraph->QueryInterface(IID_IPersistStream,
             reinterpret_cast<void**>(&pPersistStream));
    if (SUCCEEDED(hr))
    {
        IStream *pStream = 0;
        hr = pStorage->OpenStream(L"ActiveMovieGraph", 0, 
            STGM_READ | STGM_SHARE_EXCLUSIVE, 0, &pStream);
        if(SUCCEEDED(hr))
        {
            hr = pPersistStream->Load(pStream);
            pStream->Release();
        }
        pPersistStream->Release();
    }
    pStorage->Release();
    return hr;
}

```



> [!Note]  
> <span data-ttu-id="396b6-106">La chiamata a **IPersistStream:: Load** nell'esempio di codice precedente può restituire un errore DirectShow o un codice di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="396b6-106">The call to **IPersistStream::Load** in the previous code example can return a DirectShow error or success code.</span></span> <span data-ttu-id="396b6-107">Per un elenco di possibili valori restituiti, vedere [codici di errore e di esito positivo](error-and-success-codes.md).</span><span class="sxs-lookup"><span data-stu-id="396b6-107">For a list of possible return values, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 

<span data-ttu-id="396b6-108">I file GraphEdit sono destinati solo ai test e al debug.</span><span class="sxs-lookup"><span data-stu-id="396b6-108">GraphEdit files are intended only for testing and debugging.</span></span> <span data-ttu-id="396b6-109">Non sono destinate all'uso da parte delle applicazioni dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="396b6-109">They are not meant for use by end-user applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="396b6-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="396b6-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="396b6-111">Simulazione della creazione di grafici con GraphEdit</span><span class="sxs-lookup"><span data-stu-id="396b6-111">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[<span data-ttu-id="396b6-112">**StgIsStorageFile**</span><span class="sxs-lookup"><span data-stu-id="396b6-112">**StgIsStorageFile**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[<span data-ttu-id="396b6-113">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="396b6-113">**StgOpenStorage**</span></span>](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
