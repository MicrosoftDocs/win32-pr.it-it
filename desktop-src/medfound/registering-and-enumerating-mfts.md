---
description: In questa sezione viene descritto come enumerare Media Foundation e come registrare un MFT personalizzato in modo che le applicazioni possano individuarlo.
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: Registrazione ed enumerazione di MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3110351479f2a906d68b6c054d9e23886cbcd4cdb031fc8a4951a1d4b8d1e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101830"
---
# <a name="registering-and-enumerating-mfts"></a>Registrazione ed enumerazione di MFT

In questa sezione viene descritto come enumerare Media Foundation e come registrare un MFT personalizzato in modo che le applicazioni possano individuarlo.

-   [Enumerazione di MFT](#registering-and-enumerating-mfts)
-   [Registrazione di MFT](#registering-mfts)
-   [Argomenti correlati](#related-topics)

## <a name="enumerating-mfts"></a>Enumerazione di MFT

Per individuare i MFT registrati nel sistema, un'applicazione può chiamare la [**funzione MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

> [!Note]  
> Questa funzione richiede l'Windows 7. Prima di Windows 7, le applicazioni devono usare invece la [**funzione MFTEnum.**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)

 

Questa funzione accetta le informazioni seguenti come input:

-   Categoria di MFT da enumerare, ad esempio decodificatore video o decodificatore audio.
-   Formato di input o output di cui trovare una corrispondenza.
-   Flag che specificano condizioni di ricerca aggiuntive.

La funzione restituisce una matrice di [**puntatori IMFActivate,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ognuno dei quali rappresenta un MFT che corrisponde ai criteri di enumerazione.

Ad esempio, il codice seguente enumera Windows decodificatori Media Video:


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



Per impostazione predefinita, alcuni tipi di MFT sono esclusi dall'enumerazione, tra cui MFT asincroni, MFT hardware e MFT con le strutture field-of-use. Questi elementi sono esclusi perché richiedono una gestione speciale di qualche tipo. Usare il *parametro Flags* di [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) per modificare l'impostazione predefinita. Ad esempio, per includere MFT hardware nei risultati dell'enumerazione, impostare il flag **HARDWARE MFT \_ ENUM \_ FLAG: \_**


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



## <a name="registering-mfts"></a>Registrazione di MFT

Quando si registra una trasformazione Media Foundation (MFT), nel Registro di sistema vengono scritti due tipi di informazioni:

-   CLSID del MFT, in modo che i client possano chiamare **CoCreateInstance** o **CoGetClassObject** per creare un'istanza del MFT. Questa voce del Registro di sistema segue il formato standard per le class factory COM. Per altre informazioni, vedere la documentazione Windows SDK per Component Object Model (COM).
-   Informazioni che consentono a un'applicazione di enumerare MFT per categoria funzionale.

Per creare le voci di enumerazione MFT nel Registro di sistema, chiamare la [**funzione MFTRegister.**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) È possibile includere le informazioni seguenti sul MFT:

-   Categoria del MFT, ad esempio decodificatore video o codificatore video. Per un elenco di categorie, vedere [**MFT \_ CATEGORY.**](mft-category.md)
-   Elenco di formati di input e output supportati da MFT. Ogni formato è definito da un tipo principale e da un sottotipo. Per ottenere informazioni più dettagliate sul formato, il client deve creare MFT e chiamare [**i metodi IMFTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) Il caricatore della topologia usa queste informazioni quando risolve una topologia parziale.

Per rimuovere le voci dal Registro di sistema, chiamare [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).

Nel codice seguente viene illustrato come registrare un MFT. In questo esempio si presuppone che MFT sia un effetto video che supporta gli stessi formati sia per l'input che per l'output.


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

[Restrizioni sul campo di utilizzo](field-of-use-restrictions.md)
</dt> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> </dl>

 

 



