---
description: Questo argomento descrive come creare un profilo ASF in Microsoft Media Foundation.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Creazione di un profilo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a0225a6ff17f68c5443fce15f9bdc196901313ccaaebdde2f7f34c49860538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743248"
---
# <a name="creating-an-asf-profile"></a>Creazione di un profilo ASF

Questo argomento descrive come creare un profilo ASF in Microsoft Media Foundation.

-   [Creare un nuovo profilo](#create-a-new-profile)
-   [Ottenere il profilo dall'oggetto ContentInfo di ASF](#get-the-profile-from-the-asf-contentinfo-object)
-   [Ottenere il profilo da un descrittore di presentazione](#get-the-profile-from-a-presentation-descriptor)
-   [Argomenti correlati](#related-topics)

## <a name="create-a-new-profile"></a>Creare un nuovo profilo

Per creare un profilo ASF vuoto, chiamare la [**funzione MFCreateASFProfile.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) Questa funzione restituisce un puntatore [**all'interfaccia IMFASFProfile.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) L'applicazione può usare questa interfaccia per aggiungere flussi al profilo e per configurare ognuno dei flussi. Per altre informazioni, vedere [Creating and Configuring ASF Flussi](creating-and-configuring-asf-streams.md).

Facoltativamente, l'applicazione può aggiungere oggetti a esclusione reciproca a due o più flussi. Vedere [Uso dell'esclusione reciproca per ASF Flussi](using-mutual-exclusion-for-asf-streams.md).

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a>Ottenere il profilo dall'oggetto ContentInfo di ASF

Un'applicazione può ottenere il profilo ASF di un file ASF esistente [dall'oggetto ContentInfo di ASF.](asf-contentinfo-object.md) Il profilo è già configurato e contiene le impostazioni per tutti i flussi nel file.

Inizializzare l'oggetto ContentInfo analizzando l'oggetto intestazione ASF del file. Questa operazione viene eseguita tramite [**il metodo IMFASFContentInfo::P arseHeader.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) Dopo aver letto tutti gli oggetti intestazione e aver popolato la libreria ASF, viene generato il profilo per questo file. L'applicazione può ottenere un puntatore a questo profilo inizializzato chiamando [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).

## <a name="get-the-profile-from-a-presentation-descriptor"></a>Ottenere il profilo da un descrittore di presentazione

È possibile ottenere l'oggetto profilo di [](presentation-descriptors.md) un file ASF esistente dal descrittore di presentazione per il file o dall'oggetto [ContentInfo di ASF.](asf-contentinfo-object.md) In questo caso, il profilo è già configurato e contiene le impostazioni per tutti i flussi nel file. Ciò può essere utile se si vuole modificare un profilo ASF esistente. Ad esempio, potrebbe essere necessario ricodificare un file Windows Media Video a una velocità in bit inferiore.

Per ottenere il profilo dal descrittore di presentazione, chiamare [**MFCreateASFProfileFromPresentationDescriptor.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) Questa funzione analizza il descrittore di presentazione e popola un profilo ASF con informazioni sul file multimediale. La funzione restituisce un puntatore all'interfaccia IMFASFProfile. È quindi possibile usare questa interfaccia per modificare il profilo.

Per ottenere il descrittore di presentazione, chiamare uno dei metodi seguenti:

-   Dall'origine multimediale ASF chiamare [**IMFMediaSource::CreatePresentationDescriptor.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)
-   [Dall'oggetto ContentInfo](asf-contentinfo-object.md) di ASF chiamare [**IMFASFContentInfo::GeneratePresentationDescriptor.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) Prima di chiamare questo metodo, assicurarsi che l'oggetto ContentInfo sia inizializzato per la lettura. Per altre informazioni, vedere "Inizializzazione dell'oggetto ContentInfo da un file ASF esistente" in Lettura dell'oggetto intestazione [ASF di un file esistente.](reading-the-asf-header-object-of-an-existing-file.md) Tuttavia, se si dispone già di un oggetto ContentInfo inizializzato, è possibile ottenere il profilo direttamente da esso. Questa operazione è descritta in "Recupero del profilo dall'oggetto ContentInfo" più avanti in questo argomento.

Nell'esempio seguente viene illustrato come creare un profilo da un descrittore di presentazione. La funzione crea un'origine multimediale per il file, ottiene il descrittore di presentazione dall'origine multimediale e crea un profilo. Questo esempio presuppone che *pszFileName specifichi* l'URL di un file ASF.


```C++
HRESULT GetASFProfile(PCWSTR pszFileName, IMFASFProfile** ppProfile)
{
    *ppProfile = NULL;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSourceUnk = NULL;
    IMFMediaSource* pSource = NULL;
    IMFPresentationDescriptor* pPD = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        hr = pResolver->CreateObjectFromURL(
                pszFileName,
                MF_RESOLUTION_MEDIASOURCE, 
                NULL,                      
                &ObjectType,               
                &pSourceUnk   
            );
    }

    // Get the IMFMediaSource interface from the media source.
    if (SUCCEEDED(hr))
    {
        hr = pSourceUnk->QueryInterface(IID_PPV_ARGS(&pSource));
    }

    // Get the presentation desccriptor.
    if (SUCCEEDED(hr))
    {
        hr = pSource->CreatePresentationDescriptor(&pPD);
    }

    // Get the profile from the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFProfileFromPresentationDescriptor(pPD, ppProfile);
    }

    SafeRelease(&pResolver);
    SafeRelease(&pSourceUnk);
    SafeRelease(&pSource);
    SafeRelease(&pPD);
    return hr;
}
```



Questo esempio usa [SafeRelease per rilasciare](saferelease.md) i puntatori a interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Profilo ASF](asf-profile.md)
</dt> </dl>

 

 



