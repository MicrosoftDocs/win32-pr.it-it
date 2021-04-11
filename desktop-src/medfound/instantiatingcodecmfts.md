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
# <a name="instantiating-codec-mfts"></a><span data-ttu-id="feb72-103">Creazione di un'istanza di codec MFTs</span><span class="sxs-lookup"><span data-stu-id="feb72-103">Instantiating Codec MFTs</span></span>

<span data-ttu-id="feb72-104">Le [trasformazioni Media Foundation](media-foundation-transforms.md) (MFTS) sono oggetti com che implementano l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="feb72-104">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) are COM objects that implement the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="feb72-105">Un MFT è un oggetto per la trasformazione dei dati multimediali come parte di una pipeline.</span><span class="sxs-lookup"><span data-stu-id="feb72-105">An MFT is an object for transforming multimedia data as part of a pipeline.</span></span> <span data-ttu-id="feb72-106">Una pipeline è un grafo aciclici diretto, composto da origini multimediali, trasformazioni di supporti e sink multimediali.</span><span class="sxs-lookup"><span data-stu-id="feb72-106">A pipeline is a directed acyclic graph, consisting of media sources, media transforms, and media sinks.</span></span> <span data-ttu-id="feb72-107">Una pipeline elabora i dati multimediali in streaming in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="feb72-107">A pipeline processes streaming multimedia data asynchronously.</span></span>

<span data-ttu-id="feb72-108">Sebbene sia possibile creare un'istanza di MFTs e usarlo indipendentemente dall'infrastruttura della pipeline Media Foundation, è preferibile usare il Framework MediaFoundation, laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="feb72-108">Although MFTs can be instantiated and used independently of the Media Foundation pipeline infrastructure, it is preferable to use the MediaFoundation framework where possible.</span></span>

<span data-ttu-id="feb72-109">È possibile creare un codec MFT chiamando la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="feb72-109">You can create a codec MFT by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="feb72-110">È necessario passare l'identificatore di classe di MFT, l'identificatore di interfaccia di [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)e un puntatore a un puntatore **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="feb72-110">You must pass the class identifier of the MFT, the interface identifier of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), and a pointer to an **IMFTransform** pointer.</span></span>

<span data-ttu-id="feb72-111">Gli identificatori di classe del codec MFTs sono definiti come costanti nel file di intestazione wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="feb72-111">The class identifiers of the codec MFTs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="feb72-112">La costante per l'identificatore di interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) è IID \_ IMFTransform.</span><span class="sxs-lookup"><span data-stu-id="feb72-112">The constant for the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface identifier is IID\_IMFTransform.</span></span>

<span data-ttu-id="feb72-113">Nell'esempio di codice seguente viene illustrato come creare un'istanza di un codec MFT:</span><span class="sxs-lookup"><span data-stu-id="feb72-113">The following code example demonstrates how to create an instance of a codec MFT:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="feb72-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="feb72-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feb72-115">Uso di codec MFTs</span><span class="sxs-lookup"><span data-stu-id="feb72-115">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 
