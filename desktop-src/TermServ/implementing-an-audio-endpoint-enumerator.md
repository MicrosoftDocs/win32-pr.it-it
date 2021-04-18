---
title: Implementazione di un enumeratore di endpoint audio personalizzato
description: A partire da Windows Server 2008 R2, è possibile implementare un enumeratore endpoint audio remoto personalizzato come parte di un provider di protocollo Desktop remoto.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ab2a572169f20a7f8f9db194449be5361e409
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300590"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a><span data-ttu-id="70753-103">Implementazione di un enumeratore di endpoint audio personalizzato</span><span class="sxs-lookup"><span data-stu-id="70753-103">Implementing a Custom Audio Endpoint Enumerator</span></span>

<span data-ttu-id="70753-104">A partire da Windows Server 2008 R2, è possibile implementare un enumeratore endpoint audio remoto personalizzato come parte di un provider di protocollo Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="70753-104">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span> <span data-ttu-id="70753-105">Un provider di protocollo Desktop remoto può usare un enumeratore di endpoint audio personalizzato per recuperare una raccolta di endpoint audio con un set specifico di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="70753-105">A Remote Desktop protocol provider can use a custom audio endpoint enumerator to retrieve a collection of audio endpoints that have a specific set of capabilities.</span></span>

<span data-ttu-id="70753-106">**Per implementare un enumeratore di endpoint audio remoto personalizzato**</span><span class="sxs-lookup"><span data-stu-id="70753-106">**To implement a custom remote audio endpoint enumerator**</span></span>

1.  <span data-ttu-id="70753-107">La soluzione di enumeratore endpoint personalizzato deve implementare quattro tipi principali di oggetti: oggetti enumeratore dispositivi, oggetti raccolta dispositivi, oggetti dispositivo e oggetti archivio proprietà.</span><span class="sxs-lookup"><span data-stu-id="70753-107">Your custom endpoint enumerator solution should implement four main types of objects: device enumerator objects, device collection objects, device objects, and property store objects.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="70753-108">Tipo di oggetto</span><span class="sxs-lookup"><span data-stu-id="70753-108">Object type</span></span></th>
    <th><span data-ttu-id="70753-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70753-109">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="70753-110">Oggetto enumeratore dispositivi</span><span class="sxs-lookup"><span data-stu-id="70753-110">Device enumerator object</span></span><br/></td>
    <td><span data-ttu-id="70753-111">Un oggetto enumeratore di dispositivi fornisce la funzionalità di enumeratore dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="70753-111">A device enumerator object provides the endpoint enumerator functionality.</span></span> <span data-ttu-id="70753-112">Espone metodi che restituiscono un endpoint predefinito e raccolte di endpoint specificati.</span><span class="sxs-lookup"><span data-stu-id="70753-112">It exposes methods that return a default endpoint and specified collections of endpoints.</span></span> <span data-ttu-id="70753-113">Ad esempio, a seconda dei criteri specificati, l'enumeratore può restituire gli endpoint di comunicazione, gli endpoint di riproduzione o gli endpoint di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="70753-113">For example, depending on the criteria specified, the enumerator can return communication endpoints, playback endpoints, or capture endpoints.</span></span> <span data-ttu-id="70753-114">L'oggetto enumeratore Device deve implementare l'interfaccia <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="70753-114">The device enumerator object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="70753-115">Oggetto raccolta dispositivi</span><span class="sxs-lookup"><span data-stu-id="70753-115">Device collection object</span></span><br/></td>
    <td><span data-ttu-id="70753-116">Un oggetto raccolta dispositivi rappresenta una raccolta di dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="70753-116">A device collection object represents a collection of audio devices.</span></span> <span data-ttu-id="70753-117">Deve implementare l'interfaccia <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="70753-117">It must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="70753-118">Oggetto dispositivo</span><span class="sxs-lookup"><span data-stu-id="70753-118">Device object</span></span><br/></td>
    <td><span data-ttu-id="70753-119">Un oggetto dispositivo rappresenta un dispositivo audio particolare.</span><span class="sxs-lookup"><span data-stu-id="70753-119">A device object represents a particular audio device.</span></span> <span data-ttu-id="70753-120">Consente di accedere all'archivio delle proprietà del dispositivo audio ed espone le interfacce di riproduzione e acquisizione audio disponibili sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70753-120">It provides access to the audio device's property store and exposes the audio playback and capture interfaces available on the device.</span></span> <span data-ttu-id="70753-121">L'oggetto dispositivo deve implementare le interfacce <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> e <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="70753-121">The device object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> and <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> interfaces.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="70753-122">Oggetto archivio proprietà</span><span class="sxs-lookup"><span data-stu-id="70753-122">Property store object</span></span><br/></td>
    <td><span data-ttu-id="70753-123">Un oggetto archivio proprietà espone le proprietà associate a un dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="70753-123">A property store object exposes the properties associated with an audio device.</span></span> <span data-ttu-id="70753-124">Alcune di queste proprietà vengono usate dal sistema, ma le applicazioni possono archiviare anche proprietà arbitrarie con l'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="70753-124">Some of these properties are used by the system, but applications can store arbitrary properties with the audio endpoint as well.</span></span><br/> <span data-ttu-id="70753-125">Tutti i dispositivi audio hanno le tre proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="70753-125">All audio devices have the following three properties:</span></span><br/>
    <ul>
    <li><span data-ttu-id="70753-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="70753-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span></span></li>
    <li><span data-ttu-id="70753-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span><span class="sxs-lookup"><span data-stu-id="70753-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span></span></li>
    <li><span data-ttu-id="70753-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="70753-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span></span></li>
    </ul>
