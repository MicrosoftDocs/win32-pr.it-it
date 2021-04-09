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
# <a name="instantiating-codec-dmos"></a><span data-ttu-id="4321f-103">Creazione di un'istanza di codec DMOs</span><span class="sxs-lookup"><span data-stu-id="4321f-103">Instantiating Codec DMOs</span></span>

<span data-ttu-id="4321f-104">È possibile creare un codec DMO chiamando la funzione com [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="4321f-104">You can create a codec DMO by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="4321f-105">È necessario passare l'identificatore di classe di DMO, l'identificatore di interfaccia di **IMediaObject** e un puntatore a un puntatore **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="4321f-105">You must pass the class identifier of the DMO, the interface identifier of **IMediaObject**, and a pointer to an **IMediaObject** pointer.</span></span>

<span data-ttu-id="4321f-106">Gli identificatori di classe del codec DMOs sono definiti come costanti nel file di intestazione wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="4321f-106">The class identifiers of the codec DMOs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="4321f-107">La costante per l'identificatore di interfaccia **IMediaObject** è IID \_ IMediaObject.</span><span class="sxs-lookup"><span data-stu-id="4321f-107">The constant for the **IMediaObject** interface identifier is IID\_IMediaObject.</span></span>

<span data-ttu-id="4321f-108">Nell'esempio di codice seguente viene illustrato come creare un'istanza di un codec DMO:</span><span class="sxs-lookup"><span data-stu-id="4321f-108">The following code example demonstrates how to create an instance of a codec DMO:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4321f-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4321f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4321f-110">Uso di codec DMOs</span><span class="sxs-lookup"><span data-stu-id="4321f-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
