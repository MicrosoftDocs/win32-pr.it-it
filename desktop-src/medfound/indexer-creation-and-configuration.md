---
description: In questo argomento vengono fornite informazioni sulla creazione dell'oggetto indicizzatore predefinito fornito da Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Creazione e configurazione dell'indicizzatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0a341e3074ca44aa4403a3f2f518b4fb9082d4c6eadee1f4ca94a69e17bd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061201"
---
# <a name="indexer-creation-and-configuration"></a>Creazione e configurazione dell'indicizzatore

*L'indicizzatore* ASF è un componente del livello WMContainer usato per leggere o scrivere oggetti indice in un file ASF (Advanced Systems Format). In questo argomento vengono fornite informazioni sulla creazione dell'oggetto indicizzatore predefinito fornito da Media Foundation.

Per informazioni sulla struttura di un file ASF, vedere [Struttura del file ASF.](asf-file-structure.md)

**Per creare e inizializzare l'indicizzatore ASF**

1.  Chiamare la [**funzione MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) per ricevere un [**puntatore IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) all'oggetto indicizzatore.
2.  Chiamare [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) per specificare la modalità di lettura o scrittura per l'oggetto indicizzatore. Per impostazione predefinita, l'indicizzatore è configurato per la ricerca in avanti.

    

    | Uso                       | Contrassegno                                           |
    |---------------------------|------------------------------------------------|
    | Lettura (ricerca in avanti) | Zero (impostazione predefinita)                                 |
    | Lettura (ricerca inversa) | **LETTURA DELL'INDICIZZATORE MFASF \_ \_ PER \_ \_ REVERSEPLAYBACK** |
    | Scrittura                   | L'INDICIZZATORE MFASF \_ \_ SCRIVE UN NUOVO \_ \_ INDICE              |

    

     

    > [!Note]  
    > La stessa istanza dell'indicizzatore non può essere usata sia per la lettura che per la scrittura. È necessario configurare l'indicizzatore per uno o l'altro.

     

3.  Chiamare [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) per inizializzare l'indicizzatore specificando il puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) dell'oggetto ContentInfo che descrive il file da scrivere o leggere. L'oggetto ContentInfo contiene informazioni che costituiscono [l'oggetto Intestazione ASF.](asf-file-structure.md) L'oggetto indicizzatore richiede un oggetto ContentInfo valido prima di generare o leggere le voci di indice di un file ASF.

Nell'esempio di codice seguente viene illustrato come un'applicazione può creare e inizializzare l'oggetto indicizzatore per l'utilizzo di contenuto ASF specifico. L'oggetto ContentInfo rappresenta l'oggetto Intestazione ASF. il contenuto viene passato come flusso di byte.


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzatore ASF](asf-index-object.md)
</dt> <dt>

[Uso dell'indicizzatore per la ricerca all'interno di un file ASF](using-the-indexer-to-seek.md)
</dt> <dt>

[Uso dell'indicizzatore per scrivere un nuovo indice](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