<span data-ttu-id="70753-129">L'oggetto archivio proprietà deve implementare l'interfaccia <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> .</span><span class="sxs-lookup"><span data-stu-id="70753-129">The property store object must implement the <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="70753-130">L'enumeratore endpoint personalizzato deve essere implementato in una DLL che può essere caricata nel sistema audio e in altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="70753-130">The custom endpoint enumerator must be implemented in a DLL that can be loaded into the audio system and other applications.</span></span> <span data-ttu-id="70753-131">La DLL deve essere firmata in modo che i processi protetti possano caricarla.</span><span class="sxs-lookup"><span data-stu-id="70753-131">The DLL must be signed so that secure processes can load it.</span></span> <span data-ttu-id="70753-132">La DLL deve implementare ed esportare la funzione [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) , che funge da punto di ingresso all'enumeratore dell'endpoint personalizzato.</span><span class="sxs-lookup"><span data-stu-id="70753-132">The DLL must implement and export the [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) function, which acts as an entry point to the custom endpoint enumerator.</span></span>

<span data-ttu-id="70753-133">Il servizio Servizi Desktop remoto chiama il metodo [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) e imposta il parametro *QueryType* su **WTS \_ query \_ AUDIOENUM \_ dll** per recuperare il nome dell'oggetto enumeratore.</span><span class="sxs-lookup"><span data-stu-id="70753-133">The Remote Desktop Services service calls the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) method and sets the *QueryType* parameter to **WTS\_QUERY\_AUDIOENUM\_DLL** to retrieve the name of the enumerator object.</span></span>

<span data-ttu-id="70753-134">Gli oggetti enumeratore personalizzati utilizzano interfacce simili a COM e un meccanismo di conteggio dei riferimenti simile a COM, ma non sono veri oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="70753-134">Custom enumerator objects use COM-like interfaces and a COM-like reference counting mechanism, but they are not true COM objects.</span></span> <span data-ttu-id="70753-135">L'enumeratore di endpoint personalizzato deve avere la possibilità di utilizzare interfacce audio legacy utilizzate da applicazioni che non supportano COM.</span><span class="sxs-lookup"><span data-stu-id="70753-135">The custom endpoint enumerator must have the ability to work with legacy audio interfaces used by applications that do not support COM.</span></span> <span data-ttu-id="70753-136">Per questo motivo, l'enumeratore endpoint personalizzato non deve basarsi sul meccanismo di gestione del ciclo di vita di COM.</span><span class="sxs-lookup"><span data-stu-id="70753-136">For this reason, the custom endpoint enumerator must not rely on COM's life cycle management mechanism.</span></span> <span data-ttu-id="70753-137">I consumer dell'enumeratore dell'endpoint audio, ad esempio MMDevAPI.dll, caricano la DLL dell'enumeratore di endpoint personalizzato quando richiesto dalle applicazioni utente e non scaricano l'enumeratore mentre l'enumeratore include un riferimento a un oggetto enumeratore di dispositivi, oggetto della raccolta dispositivi, oggetto dispositivo o oggetto archivio proprietà.</span><span class="sxs-lookup"><span data-stu-id="70753-137">Consumers of your audio endpoint enumerator, such as MMDevAPI.dll, load the custom endpoint enumerator DLL when required by user applications, and they will not unload the enumerator while the enumerator holds a reference to a device enumerator object, device collection object, device object, or property store object.</span></span> <span data-ttu-id="70753-138">Tuttavia, non è possibile per questi consumer tenere traccia dei riferimenti ad altri tipi di oggetti di proprietà dell'enumeratore di endpoint personalizzato.</span><span class="sxs-lookup"><span data-stu-id="70753-138">It is not possible, however, for these consumers to track references to other types of objects owned by the custom endpoint enumerator.</span></span> <span data-ttu-id="70753-139">Di conseguenza, è consigliabile che l'enumeratore dell'endpoint personalizzato non crei oggetti che potrebbero sopravvivere a questi quattro tipi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="70753-139">Accordingly, we recommend that your custom endpoint enumerator not create any objects that could outlive these four types of objects.</span></span>

