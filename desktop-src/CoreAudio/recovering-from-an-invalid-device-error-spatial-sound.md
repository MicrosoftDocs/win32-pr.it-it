---
description: Ripristino da un errore di Invalid-Device (audio spaziale)
title: Ripristino da un errore di Invalid-Device (audio spaziale)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127423"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a><span data-ttu-id="8504a-103">Ripristino da un errore di Invalid-Device (audio spaziale)</span><span class="sxs-lookup"><span data-stu-id="8504a-103">Recovering from an Invalid-Device Error (Spatial Sound)</span></span>

<span data-ttu-id="8504a-104">Molti dei metodi dell'API Microsoft spatial audio, ad esempio [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)e [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), restituiscono i codici di errore se il dispositivo dell'endpoint audio utilizzato dall'applicazione client diventa non valido o il formato di rendering dell'audio spaziale viene modificato nell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="8504a-104">Many of the methods of the Microsoft Spatial Audio API, such as [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream), and [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), return error codes if the audio endpoint device that the client application is using becomes invalid or the spatial audio rendering format is changed on the endpoint.</span></span> <span data-ttu-id="8504a-105">Questi codici di errore indicano che il dispositivo endpoint è stato scollegato o che l'hardware audio o le risorse hardware associate sono state riconfigurate, disabilitate, rimosse, la modalità audio spaziale viene modificata o non è disponibile per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="8504a-105">These error codes indicates that the endpoint device has been unplugged, or that the audio hardware or associated hardware resources have been reconfigured, disabled, removed, spatial audio mode is changed or otherwise made unavailable for use.</span></span> <span data-ttu-id="8504a-106">Spesso l'applicazione può risolvere questo errore.</span><span class="sxs-lookup"><span data-stu-id="8504a-106">Frequently, the application can recover from this error.</span></span>

<span data-ttu-id="8504a-107">I codici di errore che indicano un errore di dispositivo non valido includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8504a-107">Error codes that indicate an invalid-device error include the following:</span></span>

- <span data-ttu-id="8504a-108">SPTLAUDCLNT_E_DESTROYED</span><span class="sxs-lookup"><span data-stu-id="8504a-108">SPTLAUDCLNT_E_DESTROYED</span></span>
- <span data-ttu-id="8504a-109">AUDCLNT_E_DEVICE_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="8504a-109">AUDCLNT_E_DEVICE_INVALIDATED</span></span>
- <span data-ttu-id="8504a-110">AUDCLNT_E_RESOURCES_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="8504a-110">AUDCLNT_E_RESOURCES_INVALIDATED</span></span>
- <span data-ttu-id="8504a-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span><span class="sxs-lookup"><span data-stu-id="8504a-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span></span>
- <span data-ttu-id="8504a-112">SPTLAUDCLNT_E_INTERNAL</span><span class="sxs-lookup"><span data-stu-id="8504a-112">SPTLAUDCLNT_E_INTERNAL</span></span>

## <a name="strategies-for-handling-invalid-device-errors"></a><span data-ttu-id="8504a-113">Strategie per la gestione di errori di dispositivo non valido</span><span class="sxs-lookup"><span data-stu-id="8504a-113">Strategies for handling invalid-device errors</span></span>

<span data-ttu-id="8504a-114">La strategia consigliata per il ripristino da un errore di dispositivo non valido dipende dal fatto che l'applicazione selezioni automaticamente un dispositivo specifico in base ai requisiti interni o che consenta all'utente di selezionare in modo esplicito un dispositivo da un elenco di dispositivi disponibili.</span><span class="sxs-lookup"><span data-stu-id="8504a-114">The recommended strategy for recovering from an invalid-device error depends on whether the application automatically selects a specific device based on internal requirements or it allows the user to explicitly select a device from a list of available devices.</span></span> 

### <a name="default-audio-device"></a><span data-ttu-id="8504a-115">Dispositivo audio predefinito</span><span class="sxs-lookup"><span data-stu-id="8504a-115">Default audio device</span></span>

