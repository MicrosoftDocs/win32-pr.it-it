---
description: Caricamento di un grafoModifica file a livello di codice
ms.assetid: 0e1cff4e-43f8-4d0a-b7a7-b6d0278e9e4a
title: Caricamento di un grafoModifica file a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf2bdff86a47e740e6cb177a70a7b1e12ffc7c865d8ad231f6ada9122f286d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153179"
---
# <a name="loading-a-graphedit-file-programmatically"></a>Caricamento di un grafoModifica file a livello di codice

Un'applicazione può usare **l'interfaccia IPersistStream** per caricare un file GraphEdit (con estensione grf). Usare il codice seguente:


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
> La chiamata a **IPersistStream::Load nell'esempio** di codice precedente può restituire un DirectShow di errore o di esito positivo. Per un elenco dei valori restituiti possibili, vedere [Codici di errore e di esito positivo.](error-and-success-codes.md)

 

I file GraphEdit sono destinati solo a test e debug. Non sono destinati all'uso da parte delle applicazioni degli utenti finali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Simulazione Graph compilazione con GraphModifica](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[**StgIsStorageFile**](/windows/win32/api/coml2api/nf-coml2api-stgisstoragefile)
</dt> <dt>

[**StgOpenStorage**](/windows/win32/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 
