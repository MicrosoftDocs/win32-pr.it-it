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
# <a name="creating-the-asf-splitter-object"></a>Creazione dell'oggetto Splitter ASF

L'oggetto *splitter* ASF è un oggetto livello WMContainer che analizza l'oggetto dati ASF di un file di formato Advanced Systems (ASF). Per creare una nuova istanza dell'oggetto Splitter ASF, chiamare la funzione [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) . Questa funzione restituisce un puntatore all'interfaccia [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) che rappresenta un oggetto Splitter vuoto.

Prima che la barra di divisione possa iniziare l'analisi, l'applicazione deve inizializzare la barra di divisione con le informazioni dell'oggetto intestazione ASF. Per inizializzare la barra di divisione, chiamare il metodo [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) . Questo metodo accetta un puntatore all' [oggetto ContentInfo ASF](asf-contentinfo-object.md) che contiene le informazioni di intestazione del file ASF da analizzare. L'applicazione deve inizializzare l'oggetto ContentInfo prima di passarlo alla barra di divisione, in modo che le caratteristiche del file multimediale siano note all'applicazione. Il metodo **Initialize** della barra di divisione estrae le informazioni sul flusso dall'oggetto ContentInfo, ad esempio i numeri di flusso, in modo che la barra di divisione possa analizzare i pacchetti di dati.

### <a name="example"></a>Esempio

Nell'esempio di codice seguente viene illustrato come creare una barra di divisione e inizializzarla con un oggetto ContentInfo esistente.


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
> Questo esempio usa la funzione [SafeRelease](saferelease.md) per rilasciare i puntatori a interfaccia.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Barra di divisione ASF](asf-splitter.md)
</dt> </dl>

 

 



