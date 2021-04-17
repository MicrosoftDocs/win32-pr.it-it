---
description: Topologie del dispositivo
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: Topologie del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524257"
---
# <a name="device-topologies"></a><span data-ttu-id="e5bc7-103">Topologie del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e5bc7-103">Device Topologies</span></span>

<span data-ttu-id="e5bc7-104">L' [API DeviceTopology](devicetopology-api.md) fornisce ai client il controllo su un'ampia gamma di funzioni interne di schede audio a cui non possono accedere tramite l'API [MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)o l' [API EndpointVolume](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="e5bc7-104">The [DeviceTopology API](devicetopology-api.md) gives clients control over a variety of internal functions of audio adapters that they cannot access through the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), or the [EndpointVolume API](endpointvolume-api.md).</span></span>

<span data-ttu-id="e5bc7-105">Come spiegato in precedenza, l' [API MMDevice](mmdevice-api.md), [WASAPI](wasapi.md)e l' [API EndpointVolume](endpointvolume-api.md) presentano microfoni, altoparlanti, cuffie e altri dispositivi di input e output audio ai client come [dispositivi di endpoint audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="e5bc7-105">As explained previously, the [MMDevice API](mmdevice-api.md), [WASAPI](wasapi.md), and the [EndpointVolume API](endpointvolume-api.md) present microphones, speakers, headphones, and other audio input and output devices to clients as [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="e5bc7-106">Il modello di dispositivo endpoint fornisce ai client un comodo accesso ai controlli volume e mute nei dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-106">The endpoint device model provides clients with convenient access to volume and mute controls in audio devices.</span></span> <span data-ttu-id="e5bc7-107">I client che richiedono solo questi controlli semplici possono evitare di attraversare le topologie interne dei dispositivi hardware nelle schede audio.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-107">Clients that require only these simple controls can avoid traversing the internal topologies of hardware devices in audio adapters.</span></span>

<span data-ttu-id="e5bc7-108">In Windows Vista, il motore audio configura automaticamente le topologie dei dispositivi audio per l'uso da parte delle applicazioni audio.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-108">In Windows Vista, the audio engine automatically configures the topologies of audio devices for use by audio applications.</span></span> <span data-ttu-id="e5bc7-109">Quindi, raramente, le applicazioni devono usare l'API DeviceTopology per questo scopo.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-109">Thus, applications rarely, if ever, need to use the DeviceTopology API for this purpose.</span></span> <span data-ttu-id="e5bc7-110">Si supponga, ad esempio, che una scheda audio includa un multiplexer di input in grado di acquisire un flusso da un input di riga o un microfono, ma che non sia in grado di acquisire flussi da entrambi i dispositivi endpoint nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-110">For example, assume that an audio adapter contains an input multiplexer that can capture a stream from either a line input or a microphone, but that cannot capture streams from both endpoint devices at the same time.</span></span> <span data-ttu-id="e5bc7-111">Si supponga che l'utente abbia abilitato le applicazioni in modalità esclusiva per precedere l'uso di un dispositivo endpoint audio dalle applicazioni in modalità condivisa, come descritto in [flussi in modalità esclusiva](exclusive-mode-streams.md).</span><span class="sxs-lookup"><span data-stu-id="e5bc7-111">Assume that the user has enabled exclusive-mode applications to preempt the use of an audio endpoint device by shared-mode applications, as described in [Exclusive-Mode Streams](exclusive-mode-streams.md).</span></span> <span data-ttu-id="e5bc7-112">Se un'applicazione in modalità condivisa sta registrando un flusso dall'input di riga nel momento in cui un'applicazione in modalità esclusiva inizia a registrare un flusso dal microfono, il motore audio passa automaticamente il multiplexer dall'input di riga al microfono.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-112">If a shared-mode application is recording a stream from the line input at the time that an exclusive-mode application begins recording a stream from the microphone, the audio engine automatically switches the multiplexer from the line input to the microphone.</span></span> <span data-ttu-id="e5bc7-113">Al contrario, nelle versioni precedenti di Windows, incluso Windows XP, l'applicazione in modalità esclusiva in questo esempio utilizzerebbe le funzioni **mixerXxx** nell'API multimediale di Windows per attraversare le topologie dei dispositivi dell'adapter, individuare il multiplexer e configurare multiplexer per selezionare l'input del microfono.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-113">In contrast, in earlier versions of Windows, including Windows XP, the exclusive-mode application in this example would use the **mixerXxx** functions in the Windows multimedia API to traverse the topologies of the adapter devices, discover the multiplexer, and configure the multiplexer to select the microphone input.</span></span> <span data-ttu-id="e5bc7-114">In Windows Vista questi passaggi non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-114">In Windows Vista, these steps are no longer required.</span></span>

<span data-ttu-id="e5bc7-115">Tuttavia, alcuni client potrebbero richiedere il controllo esplicito dei tipi di controlli hardware audio a cui non è possibile accedere tramite l'API MMDevice, WASAPI o l'API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-115">However, some clients might require explicit control over types of audio hardware controls that cannot be accessed through the MMDevice API, WASAPI, or the EndpointVolume API.</span></span> <span data-ttu-id="e5bc7-116">Per questi client, l'API DeviceTopology consente di attraversare le topologie dei dispositivi Adapter per individuare e gestire i controlli audio nei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-116">For these clients, the DeviceTopology API provides the ability to traverse the topologies of adapter devices to discover and manage the audio controls in the devices.</span></span> <span data-ttu-id="e5bc7-117">Le applicazioni che usano l'API di DeviceTopology devono essere progettate con attenzione per evitare di interferire con i criteri audio di Windows e le configurazioni interne dei dispositivi audio condivisi con altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-117">Applications that use the DeviceTopology API must be designed with care to avoid interfering with Windows audio policy and disturbing the internal configurations of audio devices that are shared with other applications.</span></span> <span data-ttu-id="e5bc7-118">Per ulteriori informazioni sui criteri audio di Windows, vedere [componenti audio in modalità utente](user-mode-audio-components.md).</span><span class="sxs-lookup"><span data-stu-id="e5bc7-118">For more information about Windows audio policy, see [User-Mode Audio Components](user-mode-audio-components.md).</span></span>

<span data-ttu-id="e5bc7-119">L'API DeviceTopology fornisce interfacce per l'individuazione e la gestione dei seguenti tipi di controlli audio in una topologia di dispositivo:</span><span class="sxs-lookup"><span data-stu-id="e5bc7-119">The DeviceTopology API provides interfaces for discovering and managing the following types of audio controls in a device topology:</span></span>

-   <span data-ttu-id="e5bc7-120">Controllo di guadagno automatico</span><span class="sxs-lookup"><span data-stu-id="e5bc7-120">Automatic gain control</span></span>
-   <span data-ttu-id="e5bc7-121">Controllo Bass</span><span class="sxs-lookup"><span data-stu-id="e5bc7-121">Bass control</span></span>
-   <span data-ttu-id="e5bc7-122">Selettore input (Multiplexer)</span><span class="sxs-lookup"><span data-stu-id="e5bc7-122">Input selector (multiplexer)</span></span>
-   <span data-ttu-id="e5bc7-123">Controllo della sonorità</span><span class="sxs-lookup"><span data-stu-id="e5bc7-123">Loudness control</span></span>
-   <span data-ttu-id="e5bc7-124">Controllo midrange</span><span class="sxs-lookup"><span data-stu-id="e5bc7-124">Midrange control</span></span>
-   <span data-ttu-id="e5bc7-125">Disattiva controllo</span><span class="sxs-lookup"><span data-stu-id="e5bc7-125">Mute control</span></span>
-   <span data-ttu-id="e5bc7-126">Selettore di output (demultiplexer)</span><span class="sxs-lookup"><span data-stu-id="e5bc7-126">Output selector (demultiplexer)</span></span>
-   <span data-ttu-id="e5bc7-127">Misurazione picco</span><span class="sxs-lookup"><span data-stu-id="e5bc7-127">Peak meter</span></span>
-   <span data-ttu-id="e5bc7-128">Controllo Treble</span><span class="sxs-lookup"><span data-stu-id="e5bc7-128">Treble control</span></span>
-   <span data-ttu-id="e5bc7-129">Controllo volume</span><span class="sxs-lookup"><span data-stu-id="e5bc7-129">Volume control</span></span>

<span data-ttu-id="e5bc7-130">Inoltre, l'API DeviceTopology consente ai client di eseguire query sui dispositivi Adapter per ottenere informazioni sui formati di flusso supportati.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-130">In addition, the DeviceTopology API enables clients to query adapter devices for information about the stream formats that they support.</span></span> <span data-ttu-id="e5bc7-131">Il file di intestazione Devicetopology. h definisce le interfacce nell'API DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-131">The header file Devicetopology.h defines the interfaces in the DeviceTopology API.</span></span>

<span data-ttu-id="e5bc7-132">Nel diagramma seguente viene illustrato un esempio di diverse topologie di dispositivo connesse per la parte di una scheda PCI che acquisisce l'audio da un microfono, un input di linea e un lettore di CD.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-132">The following diagram shows an example of several connected device topologies for the portion of a PCI adapter that captures audio from a microphone, line input, and CD player.</span></span>

![esempio di quattro topologie di dispositivi connessi](images/fig2.jpg)

<span data-ttu-id="e5bc7-134">Il diagramma precedente Mostra i percorsi dati che portano dagli input analoghi al bus di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-134">The preceding diagram shows the data paths that lead from the analog inputs to the system bus.</span></span> <span data-ttu-id="e5bc7-135">Ognuno dei dispositivi seguenti è rappresentato come un oggetto topologia di dispositivo con un'interfaccia [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) :</span><span class="sxs-lookup"><span data-stu-id="e5bc7-135">Each of the following devices is represented as a device-topology object with an [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) interface:</span></span>

-   <span data-ttu-id="e5bc7-136">Dispositivo di acquisizione Wave</span><span class="sxs-lookup"><span data-stu-id="e5bc7-136">Wave capture device</span></span>
-   <span data-ttu-id="e5bc7-137">Dispositivo multiplexer di input</span><span class="sxs-lookup"><span data-stu-id="e5bc7-137">Input multiplexer device</span></span>
-   <span data-ttu-id="e5bc7-138">Dispositivo endpoint A</span><span class="sxs-lookup"><span data-stu-id="e5bc7-138">Endpoint device A</span></span>
-   <span data-ttu-id="e5bc7-139">Dispositivo endpoint B</span><span class="sxs-lookup"><span data-stu-id="e5bc7-139">Endpoint device B</span></span>

<span data-ttu-id="e5bc7-140">Si noti che il diagramma della topologia combina i dispositivi Adapter (i dispositivi Wave Capture e input multiplexer) con i dispositivi endpoint.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-140">Note that the topology diagram combines adapter devices (the wave capture and input multiplexer devices) with endpoint devices.</span></span> <span data-ttu-id="e5bc7-141">Attraverso le connessioni tra i dispositivi, i dati audio passano da un dispositivo a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-141">Through the connections between devices, audio data passes from one device to the next.</span></span> <span data-ttu-id="e5bc7-142">Su ogni lato di una connessione è presente un connettore (con etichetta con nel diagramma) tramite il quale i dati entrano o lasciano un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-142">On each side of a connection is a connector (labeled Con in the diagram) through which data enters or leaves a device.</span></span>

<span data-ttu-id="e5bc7-143">Sul lato sinistro del diagramma, i segnali provenienti dai jack di input della riga e del microfono immettono i dispositivi endpoint.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-143">On the left edge of the diagram, signals from the line-input and microphone jacks enter the endpoint devices.</span></span>

<span data-ttu-id="e5bc7-144">All'interno del dispositivo di acquisizione Wave e il dispositivo multiplexer di input sono funzioni di elaborazione del flusso, che, nella terminologia dell'API DeviceTopology, sono denominate unità secondarie.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-144">Inside the wave capture device and input multiplexer device are stream-processing functions, which, in the terminology of the DeviceTopology API, are called subunits.</span></span> <span data-ttu-id="e5bc7-145">Nel diagramma precedente vengono visualizzati i tipi di unità secondari seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5bc7-145">The following types of subunits appear in the preceding diagram:</span></span>

-   <span data-ttu-id="e5bc7-146">Controllo volume (con etichetta VOL)</span><span class="sxs-lookup"><span data-stu-id="e5bc7-146">Volume control (labeled Vol)</span></span>
-   <span data-ttu-id="e5bc7-147">Controllo mute (con etichetta mute)</span><span class="sxs-lookup"><span data-stu-id="e5bc7-147">Mute control (labeled Mute)</span></span>
-   <span data-ttu-id="e5bc7-148">Multiplexer (o selettore input; con etichetta MUX)</span><span class="sxs-lookup"><span data-stu-id="e5bc7-148">Multiplexer (or input selector; labeled MUX)</span></span>
-   <span data-ttu-id="e5bc7-149">Convertitore analogico-digitale (ADC con etichetta)</span><span class="sxs-lookup"><span data-stu-id="e5bc7-149">Analog-to-digital converter (labeled ADC)</span></span>

<span data-ttu-id="e5bc7-150">Le impostazioni nelle unità secondarie volume, mute e multiplexer possono essere controllate dai client e l'API DeviceTopology fornisce le interfacce di controllo ai client per controllarle.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-150">The settings in the volume, mute, and multiplexer subunits can be controlled by clients, and the DeviceTopology API provides control interfaces to clients for controlling them.</span></span> <span data-ttu-id="e5bc7-151">In questo esempio, la sottounità ADC non ha impostazioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-151">In this example, the ADC subunit has no control settings.</span></span> <span data-ttu-id="e5bc7-152">Di conseguenza, l'API DeviceTopology non fornisce alcuna interfaccia di controllo per ADC.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-152">Thus, the DeviceTopology API provides no control interface for the ADC.</span></span>

<span data-ttu-id="e5bc7-153">Nella terminologia dell'API DeviceTopology, i connettori e le unità secondarie appartengono alla stessa categoria generale, parti.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-153">In the terminology of the DeviceTopology API, connectors and subunits belong to the same general category—parts.</span></span> <span data-ttu-id="e5bc7-154">Tutte le parti, indipendentemente dal fatto che si tratti di connettori o unità secondarie, forniscono un set comune di funzioni.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-154">All parts, regardless of whether they are connectors or subunits, provide a common set of functions.</span></span> <span data-ttu-id="e5bc7-155">L'API DeviceTopology implementa un'interfaccia [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) per rappresentare le funzioni generiche comuni ai connettori e alle sottounità.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-155">The DeviceTopology API implements an [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) interface to represent the generic functions that are common to connectors and subunits.</span></span> <span data-ttu-id="e5bc7-156">L'API implementa le interfacce [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) e [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) per rappresentare gli aspetti specifici dei connettori e delle sottounità.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-156">The API implements the [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) and [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) interfaces to represent the specific aspects of connectors and subunits.</span></span>

<span data-ttu-id="e5bc7-157">L'API DeviceTopology costruisce le topologie del dispositivo di acquisizione Wave e del dispositivo multiplexer di input dai filtri di streaming kernel (KS) che il driver audio espone al sistema operativo per rappresentare questi dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-157">The DeviceTopology API constructs the topologies of the wave capture device and input multiplexer device from the kernel-streaming (KS) filters that the audio driver exposes to the operating system to represent these devices.</span></span> <span data-ttu-id="e5bc7-158">Il driver della scheda audio implementa le interfacce **IMiniportWaveXxx** e **IMiniportTopology** per rappresentare le parti dipendenti dall'hardware di questi filtri. per ulteriori informazioni su queste interfacce e sui filtri KS, vedere la documentazione di Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-158">(The audio adapter driver implements **IMiniportWaveXxx** and **IMiniportTopology** interfaces to represent the hardware-dependent portions of these filters; for more information about these interfaces and about KS filters, see the Windows DDK documentation.)</span></span>

<span data-ttu-id="e5bc7-159">L'API DeviceTopology costruisce topologie semplici per rappresentare i dispositivi endpoint a e B nel diagramma precedente.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-159">The DeviceTopology API constructs trivial topologies to represent endpoint devices A and B in the preceding diagram.</span></span> <span data-ttu-id="e5bc7-160">La topologia del dispositivo di un endpoint è costituita da un singolo connettore.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-160">The device topology of an endpoint device consists of a single connector.</span></span> <span data-ttu-id="e5bc7-161">Questa topologia è semplicemente un segnaposto per il dispositivo endpoint e non contiene unità secondarie per l'elaborazione dei dati audio.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-161">This topology is merely a placeholder for the endpoint device and contains no subunits for processing audio data.</span></span> <span data-ttu-id="e5bc7-162">Infatti, i dispositivi Adapter contengono tutte le sottounità usate dalle applicazioni client per controllare l'elaborazione audio.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-162">In fact, adapter devices contain all of the subunits that client applications use to control audio processing.</span></span> <span data-ttu-id="e5bc7-163">La topologia del dispositivo di un endpoint viene utilizzata principalmente come punto di partenza per l'esplorazione delle topologie dei dispositivi adapter.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-163">The device topology of an endpoint device serves primarily as a starting point for exploring the device topologies of adapter devices.</span></span>

<span data-ttu-id="e5bc7-164">Le connessioni interne tra due parti di una topologia di dispositivo sono denominate collegamenti.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-164">Internal connections between two parts in a device topology are called links.</span></span> <span data-ttu-id="e5bc7-165">L'API DeviceTopology fornisce metodi per attraversare i collegamenti da una parte all'altra in una topologia di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-165">The DeviceTopology API provides methods for traversing links from one part to the next in a device topology.</span></span> <span data-ttu-id="e5bc7-166">L'API fornisce anche metodi per attraversare le connessioni tra topologie di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-166">The API also provides methods for traversing the connections between device topologies.</span></span>

<span data-ttu-id="e5bc7-167">Per iniziare l'esplorazione di un set di topologie di dispositivi connessi, un'applicazione client attiva l'interfaccia **IDeviceTopology** di un dispositivo endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-167">To begin exploration of a set of connected device topologies, a client application activates the **IDeviceTopology** interface of an audio endpoint device.</span></span> <span data-ttu-id="e5bc7-168">Il connettore in un dispositivo endpoint si connette a un connettore in una scheda audio o a una rete.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-168">The connector in an endpoint device connects either to a connector in an audio adapter or to a network.</span></span> <span data-ttu-id="e5bc7-169">Se l'endpoint si connette a un dispositivo in una scheda audio, i metodi nell'API DeviceTopology consentono all'applicazione di eseguire l'istruzione attraverso la connessione dall'endpoint alla scheda ottenendo un riferimento all'interfaccia **IDeviceTopology** del dispositivo adattatore sull'altro lato della connessione.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-169">If the endpoint connects to a device on an audio adapter, then the methods in the DeviceTopology API enable the application to step across the connection from the endpoint to the adapter by obtaining a reference to the **IDeviceTopology** interface of the adapter device on the other side of the connection.</span></span> <span data-ttu-id="e5bc7-170">Una rete, d'altra parte, non ha una topologia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-170">A network, on the other hand, has no device topology.</span></span> <span data-ttu-id="e5bc7-171">Una connessione di rete invia tramite pipe un flusso audio a un client che accede al sistema in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-171">A network connection pipes an audio stream to a client that is accessing the system remotely.</span></span>

<span data-ttu-id="e5bc7-172">L'API DeviceTopology consente di accedere solo alle topologie dei dispositivi hardware in una scheda audio.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-172">The DeviceTopology API provides access only to the topologies of the hardware devices in an audio adapter.</span></span> <span data-ttu-id="e5bc7-173">I dispositivi esterni sul bordo sinistro del diagramma e i componenti software sul bordo destro esulano dall'ambito dell'API.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-173">The external devices on the left edge of the diagram and the software components on the right edge are beyond the scope of the API.</span></span> <span data-ttu-id="e5bc7-174">Le linee tratteggiate su entrambi i lati del diagramma rappresentano i limiti dell'API DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-174">The dashed lines on either side of the diagram represent the limits of the DeviceTopology API.</span></span> <span data-ttu-id="e5bc7-175">Il client può usare l'API per esplorare un percorso dati che si estende dal jack di input al bus di sistema, ma l'API non può penetrare oltre questi limiti.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-175">The client can use the API to explore a data path that stretches from the input jack to the system bus, but the API cannot penetrate beyond these boundaries.</span></span>

<span data-ttu-id="e5bc7-176">A ogni connettore del diagramma precedente è associato un tipo di connessione che indica il tipo di connessione eseguita dal connettore.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-176">Each connector in the preceding diagram has an associated connection type that indicates the type of connection that the connector makes.</span></span> <span data-ttu-id="e5bc7-177">Pertanto, i connettori sui due lati di una connessione hanno sempre tipi di connessione identici.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-177">Thus, the connectors on the two sides of a connection always have identical connection types.</span></span> <span data-ttu-id="e5bc7-178">Il tipo di connessione è indicato da un valore di enumerazione [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) : fisico \_ esterno, fisico \_ interno, software \_ fisso, i/ \_ o software o rete.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-178">The connection type is indicated by a [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) enumeration value—Physical\_External, Physical\_Internal, Software\_Fixed, Software\_IO, or Network.</span></span> <span data-ttu-id="e5bc7-179">Le connessioni tra il dispositivo multiplexer di input e i dispositivi endpoint A e B sono di tipo \_ External fisico, il che significa che la connessione rappresenta una connessione fisica a un dispositivo esterno (in altre parole, un jack audio accessibile dall'utente).</span><span class="sxs-lookup"><span data-stu-id="e5bc7-179">The connections between the input multiplexer device and endpoint devices A and B are of type Physical\_External, which means that the connection represents a physical connection to an external device (in other words, a user-accessible audio jack).</span></span> <span data-ttu-id="e5bc7-180">La connessione al segnale analogico dal lettore CD interno è di tipo \_ Internal fisico, che indica una connessione fisica a un dispositivo ausiliario installato all'interno dello chassis del sistema.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-180">The connection to the analog signal from the internal CD player is of type Physical\_Internal, which indicates a physical connection to an auxiliary device that is installed inside the system chassis.</span></span> <span data-ttu-id="e5bc7-181">La connessione tra il dispositivo di acquisizione Wave e il dispositivo multiplexer di input è di tipo software \_ fixed, che indica una connessione permanente che è fissa e non può essere configurata in controllo software.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-181">The connection between the wave capture device and input multiplexer device is of type Software\_Fixed, which indicates a permanent connection that is fixed and cannot be configured under software control.</span></span> <span data-ttu-id="e5bc7-182">Infine, la connessione al bus di sistema sul lato destro del diagramma è di tipo software \_ io, che indica che l'i/O dei dati per la connessione viene implementato da un motore DMA sotto controllo software.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-182">Finally, the connection to the system bus on the right side of the diagram is of type Software\_IO, which indicates that the data I/O for the connection is implemented by a DMA engine under software control.</span></span> <span data-ttu-id="e5bc7-183">Il diagramma non include un esempio di tipo di connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-183">(The diagram does not include an example of a Network connection type.)</span></span>

<span data-ttu-id="e5bc7-184">Il client inizia a attraversare un percorso dati sul dispositivo endpoint.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-184">The client begins traversing a data path at the endpoint device.</span></span> <span data-ttu-id="e5bc7-185">In primo luogo, il client ottiene un'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) che rappresenta il dispositivo dell'endpoint, come illustrato in [enumerazione dei dispositivi audio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="e5bc7-185">First, the client obtains an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface that represents the endpoint device, as explained in [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span> <span data-ttu-id="e5bc7-186">Per ottenere l'interfaccia **IDeviceTopology** per il dispositivo endpoint, il client chiama il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con il parametro *IID* impostato su REFIID IID \_ IDeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-186">To obtain the **IDeviceTopology** interface for the endpoint device, the client calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method with parameter *iid* set to REFIID IID\_IDeviceTopology.</span></span>

<span data-ttu-id="e5bc7-187">Nell'esempio del diagramma precedente, il dispositivo multiplexer di input contiene tutti i controlli hardware (volume, mute e multiplexer) per i flussi di acquisizione dai jack di input di riga e microfono.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-187">In the example in the preceding diagram, the input multiplexer device contains all the hardware controls (volume, mute, and multiplexer) for the capture streams from the line-input and microphone jacks.</span></span> <span data-ttu-id="e5bc7-188">Nell'esempio di codice seguente viene illustrato come ottenere l'interfaccia **IDeviceTopology** per il dispositivo multiplexer di input dall'interfaccia **IMMDevice** per il dispositivo endpoint per l'input o il microfono della riga:</span><span class="sxs-lookup"><span data-stu-id="e5bc7-188">The following code example shows how to obtain the **IDeviceTopology** interface for the input multiplexer device from the **IMMDevice** interface for the endpoint device for the line input or microphone:</span></span>


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



<span data-ttu-id="e5bc7-189">La funzione GetHardwareDeviceTopology nell'esempio di codice precedente esegue i passaggi seguenti per ottenere l'interfaccia **IDeviceTopology** per il dispositivo multiplexer di input:</span><span class="sxs-lookup"><span data-stu-id="e5bc7-189">The GetHardwareDeviceTopology function in the previous code example performs the following steps to obtain the **IDeviceTopology** interface for the input multiplexer device:</span></span>

1.  <span data-ttu-id="e5bc7-190">Chiamare il metodo **IMMDevice:: Activate** per ottenere l'interfaccia **IDeviceTopology** per il dispositivo endpoint.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-190">Call the **IMMDevice::Activate** method to get the **IDeviceTopology** interface for the endpoint device.</span></span>
2.  <span data-ttu-id="e5bc7-191">Con l'interfaccia **IDeviceTopology** ottenuta nel passaggio precedente, chiamare il metodo [**IDeviceTopology:: GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) per ottenere l'interfaccia **IConnector** del connettore singolo (numero di connettore 0) nel dispositivo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-191">With the **IDeviceTopology** interface obtained in the preceding step, call the [**IDeviceTopology::GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) method to get the **IConnector** interface of the single connector (connector number 0) in the endpoint device.</span></span>
3.  <span data-ttu-id="e5bc7-192">Con l'interfaccia **IConnector** ottenuta nel passaggio precedente, chiamare il metodo [**IConnector:: GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) per ottenere l'interfaccia **IConnector** del connettore nel dispositivo multiplexer di input.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-192">With the **IConnector** interface obtained in the preceding step, call the [**IConnector::GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) method to get the **IConnector** interface of the connector in the input multiplexer device.</span></span>
4.  <span data-ttu-id="e5bc7-193">Eseguire una query sull'interfaccia **IConnector** ottenuta nel passaggio precedente per la relativa interfaccia **IPart** .</span><span class="sxs-lookup"><span data-stu-id="e5bc7-193">Query the **IConnector** interface obtained in the preceding step for its **IPart** interface.</span></span>
5.  <span data-ttu-id="e5bc7-194">Con l'interfaccia **IPart** ottenuta nel passaggio precedente, chiamare il metodo [**IPart:: GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) per ottenere l'interfaccia **IDeviceTopology** per il dispositivo multiplexer di input.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-194">With the **IPart** interface obtained in the preceding step, call the [**IPart::GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) method to get the **IDeviceTopology** interface for the input multiplexer device.</span></span>

<span data-ttu-id="e5bc7-195">Prima che l'utente possa registrare dal microfono nel diagramma precedente, l'applicazione client deve verificare che il multiplexer selezioni l'input del microfono.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-195">Before the user can record from the microphone in the preceding diagram, the client application must make certain that the multiplexer selects the microphone input.</span></span> <span data-ttu-id="e5bc7-196">Nell'esempio di codice seguente viene illustrato come un client può attraversare il percorso dati dal microfono fino a quando non trova il multiplexer, che quindi programma per selezionare l'input del microfono:</span><span class="sxs-lookup"><span data-stu-id="e5bc7-196">The following code example shows how a client can traverse the data path from the microphone until it finds the multiplexer, which it then programs to select the microphone input:</span></span>


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



<span data-ttu-id="e5bc7-197">L'API DeviceTopology implementa un'interfaccia [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) per incapsulare un multiplexer, ad esempio quello nel diagramma precedente.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-197">The DeviceTopology API implements an [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) interface to encapsulate a multiplexer, such as the one in the preceding diagram.</span></span> <span data-ttu-id="e5bc7-198">Un'interfaccia [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) incapsula un Demultiplexer. Nell'esempio di codice precedente, il ciclo interno della funzione SelectCaptureDevice esegue una query su ogni unità secondaria che trova per individuare se la sottounità è un multiplexer.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-198">(An [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) interface encapsulates a demultiplexer.) In the preceding code example, the inner loop of the SelectCaptureDevice function queries each subunit that it finds to discover whether the subunit is a multiplexer.</span></span> <span data-ttu-id="e5bc7-199">Se l'unità secondaria è un multiplexer, la funzione chiama il metodo [**IAudioInputSelector:: Seselection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) per selezionare l'input che si connette al flusso dal dispositivo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-199">If the subunit is a multiplexer, then the function calls the [**IAudioInputSelector::SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) method to select the input that connects to the stream from the endpoint device.</span></span>

<span data-ttu-id="e5bc7-200">Nell'esempio di codice precedente, ogni iterazione del ciclo esterno attraversa una topologia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-200">In the preceding code example, each iteration of the outer loop traverses one device topology.</span></span> <span data-ttu-id="e5bc7-201">Quando si attraversano le topologie di dispositivo nel diagramma precedente, la prima iterazione attraversa il dispositivo multiplexer di input e la seconda iterazione attraversa il dispositivo di acquisizione Wave.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-201">When traversing the device topologies in the preceding diagram, the first iteration traverses the input multiplexer device and the second iteration traverses the wave capture device.</span></span> <span data-ttu-id="e5bc7-202">La funzione verrà terminata quando raggiunge il connettore sul bordo destro del diagramma.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-202">The function will terminate when it reaches the connector at the right edge of the diagram.</span></span> <span data-ttu-id="e5bc7-203">La terminazione si verifica quando la funzione rileva un connettore con un \_ tipo di connessione io software.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-203">Termination occurs when the function detects a connector with a Software\_IO connection type.</span></span> <span data-ttu-id="e5bc7-204">Questo tipo di connessione identifica il punto in cui il dispositivo adapter si connette al bus di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-204">This connection type identifies the point at which the adapter device connects to the system bus.</span></span>

<span data-ttu-id="e5bc7-205">La chiamata al metodo [**IPart:: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) nell'esempio di codice precedente ottiene un valore di enumerazione **IPartType** che indica se la parte corrente è un connettore o una sottounità di elaborazione audio.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-205">The call to the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) method in the preceding code example obtains an **IPartType** enumeration value that indicates whether the current part is a connector or an audio-processing subunit.</span></span>

<span data-ttu-id="e5bc7-206">Il ciclo interno nell'esempio di codice precedente passa attraverso il collegamento da una parte alla successiva chiamando il metodo [**IPart:: EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) .</span><span class="sxs-lookup"><span data-stu-id="e5bc7-206">The inner loop in the preceding code example steps across the link from one part to the next by calling the [**IPart::EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) method.</span></span> <span data-ttu-id="e5bc7-207">(Esiste anche un metodo [**IPart:: EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) per l'esecuzione di un'istruzione nella direzione opposta). Questo metodo recupera un oggetto [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) che contiene un elenco di tutte le parti in uscita.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-207">(There's also an [**IPart::EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) method for stepping in the opposite direction.) This method retrieves an [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) object that contains a list of all the outgoing parts.</span></span> <span data-ttu-id="e5bc7-208">Tuttavia, qualsiasi parte che la funzione SelectCaptureDevice prevede di riscontrare in un dispositivo di acquisizione avrà sempre esattamente una parte in uscita.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-208">However, any part that the SelectCaptureDevice function expects to encounter in a capture device will always have exactly one outgoing part.</span></span> <span data-ttu-id="e5bc7-209">Quindi, la chiamata successiva a [**IPartsList:: GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) richiede sempre la prima parte nell'elenco, il numero di parte 0, perché la funzione presuppone che questa sia l'unica parte nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-209">Thus, the subsequent call to [**IPartsList::GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) always requests the first part in the list, part number 0, because the function assumes that this is the only part in the list.</span></span>

<span data-ttu-id="e5bc7-210">Se la funzione SelectCaptureDevice rileva una topologia per la quale il presupposto non è valido, la funzione potrebbe non riuscire a configurare correttamente il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-210">If the SelectCaptureDevice function encounters a topology for which that assumption is not valid, the function might fail to configure the device correctly.</span></span> <span data-ttu-id="e5bc7-211">Per evitare un errore di questo tipo, una versione più generica della funzione può eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5bc7-211">To avoid such a failure, a more general-purpose version of the function might do the following:</span></span>

-   <span data-ttu-id="e5bc7-212">Chiamare il metodo [**IPartsList:: GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) per determinare il numero di parti in uscita.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-212">Call the [**IPartsList::GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) method to determine the number of outgoing parts.</span></span>
-   <span data-ttu-id="e5bc7-213">Per ogni parte in uscita, chiamare **IPartsList:: GetPart** per iniziare a attraversare il percorso dati che conduce dalla parte.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-213">For each outgoing part, call **IPartsList::GetPart** to begin to traverse the data path that leads from the part.</span></span>

<span data-ttu-id="e5bc7-214">Alcune parti, ma non necessariamente tutte, dispongono di controlli hardware associati che i client possono impostare o ottenere.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-214">Some, but not necessarily all, parts have associated hardware controls that clients can set or get.</span></span> <span data-ttu-id="e5bc7-215">Una particolare parte potrebbe avere zero, uno o più controlli hardware.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-215">A particular part might have zero, one, or more hardware controls.</span></span> <span data-ttu-id="e5bc7-216">Un controllo hardware è rappresentato dalla coppia di interfacce seguente:</span><span class="sxs-lookup"><span data-stu-id="e5bc7-216">A hardware control is represented by the following pair of interfaces:</span></span>

-   <span data-ttu-id="e5bc7-217">Interfaccia di controllo generico, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), che dispone di metodi comuni a tutti i controlli hardware.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-217">A generic control interface, [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface), which has methods that are common to all hardware controls.</span></span>
-   <span data-ttu-id="e5bc7-218">Interfaccia specifica della funzione (ad esempio, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) che espone i parametri di controllo per un particolare tipo di controllo hardware (ad esempio, un controllo del volume).</span><span class="sxs-lookup"><span data-stu-id="e5bc7-218">A function-specific interface (for example, [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)) that exposes the control parameters for a particular type of hardware control (for example, a volume control).</span></span>

