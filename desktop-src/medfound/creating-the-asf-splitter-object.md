---
description: Creazione dell'oggetto separatore ASF
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Creazione dell'oggetto separatore ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5782f42b53607943704836c350b76e69d872e8d9654959d4453d8e029c21f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600811"
---
# <a name="creating-the-asf-splitter-object"></a>Creazione dell'oggetto separatore ASF

L'oggetto *barra di* divisione ASF è un oggetto livello WMContainer che analizza l'oggetto dati ASF di un file ASF (Advanced Systems Format). Per creare una nuova istanza dell'oggetto barra di divisione ASF, chiamare la [**funzione MFCreateASFSplitter.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) Questa funzione restituisce un puntatore [**all'interfaccia IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) che rappresenta un oggetto separatore vuoto.

Prima che la barra di divisione possa iniziare l'analisi, l'applicazione deve inizializzare la barra di divisione con le informazioni dell'oggetto intestazione ASF. Per inizializzare la barra di divisione, chiamare il [**metodo IMFASFSplitter::Initialize.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) Questo metodo accetta un puntatore [all'oggetto ContentInfo di ASF](asf-contentinfo-object.md) che contiene le informazioni di intestazione del file ASF da analizzare. L'applicazione deve inizializzare l'oggetto ContentInfo prima di passarlo alla barra di divisione in modo che le caratteristiche del file multimediale siano note all'applicazione. Il metodo **Initialize** della barra di divisione estrae le informazioni del flusso dall'oggetto ContentInfo, ad esempio i numeri di flusso, in modo che la barra di divisione possa analizzare i pacchetti di dati.

### <a name="example"></a>Esempio

L'esempio di codice seguente illustra come creare una barra di divisione e inizializzarla con un oggetto ContentInfo esistente.


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
> In questo esempio viene utilizzata [la funzione SafeRelease](saferelease.md) per rilasciare puntatori a interfaccia.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Barra di divisione ASF](asf-splitter.md)
</dt> </dl>

 

 



