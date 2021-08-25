---
description: Creazione di istanze di codec MFT
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Creazione di istanze di codec MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a73af4055aee1d5b7e6a3ea137ab2204c9e59194f57ae4776e6c8368429db877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827611"
---
# <a name="instantiating-codec-mfts"></a>Creazione di istanze di codec MFT

[Media Foundation transforms](media-foundation-transforms.md) (MFT) sono oggetti COM che implementano [**l'interfaccia IMFTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) Un MFT è un oggetto per la trasformazione dei dati multimediali come parte di una pipeline. Una pipeline è un grafo aciclico diretto, costituito da origini multimediali, trasformazioni multimediali e sink multimediali. Una pipeline elabora i dati multimediali in streaming in modo asincrono.

Anche se è possibile creare istanze di MFT e usarle indipendentemente dall'infrastruttura della pipeline Media Foundation, è preferibile usare il framework MediaFoundation laddove possibile.

È possibile creare un codec MFT chiamando la [**funzione CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) È necessario passare l'identificatore di classe di MFT, l'identificatore di interfaccia [**di IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)e un puntatore a **un puntatore IMFTransform.**

Gli identificatori di classe dei codec MFT sono definiti come costanti nel file di intestazione wmcodecdsp.h.

La costante per [**l'identificatore di interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) è IID \_ IMFTransform.

L'esempio di codice seguente illustra come creare un'istanza di un codec MFT:


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei codec MFT](workingwithcodecmfts.md)
</dt> </dl>

 

 
