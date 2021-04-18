---
title: Uso dell'esclusione reciproca a più bit rate
description: Uso dell'esclusione reciproca a più bit rate
ms.assetid: 69898b4d-fe10-422e-9ed2-87b65aa7bdb3
keywords:
- velocità in bit multipla (MBR), esclusione reciproca
- MBR (frequenza a più bit), esclusione reciproca
- esclusione reciproca, velocità in bit multipla (MBR)
- profili, velocità in bit multipla (MBR)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77c7615845d10d07982676dfdb4dc8c617cebe
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336258"
---
# <a name="using-multiple-bit-rate-mutual-exclusion"></a><span data-ttu-id="f201e-107">Uso dell'esclusione reciproca a più bit rate</span><span class="sxs-lookup"><span data-stu-id="f201e-107">Using Multiple Bit Rate Mutual Exclusion</span></span>

<span data-ttu-id="f201e-108">L'esclusione reciproca a più velocità in bit (MBR) è utile quando si desidera codificare il contenuto per diversi scenari di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="f201e-108">Multiple bit rate (MBR) mutual exclusion is useful when you want to encode content for a variety of playback scenarios.</span></span> <span data-ttu-id="f201e-109">Un output video MBR è costituito da un singolo input codificato più volte, ognuno con diverse impostazioni della velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="f201e-109">An MBR video output consists of a single input encoded multiple times, each with different bit-rate settings.</span></span> <span data-ttu-id="f201e-110">Quando viene letto un file con codifica MBR, il lettore determinerà il flusso da usare in base alla larghezza di banda disponibile.</span><span class="sxs-lookup"><span data-stu-id="f201e-110">When a file with MBR encoding is read, the reader will determine which stream to use based on the available bandwidth.</span></span>

<span data-ttu-id="f201e-111">Windows Media Format SDK supporta la codifica MBR per i flussi video e audio.</span><span class="sxs-lookup"><span data-stu-id="f201e-111">The Windows Media Format SDK supports MBR encoding for both video and audio streams.</span></span> <span data-ttu-id="f201e-112">Inoltre, è possibile creare un tipo speciale di codifica MBR denominata codifica MBR a più video.</span><span class="sxs-lookup"><span data-stu-id="f201e-112">In addition, you can create a special type of MBR encoding called multiple-video-size MBR encoding.</span></span> <span data-ttu-id="f201e-113">Il video MBR a più dimensioni video è identico a quello dei video MBR normali, tranne per il fatto che è possibile specificare dimensioni di immagine diverse per i flussi video nell'esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="f201e-113">Multiple-video-size MBR video functions identically to normal MBR video except that you can specify different image sizes for the video streams in the mutual exclusion.</span></span>

<span data-ttu-id="f201e-114">L'esempio seguente illustra come configurare un profilo per video MBR con più dimensioni del video.</span><span class="sxs-lookup"><span data-stu-id="f201e-114">The following example demonstrates how to set up a profile for MBR video with multiple video sizes.</span></span> <span data-ttu-id="f201e-115">Viene creato un nuovo profilo con tre flussi video di dimensioni e velocità in bit variabili e inclusi in un oggetto di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="f201e-115">It creates a new profile with three video streams of varying bit rates and sizes, and includes them in a mutual exclusion object.</span></span>


```C++
IWMProfileManager*  pProfileMgr = NULL;
IWMProfile*         pProfile    = NULL;
IWMMutualExclusion* pMutex      = NULL;
IWMStreamConfig*    pStream     = NULL;
IWMMediaProps*      pMediaProps = NULL;

WM_MEDIA_TYPE*      pMediaType  = NULL;
DWORD               cbMediaType = 0;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfile);

// Give the new profile a name and description.
hr = pProfile->SetName(L"MBR_Video_3_Stream_test");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// Get the media properties interface for the new stream.
hr = pStream->QueryInterface(IID_IWMMediaProps, (void**)&pMediaProps);

// Get the media-type structure.
// First, get the size of the media-type structure.
hr = pMediaProps->GetMediaType(NULL, &cbMediaType);

// Allocate memory for the structure based on the retrieved size.
pMediaType = (WM_MEDIA_TYPE*) new BYTE[cbMediaType];

// Retrieve the media-type structure.
hr = pMediaProps->GetMediaType(pMediaType, &cbMediaType);

// Change the video size to 640 x 480.
pMediaType->pbFormat->bmiHeader.biWidth  = 640;
pMediaType->pbFormat->bmiHeader.biHeight = 480;

// Replace the WM_MEDIA_TYPE in the profile with the one just changed.
hr = pMediaProps->SetMediaType(pMediaType);

// Release the media properties interface and delete the structure.
pMediaProps->Release();
pMediaProps = NULL;
delete[] pMediaType;
pMediaType = NULL;

// Set the bit rate to 200.
hr = pStream->SetBitrate(200000);

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// For the remaining two streams, leave the video at its default size of
// 320 x 240 <entity type="ndash"/>- just change the bit rates.

// Repeat for a 100K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(100000);
hr = pStream->SetStreamNumber(2);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Repeat for a 56K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(56000);
hr = pStream->SetStreamNumber(3);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Now that we have three streams, create a mutual exclusion object.
hr = pProfile->CreateNewMutualExclusion(&pMutex);

// Add the three streams to the mutual exclusion.
hr = pMutex->AddStream(1);
hr = pMutex->AddStream(2);
hr = pMutex->AddStream(3);

// Configure the mutual exclusion for MBR video.
hr = pMutex->SetType(CLSID_WMMUTEX_Bitrate);

// Add the mutual exclusion to the profile.
hr = pProfile->AddMutualExclusion(pMutex);

// Release the mutual exclusion object.
pMutex->Release();
pMutex = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a><span data-ttu-id="f201e-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f201e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f201e-117">**Interfaccia IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="f201e-117">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="f201e-118">**Interfaccia IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="f201e-118">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="f201e-119">**Interfaccia IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="f201e-119">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="f201e-120">**Interfaccia IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="f201e-120">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[<span data-ttu-id="f201e-121">**Uso dell'esclusione reciproca**</span><span class="sxs-lookup"><span data-stu-id="f201e-121">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="f201e-122">**\_tipo di supporto WM \_**</span><span class="sxs-lookup"><span data-stu-id="f201e-122">**WM\_MEDIA\_TYPE**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)
</dt> </dl>

 

 




