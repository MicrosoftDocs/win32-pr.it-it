---
description: Creazione di istanze di dmo codec
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Creazione di istanze di dmo codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180fcb6a3de7c581f48c7f78981e12b544963cbfb590e521d43413732bcc1e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957551"
---
# <a name="instantiating-codec-dmos"></a>Creazione di istanze di dmo codec

È possibile creare un codec DMO chiamando la funzione COM [**CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) È necessario passare l'identificatore di classe del DMO, l'identificatore di interfaccia **di IMediaObject** e un puntatore a un **puntatore IMediaObject.**

Gli identificatori di classe dei DMO del codec sono definiti come costanti nel file di intestazione wmcodecdsp.h.

La costante per **l'identificatore di interfaccia IMediaObject** è IID \_ IMediaObject.

L'esempio di codice seguente illustra come creare un'istanza di un codec DMO:


```
HRESULT CreateVideoEncoderDMO(IMediaObject** ppDMO)
{
    if(ppDMO == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMediaObject, 
                            (void**)ppDMO);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli oggetti DMO codec](workingwithcodecdmos.md)
</dt> </dl>

 

 
