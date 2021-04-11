---
description: In questa sezione viene descritto come enumerare Media Foundation trasformazioni e come registrare un MFT personalizzato in modo che le applicazioni possano individuarlo.
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: Registrazione ed enumerazione di MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771a22b469d472dbc59d07c2754405276883bef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966981"
---
# <a name="registering-and-enumerating-mfts"></a><span data-ttu-id="0c553-103">Registrazione ed enumerazione di MFTs</span><span class="sxs-lookup"><span data-stu-id="0c553-103">Registering and Enumerating MFTs</span></span>

<span data-ttu-id="0c553-104">In questa sezione viene descritto come enumerare Media Foundation trasformazioni e come registrare un MFT personalizzato in modo che le applicazioni possano individuarlo.</span><span class="sxs-lookup"><span data-stu-id="0c553-104">This section describes how to enumerate Media Foundation transforms, and how to register a custom MFT so that applications can discover it.</span></span>

-   [<span data-ttu-id="0c553-105">Enumerazione di MFTs</span><span class="sxs-lookup"><span data-stu-id="0c553-105">Enumerating MFTs</span></span>](#registering-and-enumerating-mfts)
-   [<span data-ttu-id="0c553-106">Registrazione di MFTs</span><span class="sxs-lookup"><span data-stu-id="0c553-106">Registering MFTs</span></span>](#registering-mfts)
-   [<span data-ttu-id="0c553-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c553-107">Related topics</span></span>](#related-topics)

## <a name="enumerating-mfts"></a><span data-ttu-id="0c553-108">Enumerazione di MFTs</span><span class="sxs-lookup"><span data-stu-id="0c553-108">Enumerating MFTs</span></span>

<span data-ttu-id="0c553-109">Per individuare MFTs registrate nel sistema, un'applicazione può chiamare la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="0c553-109">To discover MFTs that are registered on the system, an application can call the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

> [!Note]  
> <span data-ttu-id="0c553-110">Questa funzione richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c553-110">This function requires to Windows 7.</span></span> <span data-ttu-id="0c553-111">Prima di Windows 7, le applicazioni devono invece usare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .</span><span class="sxs-lookup"><span data-stu-id="0c553-111">Prior to Windows 7, applications should use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function instead.</span></span>

 

<span data-ttu-id="0c553-112">Questa funzione accetta le informazioni seguenti come input:</span><span class="sxs-lookup"><span data-stu-id="0c553-112">This function takes the following information as input:</span></span>

-   <span data-ttu-id="0c553-113">Categoria di MFT da enumerare, ad esempio decoder video o decodificatore audio.</span><span class="sxs-lookup"><span data-stu-id="0c553-113">The category of MFT to enumerate, such as video decoder or audio decoder.</span></span>
-   <span data-ttu-id="0c553-114">Formato di input o di output per cui trovare una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="0c553-114">An input or output format to match.</span></span>
-   <span data-ttu-id="0c553-115">Flag che specificano condizioni di ricerca aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="0c553-115">Flags that specify additional search conditions.</span></span>

<span data-ttu-id="0c553-116">La funzione restituisce una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , ognuno dei quali rappresenta un MFT che corrisponde ai criteri di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="0c553-116">The function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each of which represents an MFT that matches the enumeration criteria.</span></span>

<span data-ttu-id="0c553-117">Il codice seguente, ad esempio, enumera Windows Media Video i decodificatori:</span><span class="sxs-lookup"><span data-stu-id="0c553-117">For example, the following code enumerates Windows Media Video decoders:</span></span>


```C++
HRESULT hr = S_OK;
UINT32 count = 0;

IMFActivate **ppActivate = NULL;    // Array of activation objects.
IMFTransform *pDecoder = NULL;      // Pointer to the decoder.

// Match WMV3 video.
MFT_REGISTER_TYPE_INFO info = { MFMediaType_Video, MFVideoFormat_WMV3 };

UINT32 unFlags = MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;

hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );


if (SUCCEEDED(hr) && count == 0)
{
    hr = MF_E_TOPO_CODEC_NOT_FOUND;
}

// Create the first decoder in the list.

if (SUCCEEDED(hr))
{
    hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(&pDecoder));
}

for (UINT32 i = 0; i < count; i++)
{
    ppActivate[i]->Release();
}
CoTaskMemFree(ppActivate);
```



<span data-ttu-id="0c553-118">Per impostazione predefinita, alcuni tipi di MFT sono esclusi dall'enumerazione, tra cui MFTs asincrono, hardware MFTs e MFTs con ristruct di campo di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="0c553-118">By default, some types of MFT are excluded from the enumeration, including asynchronous MFTs, hardware MFTs, and MFTs with field-of-use restructions.</span></span> <span data-ttu-id="0c553-119">Questi sono esclusi perché tutti richiedono una gestione speciale di qualche tipo.</span><span class="sxs-lookup"><span data-stu-id="0c553-119">These are excluded because they all require special handling of some kind.</span></span> <span data-ttu-id="0c553-120">Usare il parametro *Flags* di [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) per modificare il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0c553-120">Use the *Flags* parameter of [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) to change the default.</span></span> <span data-ttu-id="0c553-121">Per includere, ad esempio, MFTs hardware nei risultati dell'enumerazione, impostare il flag di enumerazione **MFT \_ \_ flag \_ hardware** :</span><span class="sxs-lookup"><span data-stu-id="0c553-121">For example, to include hardware MFTs in the enumeration results, set the **MFT\_ENUM\_FLAG\_HARDWARE** flag:</span></span>


```C++
UINT32 unFlags = MFT_ENUM_FLAG_HARDWARE |
                 MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;
hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );
```



## <a name="registering-mfts"></a><span data-ttu-id="0c553-122">Registrazione di MFTs</span><span class="sxs-lookup"><span data-stu-id="0c553-122">Registering MFTs</span></span>

<span data-ttu-id="0c553-123">Quando si registra un Media Foundation Transform (MFT), due tipi di informazioni vengono scritti nel registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="0c553-123">When you register a Media Foundation transform (MFT), two types of information are written to the registry:</span></span>

-   <span data-ttu-id="0c553-124">Il CLSID di MFT, in modo che i client possano chiamare **CoCreateInstance** o **CoGetClassObject** per creare un'istanza del MFT.</span><span class="sxs-lookup"><span data-stu-id="0c553-124">The CLSID of the MFT, so that clients can call **CoCreateInstance** or **CoGetClassObject** to create an instance of the MFT.</span></span> <span data-ttu-id="0c553-125">Questa voce del registro di sistema segue il formato standard per le class factory COM.</span><span class="sxs-lookup"><span data-stu-id="0c553-125">This registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="0c553-126">Per ulteriori informazioni, vedere la documentazione di Windows SDK per il Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="0c553-126">For more information, see the Windows SDK documentation for the Component Object Model (COM).</span></span>
-   <span data-ttu-id="0c553-127">Informazioni che consentono a un'applicazione di enumerare MFTs per categoria funzionale.</span><span class="sxs-lookup"><span data-stu-id="0c553-127">Information that enables an application to enumerate MFTs by functional category.</span></span>

<span data-ttu-id="0c553-128">Per creare le voci di enumerazione MFT nel registro di sistema, chiamare la funzione [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) .</span><span class="sxs-lookup"><span data-stu-id="0c553-128">To create the MFT enumeration entries in the registry, call the [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) function.</span></span> <span data-ttu-id="0c553-129">È possibile includere le informazioni seguenti relative a MFT:</span><span class="sxs-lookup"><span data-stu-id="0c553-129">You can include the following information about the MFT:</span></span>

-   <span data-ttu-id="0c553-130">Categoria di MFT, ad esempio decoder video o codificatore video.</span><span class="sxs-lookup"><span data-stu-id="0c553-130">The category of the MFT, such as video decoder or video encoder.</span></span> <span data-ttu-id="0c553-131">Per un elenco di categorie, vedere [**la \_ categoria MFT**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="0c553-131">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>
-   <span data-ttu-id="0c553-132">Elenco di formati di input e di output supportati dal MFT.</span><span class="sxs-lookup"><span data-stu-id="0c553-132">A list of input and output formats that the MFT supports.</span></span> <span data-ttu-id="0c553-133">Ogni formato è definito da un tipo principale e da un sottotipo.</span><span class="sxs-lookup"><span data-stu-id="0c553-133">Each format is defined by a major type and a subtype.</span></span> <span data-ttu-id="0c553-134">Per ottenere informazioni più dettagliate sul formato, il client deve creare il MFT e chiamare i metodi [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Il caricatore della topologia utilizza queste informazioni quando risolve una topologia parziale.</span><span class="sxs-lookup"><span data-stu-id="0c553-134">(To get more detailed format information, the client must create the MFT and call [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods.) The topology loader uses this information when it resolves a partial topology.</span></span>

<span data-ttu-id="0c553-135">Per rimuovere le voci dal registro di sistema, chiamare [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span><span class="sxs-lookup"><span data-stu-id="0c553-135">To remove the entries from the registry, call [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span></span>

<span data-ttu-id="0c553-136">Il codice seguente illustra come registrare un MFT.</span><span class="sxs-lookup"><span data-stu-id="0c553-136">The following code shows how to register an MFT.</span></span> <span data-ttu-id="0c553-137">Questo esempio si basa sul presupposto che il MFT sia un effetto video che supporta gli stessi formati sia per l'input che per l'output.</span><span class="sxs-lookup"><span data-stu-id="0c553-137">This example assumes that the MFT is a video effect that supports the same formats for both input and output.</span></span>


```C++
// CLSID of the MFT.
extern const GUID CLSID_MyVideoEffectMFT;

// DllRegisterServer: Creates the registry entries.
STDAPI DllRegisterServer()
{
    HRESULT hr = S_OK;

    // Array of media types.
    MFT_REGISTER_TYPE_INFO aMediaTypes[] =
    {
        {   MFMediaType_Video, MFVideoFormat_NV12 },
        {   MFMediaType_Video, MFVideoFormat_YUY2 },
        {   MFMediaType_Video, MFVideoFormat_UYVY },
    };

    // Size of the array.
    const DWORD cNumMediaTypes = ARRAY_SIZE(aMediaTypes);

    hr = MFTRegister(
        CLSID_MyVideoEffectMFT,     // CLSID.
        MFT_CATEGORY_VIDEO_EFFECT,  // Category.
        L"My Video Effect",         // Friendly name.
        0,                          // Reserved, must be zero.
        cNumMediaTypes,             // Number of input types.
        aMediaTypes,                // Input types.
        cNumMediaTypes,             // Number of output types.
        aMediaTypes,                // Output types.
        NULL                        // Attributes (optional).
        );

    if (SUCCEEDED(hr))
    {
        // Register the CLSID for CoCreateInstance (not shown).
    }
    return hr;
}

// DllUnregisterServer: Removes the registry entries.
STDAPI DllUnregisterServer()
{
    HRESULT hr = MFTUnregister(CLSID_MyVideoEffectMFT);

    // Unregister the CLSID for CoCreateInstance (not shown).

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="0c553-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c553-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c553-139">Limitazioni per l'utilizzo dei campi</span><span class="sxs-lookup"><span data-stu-id="0c553-139">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="0c553-140">Trasformazioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c553-140">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 



