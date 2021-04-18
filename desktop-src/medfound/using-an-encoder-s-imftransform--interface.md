---
description: Per la conversione di file multimediali in formato ASF, è possibile utilizzare codificatori Windows Media. Per usare questi codificatori, è necessario registrarli nel sistema.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Creazione di un codificatore tramite CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a19a3ec13f60e7f602fa4f16854efa060dd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310178"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a><span data-ttu-id="02e01-104">Creazione di un codificatore tramite CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="02e01-104">Creating an Encoder by Using CoCreateInstance</span></span>

<span data-ttu-id="02e01-105">Per la conversione di file multimediali in formato ASF, è possibile utilizzare codificatori Windows Media.</span><span class="sxs-lookup"><span data-stu-id="02e01-105">For converting media files into ASF format, you can use Windows Media encoders.</span></span> <span data-ttu-id="02e01-106">Per usare questi codificatori, è necessario registrarli nel sistema.</span><span class="sxs-lookup"><span data-stu-id="02e01-106">To use these encoders, they must be registered with the system.</span></span> <span data-ttu-id="02e01-107">I codificatori vengono implementati come [trasformazioni Media Foundation](media-foundation-transforms.md) (MFTS) ed è necessario esporre l'interfaccia IMFTransform.</span><span class="sxs-lookup"><span data-stu-id="02e01-107">Encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs) and must expose the IMFTransform interface.</span></span> <span data-ttu-id="02e01-108">Questo argomento descrive il modo in cui un'applicazione può ottenere un puntatore all'interfaccia IMFTransform del codificatore MFT richiesta e crearne un'istanza per l'uso.</span><span class="sxs-lookup"><span data-stu-id="02e01-108">This topic describes how an application can get a pointer to the required MFT encoder's IMFTransform interface and instantiate it for use.</span></span>

<span data-ttu-id="02e01-109">Per informazioni sulla registrazione del codificatore, vedere Creazione di un' [istanza di un codificatore MFT](instantiating-the-encoder-mft.md).</span><span class="sxs-lookup"><span data-stu-id="02e01-109">For information about encoder registration, see [Instantiating an Encoder MFT](instantiating-the-encoder-mft.md).</span></span>

-   [<span data-ttu-id="02e01-110">Uso dell'interfaccia IMFTransform di un codificatore</span><span class="sxs-lookup"><span data-stu-id="02e01-110">Using an Encoder's IMFTransform Interface</span></span>](#creating-an-encoder-by-using-cocreateinstance)
    -   [<span data-ttu-id="02e01-111">Esempio di creazione del codificatore</span><span class="sxs-lookup"><span data-stu-id="02e01-111">Encoder Creation Example</span></span>](#encoder-creation-example)
-   [<span data-ttu-id="02e01-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02e01-112">Related topics</span></span>](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a><span data-ttu-id="02e01-113">Uso dell'interfaccia IMFTransform di un codificatore</span><span class="sxs-lookup"><span data-stu-id="02e01-113">Using an Encoder's IMFTransform Interface</span></span>

<span data-ttu-id="02e01-114">Una volta completata la registrazione dei codificatori Windows Media con il sistema, un'applicazione può enumerare i codificatori chiamando [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum).</span><span class="sxs-lookup"><span data-stu-id="02e01-114">Upon successful registration of Windows Media encoders with the system, an application can enumerate the encoders by calling [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum).</span></span> <span data-ttu-id="02e01-115">Per cercare il codificatore corretto, è necessario specificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="02e01-115">To search for the right encoder, you must specify the following:</span></span>

-   <span data-ttu-id="02e01-116">Il GUID che rappresenta la categoria, ovvero la categoria **MFT \_ \_ audio \_ encoder** o la **\_ categoria MFT \_ video \_ encoder**.</span><span class="sxs-lookup"><span data-stu-id="02e01-116">The GUID that represents the category, which is either **MFT\_CATEGORY\_AUDIO\_ENCODER** or **MFT\_CATEGORY\_VIDEO\_ENCODER**.</span></span>

-   <span data-ttu-id="02e01-117">Formato da confrontare.</span><span class="sxs-lookup"><span data-stu-id="02e01-117">The format to match.</span></span> <span data-ttu-id="02e01-118">Questa impostazione è configurata nella struttura di [**\_ informazioni sul \_ tipo \_ di registro MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) che specifica il tipo principale e il sottotipo del tipo di supporto in cui il codificatore genererà gli esempi.</span><span class="sxs-lookup"><span data-stu-id="02e01-118">This is set in the [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structure that specifies the major type and subtype of the media type that the encoder will generate samples in.</span></span> <span data-ttu-id="02e01-119">Questa struttura viene passata nel parametro *pOutputType* .</span><span class="sxs-lookup"><span data-stu-id="02e01-119">This structure is passed in the *pOutputType* parameter.</span></span> <span data-ttu-id="02e01-120">Per informazioni sui tipi supportati, vedere [GUID di tipo multimediale](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="02e01-120">For information about the supported types, see [Media Type GUIDs](media-type-guids.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="02e01-121">Le informazioni sul tipo di input nel parametro *pInputType* non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="02e01-121">The input type information in the *pInputType* parameter is not required.</span></span> <span data-ttu-id="02e01-122">Questo perché il tipo di input è noto all'applicazione e il codificatore prevede che il flusso di input sia in un formato non compresso.</span><span class="sxs-lookup"><span data-stu-id="02e01-122">This is because the input type is known to the application and the encoder expects the input stream to be in an uncompressed format.</span></span>

     

<span data-ttu-id="02e01-123">[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) restituisce una matrice di puntatori [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) per il codificatore MFTS che corrispondono ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="02e01-123">[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) returns an array of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointers for the encoder MFTs that match the search criteria.</span></span> <span data-ttu-id="02e01-124">È possibile creare un'istanza di un codificatore chiamando la funzione COM **CoCreateInstance** e passando il CLSID del codificatore che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="02e01-124">You can instantiate an encoder by calling the COM function **CoCreateInstance** and passing the CLSID of the encoder you want to use.</span></span> <span data-ttu-id="02e01-125">Questa funzione restituisce un puntatore all'interfaccia **IMFTransform** che rappresenta il codificatore.</span><span class="sxs-lookup"><span data-stu-id="02e01-125">This function returns a pointer to the **IMFTransform** interface that represents the encoder.</span></span> <span data-ttu-id="02e01-126">Per ulteriori informazioni su questa chiamata di funzione, vedere la documentazione di Windows SDK per il Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="02e01-126">For more information about this function call, see the Windows SDK documentation for the Component Object Model (COM).</span></span>

### <a name="encoder-creation-example"></a><span data-ttu-id="02e01-127">Esempio di creazione del codificatore</span><span class="sxs-lookup"><span data-stu-id="02e01-127">Encoder Creation Example</span></span>

<span data-ttu-id="02e01-128">Nell'esempio di codice seguente viene illustrato come creare un codificatore audio o video.</span><span class="sxs-lookup"><span data-stu-id="02e01-128">The following code example shows how to create an audio or video encoder.</span></span>


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="02e01-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02e01-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02e01-130">Creazione di un'istanza di un codificatore MFT</span><span class="sxs-lookup"><span data-stu-id="02e01-130">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="02e01-131">Codificatori Windows Media</span><span class="sxs-lookup"><span data-stu-id="02e01-131">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