<span data-ttu-id="e5bc7-219">Per enumerare i controlli hardware per una parte, il client chiama prima il metodo [**IPart:: GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) per determinare il numero di controlli hardware associati alla parte.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-219">To enumerate the hardware controls for a part, the client first calls the [**IPart::GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) method to determine the number of hardware controls that are associated with the part.</span></span> <span data-ttu-id="e5bc7-220">Successivamente, il client effettua una serie di chiamate al metodo [**IPart:: GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) per ottenere l'interfaccia **IControlInterface** per ogni controllo hardware.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-220">Next, the client makes a series of calls to the [**IPart::GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) method to obtain the **IControlInterface** interface for each hardware control.</span></span> <span data-ttu-id="e5bc7-221">Infine, il client ottiene l'interfaccia specifica della funzione per ogni controllo hardware chiamando il metodo [**IControlInterface:: GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) per ottenere l'ID di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-221">Finally, the client obtains the function-specific interface for each hardware control by calling the [**IControlInterface::GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) method to obtain the interface ID.</span></span> <span data-ttu-id="e5bc7-222">Il client chiama il metodo [**IPart:: Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) con questo ID per ottenere l'interfaccia specifica della funzione.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-222">The client calls the [**IPart::Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) method with this ID to obtain the function-specific interface.</span></span>