<span data-ttu-id="8504a-116">Se l'applicazione seleziona automaticamente il dispositivo predefinito, attenersi alla procedura seguente per eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="8504a-116">If the application automatically selects the default device, use the following steps to recover.</span></span>

1. <span data-ttu-id="8504a-117">Rilasciare l'interfaccia [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) e [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) e tutte le altre interfacce audio spaziali utilizzate per il rendering.</span><span class="sxs-lookup"><span data-stu-id="8504a-117">Release the [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) and [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interface and any other spatial audio interfaces that are used for rendering.</span></span> 
1. <span data-ttu-id="8504a-118">Chiamare [IMMDeviceEnumerator:: GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere il dispositivo audio predefinito corrente.</span><span class="sxs-lookup"><span data-stu-id="8504a-118">Call [IMMDeviceEnumerator::GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the current default audio device.</span></span>
1. <span data-ttu-id="8504a-119">Tentativo di attivare **ISpatialAudioClient** sul dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="8504a-119">Attempt to activate **ISpatialAudioClient** on the audio device.</span></span>
1. <span data-ttu-id="8504a-120">Attivare **ISpatialAudioObjectRenderStream**.</span><span class="sxs-lookup"><span data-stu-id="8504a-120">Activate **ISpatialAudioObjectRenderStream**.</span></span> 

### <a name="specifically-selected-audio-device"></a><span data-ttu-id="8504a-121">Dispositivo audio selezionato in modo specifico</span><span class="sxs-lookup"><span data-stu-id="8504a-121">Specifically selected audio device</span></span>

<span data-ttu-id="8504a-122">Se l'applicazione seleziona un dispositivo audio specifico, attenersi alla procedura seguente per eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="8504a-122">If the application selects a specific audio device, use the following steps to recover.</span></span>

1. <span data-ttu-id="8504a-123">Rilasciare l'interfaccia ISpatialAudioObjectRenderStream e tutte le altre interfacce audio spaziali usate per il rendering, ma non rilasciare **ISpatialAudioClient**.</span><span class="sxs-lookup"><span data-stu-id="8504a-123">Release the ISpatialAudioObjectRenderStream interface and any other spatial audio interfaces that are used for rendering, but don't release **ISpatialAudioClient**.</span></span>
1. <span data-ttu-id="8504a-124">Usare l'istanza corrente di **ISpatialAudioClient** per attivare **ISpatialAudioObjectRenderStream**.</span><span class="sxs-lookup"><span data-stu-id="8504a-124">Use the current **ISpatialAudioClient** instance to activate **ISpatialAudioObjectRenderStream**.</span></span>

<span data-ttu-id="8504a-125">Si noti che per entrambe le strategie elencate in precedenza, è possibile applicare gli stessi passaggi alle applicazioni che usano le interfacce [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) o [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) .</span><span class="sxs-lookup"><span data-stu-id="8504a-125">Note that for both strategies listed above, the same steps can be applied to applications that use the [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) or [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) interfaces.</span></span> <span data-ttu-id="8504a-126">È sufficiente sostituire **ISpatialAudioObjectRenderStream** nei passaggi precedenti con le interfacce Metadata o HRTF.</span><span class="sxs-lookup"><span data-stu-id="8504a-126">Simply replace **ISpatialAudioObjectRenderStream** in the above steps with the metadata or Hrtf interfaces.</span></span>


## <a name="related-topics"></a><span data-ttu-id="8504a-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8504a-127">Related topics</span></span>

<dl> <span data-ttu-id="8504a-128"><dt>
[Ripristino da un errore](recovering-from-an-invalid-device-error.md) 
 di Invalid-Device [Gestione dei flussi](stream-management.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="8504a-128"><dt>
[Recovering from an Invalid-Device Error](recovering-from-an-invalid-device-error.md)
[Stream Management](stream-management.md)
</dt> </span></span></dl>

 

 



