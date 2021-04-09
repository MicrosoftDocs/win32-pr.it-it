---
description: Creazione di un'istanza di codec DMOs
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Creazione di un'istanza di codec DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b98848b3e3fee5b3c28389294869eb39005c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966656"
---
# <a name="instantiating-codec-dmos"></a>Creazione di un'istanza di codec DMOs

È possibile creare un codec DMO chiamando la funzione com [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . È necessario passare l'identificatore di classe di DMO, l'identificatore di interfaccia di **IMediaObject** e un puntatore a un puntatore **IMediaObject** .

Gli identificatori di classe del codec DMOs sono definiti come costanti nel file di intestazione wmcodecdsp. h.

La costante per l'identificatore di interfaccia **IMediaObject** è IID \_ IMediaObject.

Nell'esempio di codice seguente viene illustrato come creare un'istanza di un codec DMO:


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

[Uso di codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