## <a name="to-implement-a-custom-audio-endpoint"></a><span data-ttu-id="70753-140">Per implementare un endpoint audio personalizzato</span><span class="sxs-lookup"><span data-stu-id="70753-140">To implement a custom audio endpoint</span></span>

<span data-ttu-id="70753-141">Per implementare un enumeratore di dispositivo audio personalizzato, è necessario implementare un endpoint audio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="70753-141">To implement a custom audio device enumerator, you must implement a custom audio endpoint.</span></span> <span data-ttu-id="70753-142">Il modo in cui i dispositivi audio personalizzati sono collegati consiste nell'usare le due istruzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="70753-142">The way that your custom audio devices are linked is by using the following two statements:</span></span>

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

<span data-ttu-id="70753-143">Non si prevede di implementare l'elenco completo delle interfacce [**IMMDevice:: Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) nell'enumeratore dispositivo audio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="70753-143">We do not expect you to implement the full list of [**IMMDevice::Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) interfaces in your custom audio device enumerator.</span></span> <span data-ttu-id="70753-144">In alternativa, è necessario implementare [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) e [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span><span class="sxs-lookup"><span data-stu-id="70753-144">Instead, you should implement [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) and [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="70753-145">Facoltativamente, è possibile implementare altri, ad esempio [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume).</span><span class="sxs-lookup"><span data-stu-id="70753-145">You can optionally implement a few more, such as [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume).</span></span> <span data-ttu-id="70753-146">Per qualsiasi interfaccia non implementata, è necessario restituire **E \_ nointerface** (è necessario usare questo codice di errore specifico).</span><span class="sxs-lookup"><span data-stu-id="70753-146">For any interface you do not implement, you should return **E\_NOINTERFACE** (you must use this specific failure code).</span></span> <span data-ttu-id="70753-147">Windows eseguirà quindi il fallback a un'implementazione predefinita dell'interfaccia (ad esempio, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).</span><span class="sxs-lookup"><span data-stu-id="70753-147">Windows will then fall back to a stock implementation of the interface (for example, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).</span></span>

<span data-ttu-id="70753-148">Per la documentazione di riferimento aggiuntiva su come implementare e registrare gli endpoint audio, vedere [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span><span class="sxs-lookup"><span data-stu-id="70753-148">For additional reference documentation about how to implement and register audio endpoints, see [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="70753-149">Per un diagramma che illustra il funzionamento di WASAPI, vedere [componenti audio in modalità utente](/windows/desktop/CoreAudio/user-mode-audio-components).</span><span class="sxs-lookup"><span data-stu-id="70753-149">For a diagram that shows how WASAPI works, see [User-Mode Audio Components](/windows/desktop/CoreAudio/user-mode-audio-components).</span></span> <span data-ttu-id="70753-150">Si noti che tutte le audio in modalità utente sono nuove a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="70753-150">Note that all of user-mode audio is new beginning with Windows Server 2008.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70753-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70753-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70753-152">Creazione di un provider di Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="70753-152">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="70753-153">**GetTSAudioEndpointEnumeratorForSession**</span><span class="sxs-lookup"><span data-stu-id="70753-153">**GetTSAudioEndpointEnumeratorForSession**</span></span>](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[<span data-ttu-id="70753-154">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="70753-154">**IMMDevice**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="70753-155">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="70753-155">**IMMDeviceCollection**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[<span data-ttu-id="70753-156">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="70753-156">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[<span data-ttu-id="70753-157">**IMMEndpoint**</span><span class="sxs-lookup"><span data-stu-id="70753-157">**IMMEndpoint**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[<span data-ttu-id="70753-158">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="70753-158">IPropertyStore</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>