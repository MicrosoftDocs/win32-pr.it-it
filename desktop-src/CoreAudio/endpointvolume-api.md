---
description: API EndpointVolume
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: API EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748551"
---
# <a name="endpointvolume-api"></a><span data-ttu-id="cbdd5-103">API EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="cbdd5-103">EndpointVolume API</span></span>

<span data-ttu-id="cbdd5-104">L'API EndpointVolume consente ai client specializzati di controllare e monitorare i livelli di volume dei [dispositivi dell'endpoint audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="cbdd5-104">The EndpointVolume API enables specialized clients to control and monitor the volume levels of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="cbdd5-105">Un client ottiene i riferimenti alle interfacce nell'API EndpointVolume ottenendo l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) di un dispositivo dell'endpoint audio e chiamando il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) .</span><span class="sxs-lookup"><span data-stu-id="cbdd5-105">A client obtains references to the interfaces in the EndpointVolume API by obtaining the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an audio endpoint device and calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method.</span></span>

<span data-ttu-id="cbdd5-106">Il file di intestazione Endpointvolume. h definisce le interfacce nell'API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-106">Header file Endpointvolume.h defines the interfaces in the EndpointVolume API.</span></span>

<span data-ttu-id="cbdd5-107">Le applicazioni audio che usano l' [API MMDevice](mmdevice-api.md) e [WASAPI](wasapi.md) in genere usano l'interfaccia [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) per controllare i livelli di volume per ogni singola sessione.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-107">Audio applications that use the [MMDevice API](mmdevice-api.md) and [WASAPI](wasapi.md) typically use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interface to control volume levels on a per-session basis.</span></span> <span data-ttu-id="cbdd5-108">Solo due tipi di applicazioni audio richiedono l'uso dell'API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-108">Only two types of audio applications require the use of the EndpointVolume API.</span></span> <span data-ttu-id="cbdd5-109">Questi tipi di applicazioni sono:</span><span class="sxs-lookup"><span data-stu-id="cbdd5-109">These application types are:</span></span>

-   <span data-ttu-id="cbdd5-110">Applicazioni che gestiscono i livelli di volume master dei dispositivi dell'endpoint audio, in modo analogo al programma di controllo del volume di Windows, Sndvol.exe.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-110">Applications that manage the master volume levels of audio endpoint devices, similar to the Windows volume-control program, Sndvol.exe.</span></span>
-   <span data-ttu-id="cbdd5-111">Applicazioni audio professionali ("Audio Pro") che richiedono l'accesso in modalità esclusiva ai dispositivi dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-111">Professional audio ("pro audio") applications that require exclusive-mode access to audio endpoint devices.</span></span>

<span data-ttu-id="cbdd5-112">L'uso inappropriato dell'API EndpointVolume può interferire con i criteri audio di Windows e interrompere le impostazioni del volume di sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-112">Inappropriate use of the EndpointVolume API can interfere with Windows audio policy and disrupt the user's system volume settings.</span></span>

<span data-ttu-id="cbdd5-113">Se un dispositivo endpoint audio implementa il volume hardware e i controlli di silenziamento, l'API EndpointVolume usa tali controlli per gestire il volume del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-113">If an audio endpoint device implements hardware volume and mute controls, the EndpointVolume API uses those controls to manage the device volume.</span></span> <span data-ttu-id="cbdd5-114">In caso contrario, l'API EndpointVolume implementa i controlli nel software, in modo trasparente per il client.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-114">Otherwise, the EndpointVolume API implements the controls in software, transparently to the client.</span></span>

<span data-ttu-id="cbdd5-115">Se un dispositivo dispone di controlli di volume e silenziamento hardware, le modifiche apportate alle impostazioni volume e mute del dispositivo tramite l'API EndpointVolume influiscono sul livello del volume sia in modalità condivisa che in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-115">If a device has hardware volume and mute controls, changes made to the device's volume and mute settings through the EndpointVolume API affect the volume level in both shared mode and exclusive mode.</span></span> <span data-ttu-id="cbdd5-116">Se un dispositivo non dispone di controlli di volume e silenziamento hardware, le modifiche apportate al volume software e ai controlli di silenziamento tramite l'API EndpointVolume influiscono sul livello del volume in modalità condivisa, ma non in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-116">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through the EndpointVolume API affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="cbdd5-117">In modalità esclusiva, il client e il dispositivo scambiano direttamente i dati audio, ignorando i controlli software.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-117">In exclusive mode, the client and the device exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="cbdd5-118">Per le applicazioni che devono gestire il volume hardware e i controlli di silenziamento, l'API di EndpointVolume offre due potenziali vantaggi rispetto all' [API DeviceTopology](devicetopology-api.md).</span><span class="sxs-lookup"><span data-stu-id="cbdd5-118">For applications that must manage hardware volume and mute controls, the EndpointVolume API offers two potential advantages over the [DeviceTopology API](devicetopology-api.md).</span></span>

<span data-ttu-id="cbdd5-119">In primo luogo, un numero di dispositivi scheda audio non dispone di controlli volume hardware.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-119">First, a number of audio adapter devices lack hardware volume controls.</span></span> <span data-ttu-id="cbdd5-120">Se un dispositivo non dispone di un controllo volume hardware, l'interfaccia [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) nell'API EndpointVolume implementa automaticamente un controllo volume software nel flusso da o verso tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-120">If a device lacks a hardware volume control, the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the EndpointVolume API automatically implements a software volume control on the stream to or from that device.</span></span> <span data-ttu-id="cbdd5-121">Per un client dell'API EndpointVolume, il risultato è lo stesso se il controllo del volume viene implementato nell'hardware dal dispositivo o nel software dall'interfaccia API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-121">For a client of the EndpointVolume API, the result is the same whether the volume control is implemented in hardware by the device or in software by the EndpointVolume API interface.</span></span>

