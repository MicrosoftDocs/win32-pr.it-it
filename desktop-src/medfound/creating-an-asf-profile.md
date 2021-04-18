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
# <a name="creating-an-asf-profile"></a><span data-ttu-id="7d810-103">Creazione di un profilo ASF</span><span class="sxs-lookup"><span data-stu-id="7d810-103">Creating an ASF Profile</span></span>

<span data-ttu-id="7d810-104">In questo argomento viene descritto come creare un profilo ASF in Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7d810-104">This topic describes how to create as ASF profile in Microsoft Media Foundation.</span></span>

-   [<span data-ttu-id="7d810-105">Crea un nuovo profilo</span><span class="sxs-lookup"><span data-stu-id="7d810-105">Create a New Profile</span></span>](#create-a-new-profile)
-   [<span data-ttu-id="7d810-106">Ottenere il profilo dall'oggetto ContentInfo ASF</span><span class="sxs-lookup"><span data-stu-id="7d810-106">Get the Profile from the ASF ContentInfo Object</span></span>](#get-the-profile-from-the-asf-contentinfo-object)
-   [<span data-ttu-id="7d810-107">Ottenere il profilo da un descrittore di presentazione</span><span class="sxs-lookup"><span data-stu-id="7d810-107">Get the Profile from a Presentation Descriptor</span></span>](#get-the-profile-from-a-presentation-descriptor)
-   [<span data-ttu-id="7d810-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d810-108">Related topics</span></span>](#related-topics)

## <a name="create-a-new-profile"></a><span data-ttu-id="7d810-109">Crea un nuovo profilo</span><span class="sxs-lookup"><span data-stu-id="7d810-109">Create a New Profile</span></span>

<span data-ttu-id="7d810-110">Per creare un profilo ASF vuoto, chiamare la funzione [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="7d810-110">To create an empty ASF profile, call the [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) function.</span></span> <span data-ttu-id="7d810-111">Questa funzione restituisce un puntatore all'interfaccia [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="7d810-111">This function returns a pointer to the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="7d810-112">L'applicazione può usare questa interfaccia per aggiungere flussi al profilo e per configurare ognuno dei flussi.</span><span class="sxs-lookup"><span data-stu-id="7d810-112">The application can use this interface to add streams to the profile, and to configure each of the streams.</span></span> <span data-ttu-id="7d810-113">Per ulteriori informazioni, vedere [creazione e configurazione di flussi ASF](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="7d810-113">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>

<span data-ttu-id="7d810-114">Facoltativamente, l'applicazione può aggiungere oggetti di esclusione reciproca a due o più flussi.</span><span class="sxs-lookup"><span data-stu-id="7d810-114">Optionally, the application can add mutual-exclusion objects to two or more streams.</span></span> <span data-ttu-id="7d810-115">Vedere [uso dell'esclusione reciproca per i flussi ASF](using-mutual-exclusion-for-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="7d810-115">See [Using Mutual Exclusion for ASF Streams](using-mutual-exclusion-for-asf-streams.md).</span></span>

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a><span data-ttu-id="7d810-116">Ottenere il profilo dall'oggetto ContentInfo ASF</span><span class="sxs-lookup"><span data-stu-id="7d810-116">Get the Profile from the ASF ContentInfo Object</span></span>

<span data-ttu-id="7d810-117">Un'applicazione può ottenere il profilo ASF di un file ASF esistente dall' [oggetto ContentInfo ASF](asf-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="7d810-117">An application can get the ASF profile of an existing ASF file from the [ASF ContentInfo Object](asf-contentinfo-object.md).</span></span> <span data-ttu-id="7d810-118">Il profilo è già configurato e contiene le impostazioni per tutti i flussi nel file.</span><span class="sxs-lookup"><span data-stu-id="7d810-118">The profile is already configured and contains settings for the all of the streams in the file.</span></span>

<span data-ttu-id="7d810-119">Inizializzare l'oggetto ContentInfo analizzando l'oggetto intestazione ASF del file.</span><span class="sxs-lookup"><span data-stu-id="7d810-119">Initialize the ContentInfo object by parsing the ASF Header Object of the file.</span></span> <span data-ttu-id="7d810-120">Questa operazione viene eseguita tramite il metodo [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="7d810-120">This is done through the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="7d810-121">Una volta letti tutti gli oggetti intestazione e la libreria ASF viene popolata, viene generato il profilo per il file.</span><span class="sxs-lookup"><span data-stu-id="7d810-121">After all the Header Objects are read and the ASF library is populated, the profile for this file is generated.</span></span> <span data-ttu-id="7d810-122">L'applicazione può ottenere un puntatore a questo profilo inizializzato chiamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="7d810-122">The application can get a pointer to this initialized profile by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>

## <a name="get-the-profile-from-a-presentation-descriptor"></a><span data-ttu-id="7d810-123">Ottenere il profilo da un descrittore di presentazione</span><span class="sxs-lookup"><span data-stu-id="7d810-123">Get the Profile from a Presentation Descriptor</span></span>

<span data-ttu-id="7d810-124">È possibile ottenere l'oggetto profilo di un file ASF esistente dal [descrittore di presentazione](presentation-descriptors.md) per il file o dall'oggetto [ContentInfo di ASF](asf-contentinfo-object.md) .</span><span class="sxs-lookup"><span data-stu-id="7d810-124">You can get the profile object of an existing ASF file from the [presentation descriptor](presentation-descriptors.md) for the file, or from the [ASF ContentInfo](asf-contentinfo-object.md) object.</span></span> <span data-ttu-id="7d810-125">In questo caso, il profilo è già configurato e contiene le impostazioni per tutti i flussi del file.</span><span class="sxs-lookup"><span data-stu-id="7d810-125">In this case, the profile is already configured and contains settings for all of the streams in the file.</span></span> <span data-ttu-id="7d810-126">Questa operazione può essere utile se si desidera modificare un profilo ASF esistente.</span><span class="sxs-lookup"><span data-stu-id="7d810-126">This can be useful if you want to modify an existing ASF profile.</span></span> <span data-ttu-id="7d810-127">Ad esempio, potrebbe essere necessario codificare nuovamente un file di Windows Media Video a una velocità in bit inferiore.</span><span class="sxs-lookup"><span data-stu-id="7d810-127">For example, you might wish to re-encode a Windows Media Video file at a lower bit rate.</span></span>

<span data-ttu-id="7d810-128">Per ottenere il profilo dal descrittore della presentazione, chiamare [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="7d810-128">To get the profile from the presentation descriptor, call [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span></span> <span data-ttu-id="7d810-129">Questa funzione analizza il descrittore di presentazione e popola un profilo ASF con le informazioni sul file multimediale.</span><span class="sxs-lookup"><span data-stu-id="7d810-129">This function parses the presentation descriptor, and populates an ASF profile with information about the media file.</span></span> <span data-ttu-id="7d810-130">La funzione restituisce un puntatore all'interfaccia IMFASFProfile.</span><span class="sxs-lookup"><span data-stu-id="7d810-130">The function returns a pointer to the IMFASFProfile interface.</span></span> <span data-ttu-id="7d810-131">È quindi possibile usare questa interfaccia per modificare il profilo.</span><span class="sxs-lookup"><span data-stu-id="7d810-131">You can then use this interface to modify the profile.</span></span>

<span data-ttu-id="7d810-132">Per ottenere il descrittore della presentazione, chiamare uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7d810-132">To get the presentation descriptor, call one of the following methods:</span></span>

-   <span data-ttu-id="7d810-133">Dall'origine dei supporti ASF, chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="7d810-133">From the ASF media source, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="7d810-134">Dall'oggetto [ContentInfo di ASF](asf-contentinfo-object.md) , chiamare [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="7d810-134">From the [ASF ContentInfo](asf-contentinfo-object.md) object, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="7d810-135">Prima di chiamare questo metodo, assicurarsi che l'oggetto ContentInfo venga inizializzato per la lettura.</span><span class="sxs-lookup"><span data-stu-id="7d810-135">Prior to calling this method, make sure that the ContentInfo object is initialized for reading.</span></span> <span data-ttu-id="7d810-136">Per ulteriori informazioni, vedere "inizializzazione dell'oggetto ContentInfo da un file ASF esistente" durante [la lettura dell'oggetto intestazione ASF di un file esistente](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="7d810-136">For more information, see "Initializing the ContentInfo Object from an Existing ASF File" in [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span> <span data-ttu-id="7d810-137">Tuttavia, se si dispone già di un oggetto ContentInfo inizializzato, è possibile ottenere il profilo direttamente da tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="7d810-137">However, if you already have an initialized ContentInfo object, you can get the profile directly from it.</span></span> <span data-ttu-id="7d810-138">Questa operazione è descritta in "recupero del profilo dall'oggetto ContentInfo" più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="7d810-138">This is described in "Getting the Profile from the ContentInfo Object " later in this topic.</span></span>

<span data-ttu-id="7d810-139">Nell'esempio seguente viene illustrato come creare un profilo da un descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="7d810-139">The following example shows how to create a profile from a presentation descriptor.</span></span> <span data-ttu-id="7d810-140">La funzione crea un'origine multimediale per il file, ottiene il descrittore di presentazione dall'origine multimediale e crea un profilo.</span><span class="sxs-lookup"><span data-stu-id="7d810-140">The function creates a media source for the file, gets the presentation descriptor from the media source, and creates a profile.</span></span> <span data-ttu-id="7d810-141">In questo esempio si presuppone che *pszFileName* specifichi l'URL di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="7d810-141">This example assumes that *pszFileName* specifies the URL of an ASF file.</span></span>


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



<span data-ttu-id="7d810-142">Questo esempio usa [SafeRelease](saferelease.md) per rilasciare i puntatori all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7d810-142">This example uses [SafeRelease](saferelease.md) to release interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d810-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d810-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d810-144">Profilo ASF</span><span class="sxs-lookup"><span data-stu-id="7d810-144">ASF Profile</span></span>](asf-profile.md)
</dt> </dl>

 

 



