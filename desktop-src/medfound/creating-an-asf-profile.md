---
description: In questo argomento viene descritto come creare un profilo ASF in Microsoft Media Foundation.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Creazione di un profilo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ed9553811645b8589de7fb1805f1a307c4bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305467"
---
# <a name="creating-an-asf-profile"></a>Creazione di un profilo ASF

In questo argomento viene descritto come creare un profilo ASF in Microsoft Media Foundation.

-   [Crea un nuovo profilo](#create-a-new-profile)
-   [Ottenere il profilo dall'oggetto ContentInfo ASF](#get-the-profile-from-the-asf-contentinfo-object)
-   [Ottenere il profilo da un descrittore di presentazione](#get-the-profile-from-a-presentation-descriptor)
-   [Argomenti correlati](#related-topics)

## <a name="create-a-new-profile"></a>Crea un nuovo profilo

Per creare un profilo ASF vuoto, chiamare la funzione [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) . Questa funzione restituisce un puntatore all'interfaccia [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) . L'applicazione può usare questa interfaccia per aggiungere flussi al profilo e per configurare ognuno dei flussi. Per ulteriori informazioni, vedere [creazione e configurazione di flussi ASF](creating-and-configuring-asf-streams.md).

Facoltativamente, l'applicazione può aggiungere oggetti di esclusione reciproca a due o più flussi. Vedere [uso dell'esclusione reciproca per i flussi ASF](using-mutual-exclusion-for-asf-streams.md).

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a>Ottenere il profilo dall'oggetto ContentInfo ASF

Un'applicazione può ottenere il profilo ASF di un file ASF esistente dall' [oggetto ContentInfo ASF](asf-contentinfo-object.md). Il profilo è già configurato e contiene le impostazioni per tutti i flussi nel file.

Inizializzare l'oggetto ContentInfo analizzando l'oggetto intestazione ASF del file. Questa operazione viene eseguita tramite il metodo [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) . Una volta letti tutti gli oggetti intestazione e la libreria ASF viene popolata, viene generato il profilo per il file. L'applicazione può ottenere un puntatore a questo profilo inizializzato chiamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).

## <a name="get-the-profile-from-a-presentation-descriptor"></a>Ottenere il profilo da un descrittore di presentazione

È possibile ottenere l'oggetto profilo di un file ASF esistente dal [descrittore di presentazione](presentation-descriptors.md) per il file o dall'oggetto [ContentInfo di ASF](asf-contentinfo-object.md) . In questo caso, il profilo è già configurato e contiene le impostazioni per tutti i flussi del file. Questa operazione può essere utile se si desidera modificare un profilo ASF esistente. Ad esempio, potrebbe essere necessario codificare nuovamente un file di Windows Media Video a una velocità in bit inferiore.

Per ottenere il profilo dal descrittore della presentazione, chiamare [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor). Questa funzione analizza il descrittore di presentazione e popola un profilo ASF con le informazioni sul file multimediale. La funzione restituisce un puntatore all'interfaccia IMFASFProfile. È quindi possibile usare questa interfaccia per modificare il profilo.

Per ottenere il descrittore della presentazione, chiamare uno dei metodi seguenti:

-   Dall'origine dei supporti ASF, chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   Dall'oggetto [ContentInfo di ASF](asf-contentinfo-object.md) , chiamare [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Prima di chiamare questo metodo, assicurarsi che l'oggetto ContentInfo venga inizializzato per la lettura. Per ulteriori informazioni, vedere "inizializzazione dell'oggetto ContentInfo da un file ASF esistente" durante [la lettura dell'oggetto intestazione ASF di un file esistente](reading-the-asf-header-object-of-an-existing-file.md). Tuttavia, se si dispone già di un oggetto ContentInfo inizializzato, è possibile ottenere il profilo direttamente da tale oggetto. Questa operazione è descritta in "recupero del profilo dall'oggetto ContentInfo" più avanti in questo argomento.

Nell'esempio seguente viene illustrato come creare un profilo da un descrittore di presentazione. La funzione crea un'origine multimediale per il file, ottiene il descrittore di presentazione dall'origine multimediale e crea un profilo. In questo esempio si presuppone che *pszFileName* specifichi l'URL di un file ASF.


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



Questo esempio usa [SafeRelease](saferelease.md) per rilasciare i puntatori all'interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Profilo ASF](asf-profile.md)
</dt> </dl>

 

 



