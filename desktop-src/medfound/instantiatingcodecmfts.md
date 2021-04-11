---
description: Creazione di un'istanza di codec MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Creazione di un'istanza di codec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa886f24f7dbd1acc373c7e505baddf71bc3aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226189"
---
# <a name="instantiating-codec-mfts"></a>Creazione di un'istanza di codec MFTs

Le [trasformazioni Media Foundation](media-foundation-transforms.md) (MFTS) sono oggetti com che implementano l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Un MFT è un oggetto per la trasformazione dei dati multimediali come parte di una pipeline. Una pipeline è un grafo aciclici diretto, composto da origini multimediali, trasformazioni di supporti e sink multimediali. Una pipeline elabora i dati multimediali in streaming in modo asincrono.

Sebbene sia possibile creare un'istanza di MFTs e usarlo indipendentemente dall'infrastruttura della pipeline Media Foundation, è preferibile usare il Framework MediaFoundation, laddove possibile.

È possibile creare un codec MFT chiamando la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . È necessario passare l'identificatore di classe di MFT, l'identificatore di interfaccia di [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)e un puntatore a un puntatore **IMFTransform** .

Gli identificatori di classe del codec MFTs sono definiti come costanti nel file di intestazione wmcodecdsp. h.

La costante per l'identificatore di interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) è IID \_ IMFTransform.

Nell'esempio di codice seguente viene illustrato come creare un'istanza di un codec MFT:


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

[Uso di codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 