<span data-ttu-id="e5bc7-223">Una parte che è un connettore potrebbe supportare una delle seguenti interfacce di controllo specifiche della funzione:</span><span class="sxs-lookup"><span data-stu-id="e5bc7-223">A part that is a connector might support one of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="e5bc7-224">**IKsFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-224">**IKsFormatSupport**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [<span data-ttu-id="e5bc7-225">**IKsJackDescription**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-225">**IKsJackDescription**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

<span data-ttu-id="e5bc7-226">Una parte di un'unità secondaria potrebbe supportare una o più delle seguenti interfacce di controllo specifiche della funzione:</span><span class="sxs-lookup"><span data-stu-id="e5bc7-226">A part that is a subunit might support one or more of the following function-specific control interfaces:</span></span>

-   [<span data-ttu-id="e5bc7-227">**IAudioAutoGainControl**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-227">**IAudioAutoGainControl**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [<span data-ttu-id="e5bc7-228">**IAudioBass**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-228">**IAudioBass**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [<span data-ttu-id="e5bc7-229">**IAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-229">**IAudioChannelConfig**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [<span data-ttu-id="e5bc7-230">**IAudioInputSelector**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-230">**IAudioInputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [<span data-ttu-id="e5bc7-231">**IAudioLoudness**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-231">**IAudioLoudness**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [<span data-ttu-id="e5bc7-232">**IAudioMidrange**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-232">**IAudioMidrange**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [<span data-ttu-id="e5bc7-233">**IAudioMute**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-233">**IAudioMute**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [<span data-ttu-id="e5bc7-234">**IAudioOutputSelector**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-234">**IAudioOutputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [<span data-ttu-id="e5bc7-235">**IAudioPeakMeter**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-235">**IAudioPeakMeter**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [<span data-ttu-id="e5bc7-236">**IAudioTreble**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-236">**IAudioTreble**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [<span data-ttu-id="e5bc7-237">**IAudioVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-237">**IAudioVolumeLevel**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [<span data-ttu-id="e5bc7-238">**IDeviceSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="e5bc7-238">**IDeviceSpecificProperty**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

<span data-ttu-id="e5bc7-239">Una parte supporta l'interfaccia **IDeviceSpecificProperty** solo se il controllo hardware sottostante ha un valore di controllo specifico del dispositivo e il controllo non può essere rappresentato in modo adeguato da nessun'altra interfaccia specifica della funzione nell'elenco precedente.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-239">A part supports the **IDeviceSpecificProperty** interface only if the underlying hardware control has a device-specific control value and the control cannot be adequately represented by any other function-specific interface in the preceding list.</span></span> <span data-ttu-id="e5bc7-240">In genere, una proprietà specifica del dispositivo è utile solo per un client in grado di dedurre il significato del valore della proprietà da informazioni quali il tipo di parte, il sottotipo della parte e il nome della parte.</span><span class="sxs-lookup"><span data-stu-id="e5bc7-240">Typically, a device-specific property is useful only to a client that can infer the meaning of the property value from information such as the part type, part subtype, and part name.</span></span> <span data-ttu-id="e5bc7-241">Il client può ottenere queste informazioni chiamando i metodi [**IPart:: GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)e [**IPart:: GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) .</span><span class="sxs-lookup"><span data-stu-id="e5bc7-241">The client can obtain this information by calling the [**IPart::GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype), [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype), and [**IPart::GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5bc7-242">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5bc7-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5bc7-243">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="e5bc7-243">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
