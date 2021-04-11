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
# <a name="registering-and-enumerating-mfts"></a>Registrazione ed enumerazione di MFTs

In questa sezione viene descritto come enumerare Media Foundation trasformazioni e come registrare un MFT personalizzato in modo che le applicazioni possano individuarlo.

-   [Enumerazione di MFTs](#registering-and-enumerating-mfts)
-   [Registrazione di MFTs](#registering-mfts)
-   [Argomenti correlati](#related-topics)

## <a name="enumerating-mfts"></a>Enumerazione di MFTs

Per individuare MFTs registrate nel sistema, un'applicazione può chiamare la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

> [!Note]  
> Questa funzione richiede Windows 7. Prima di Windows 7, le applicazioni devono invece usare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .

 

Questa funzione accetta le informazioni seguenti come input:

-   Categoria di MFT da enumerare, ad esempio decoder video o decodificatore audio.
-   Formato di input o di output per cui trovare una corrispondenza.
-   Flag che specificano condizioni di ricerca aggiuntive.

La funzione restituisce una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , ognuno dei quali rappresenta un MFT che corrisponde ai criteri di enumerazione.

Il codice seguente, ad esempio, enumera Windows Media Video i decodificatori:


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



Per impostazione predefinita, alcuni tipi di MFT sono esclusi dall'enumerazione, tra cui MFTs asincrono, hardware MFTs e MFTs con ristruct di campo di utilizzo. Questi sono esclusi perché tutti richiedono una gestione speciale di qualche tipo. Usare il parametro *Flags* di [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) per modificare il valore predefinito. Per includere, ad esempio, MFTs hardware nei risultati dell'enumerazione, impostare il flag di enumerazione **MFT \_ \_ flag \_ hardware** :


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



## <a name="registering-mfts"></a>Registrazione di MFTs

Quando si registra un Media Foundation Transform (MFT), due tipi di informazioni vengono scritti nel registro di sistema:

-   Il CLSID di MFT, in modo che i client possano chiamare **CoCreateInstance** o **CoGetClassObject** per creare un'istanza del MFT. Questa voce del registro di sistema segue il formato standard per le class factory COM. Per ulteriori informazioni, vedere la documentazione di Windows SDK per il Component Object Model (COM).
-   Informazioni che consentono a un'applicazione di enumerare MFTs per categoria funzionale.

Per creare le voci di enumerazione MFT nel registro di sistema, chiamare la funzione [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) . È possibile includere le informazioni seguenti relative a MFT:

-   Categoria di MFT, ad esempio decoder video o codificatore video. Per un elenco di categorie, vedere [**la \_ categoria MFT**](mft-category.md).
-   Elenco di formati di input e di output supportati dal MFT. Ogni formato è definito da un tipo principale e da un sottotipo. Per ottenere informazioni più dettagliate sul formato, il client deve creare il MFT e chiamare i metodi [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Il caricatore della topologia utilizza queste informazioni quando risolve una topologia parziale.

Per rimuovere le voci dal registro di sistema, chiamare [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).

Il codice seguente illustra come registrare un MFT. Questo esempio si basa sul presupposto che il MFT sia un effetto video che supporta gli stessi formati sia per l'input che per l'output.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limitazioni per l'utilizzo dei campi](field-of-use-restrictions.md)
</dt> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