<span data-ttu-id="cbdd5-122">In secondo luogo, anche se il dispositivo adapter implementa i controlli volume hardware, un'applicazione che usa l'API DeviceTopology per implementare un algoritmo di attraversamento della topologia potrebbe non riuscire a trovare il controllo che sta cercando.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-122">Second, even if the adapter device does implement hardware volume controls, an application that uses the DeviceTopology API to implement a topology-traversal algorithm might fail to find the control that it is looking for.</span></span> <span data-ttu-id="cbdd5-123">In genere, un'applicazione di questo tipo è progettata per attraversare la topologia hardware di un determinato dispositivo o set di dispositivi correlati.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-123">Typically, such an application is designed to traverse the hardware topology of a particular device or set of related devices.</span></span> <span data-ttu-id="cbdd5-124">L'applicazione rischia di non riuscire se tenta di attraversare la topologia di un dispositivo per cui non è stato progettato o testato appositamente.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-124">The application risks failing if it attempts to traverse the topology of a device that it has not been specifically designed for or tested with.</span></span>

<span data-ttu-id="cbdd5-125">Solo le applicazioni specializzate che devono accedere a funzioni hardware diverse dai controlli volume e mute richiedono l'uso dell'API DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-125">Only specialized applications that must access hardware functions other than volume and mute controls require the use of the DeviceTopology API.</span></span> <span data-ttu-id="cbdd5-126">Per le applicazioni che richiedono il controllo solo del livello di volume di un flusso in modalità esclusiva, l'API EndpointVolume è più semplice da usare e funziona in modo affidabile con una gamma più ampia di dispositivi hardware audio.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-126">For applications that require control only of the volume level of an exclusive-mode stream, the EndpointVolume API is simpler to use and works reliably with a wider range of audio hardware devices.</span></span>

<span data-ttu-id="cbdd5-127">Per esempi di codice che usano le interfacce nell'API EndpointVolume, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="cbdd5-127">For code examples that use the interfaces in the EndpointVolume API, see the following topics:</span></span>

-   [<span data-ttu-id="cbdd5-128">Controlli volume endpoint</span><span class="sxs-lookup"><span data-stu-id="cbdd5-128">Endpoint Volume Controls</span></span>](endpoint-volume-controls.md)
-   [<span data-ttu-id="cbdd5-129">Contatori di picco</span><span class="sxs-lookup"><span data-stu-id="cbdd5-129">Peak Meters</span></span>](peak-meters.md)

<span data-ttu-id="cbdd5-130">Per vedere un esempio che usa l'API EndpointVolume, vedere [EndpointVolume](endpointvolume.md) nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-130">To see a sample that uses the EndpointVolume API, see [EndpointVolume](endpointvolume.md) in the Windows SDK.</span></span>

<span data-ttu-id="cbdd5-131">L'API EndpointVolume implementa le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-131">The EndpointVolume API implements the following interfaces.</span></span>



| <span data-ttu-id="cbdd5-132">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="cbdd5-132">Interface</span></span>                                                | <span data-ttu-id="cbdd5-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbdd5-133">Description</span></span>                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdd5-134">**IAudioEndpointVolume**</span><span class="sxs-lookup"><span data-stu-id="cbdd5-134">**IAudioEndpointVolume**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | <span data-ttu-id="cbdd5-135">Rappresenta i controlli del volume nel flusso audio da o verso un dispositivo endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-135">Represents the volume controls on the audio stream to or from an audio endpoint device.</span></span> |
| [<span data-ttu-id="cbdd5-136">**IAudioMeterInformation**</span><span class="sxs-lookup"><span data-stu-id="cbdd5-136">**IAudioMeterInformation**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | <span data-ttu-id="cbdd5-137">Rappresenta un indicatore di picco nel flusso audio da o verso un dispositivo endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-137">Represents a peak meter on the audio stream to or from an audio endpoint device.</span></span>        |



 

<span data-ttu-id="cbdd5-138">Inoltre, i client dell'API EndpointVolume che richiedono la notifica delle modifiche del volume e del muting nei dispositivi dell'endpoint audio devono implementare la seguente interfaccia.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-138">In addition, clients of the EndpointVolume API that require notification of volume and muting changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="cbdd5-139">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="cbdd5-139">Interface</span></span>                                                            | <span data-ttu-id="cbdd5-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbdd5-140">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdd5-141">**IAudioEndpointVolumeCallback**</span><span class="sxs-lookup"><span data-stu-id="cbdd5-141">**IAudioEndpointVolumeCallback**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | <span data-ttu-id="cbdd5-142">Fornisce notifiche in caso di modifica del livello di volume o di muting di un dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="cbdd5-142">Provides notifications when the volume level or muting state of an audio endpoint device changes.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cbdd5-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cbdd5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbdd5-144">Controlli del volume</span><span class="sxs-lookup"><span data-stu-id="cbdd5-144">Volume Controls</span></span>](volume-controls.md)
</dt> <dt>

[<span data-ttu-id="cbdd5-145">**Interfaccia IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="cbdd5-145">**IMMDevice Interface**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="cbdd5-146">**IMMDevice:: Activate**</span><span class="sxs-lookup"><span data-stu-id="cbdd5-146">**IMMDevice::Activate**</span></span>](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[<span data-ttu-id="cbdd5-147">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="cbdd5-147">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[<span data-ttu-id="cbdd5-148">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="cbdd5-148">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



