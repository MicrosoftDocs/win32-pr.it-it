---
description: File di intestazione e componenti di sistema
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: File di intestazione e componenti di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4b93c63e7d32944dfdf2bf6872bd3a3153e4a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127439"
---
# <a name="header-files-and-system-components"></a><span data-ttu-id="06e0e-103">File di intestazione e componenti di sistema</span><span class="sxs-lookup"><span data-stu-id="06e0e-103">Header Files and System Components</span></span>

<span data-ttu-id="06e0e-104">Nella tabella seguente sono elencati i file di intestazione che contengono le definizioni di interfaccia per i quattro componenti audio principali.</span><span class="sxs-lookup"><span data-stu-id="06e0e-104">The following table lists the header files that contain the interface definitions for the four Core Audio components.</span></span>



|                                              |                              |
|----------------------------------------------|------------------------------|
| <span data-ttu-id="06e0e-105">Componente audio principale</span><span class="sxs-lookup"><span data-stu-id="06e0e-105">Core Audio component</span></span>                         | <span data-ttu-id="06e0e-106">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="06e0e-106">Header file</span></span>                  |
| [<span data-ttu-id="06e0e-107">API MMDevice</span><span class="sxs-lookup"><span data-stu-id="06e0e-107">MMDevice API</span></span>](mmdevice-api.md)             | <span data-ttu-id="06e0e-108">Mmdeviceapi. h</span><span class="sxs-lookup"><span data-stu-id="06e0e-108">Mmdeviceapi.h</span></span>                |
| [<span data-ttu-id="06e0e-109">WASAPI</span><span class="sxs-lookup"><span data-stu-id="06e0e-109">WASAPI</span></span>](wasapi.md)                         | <span data-ttu-id="06e0e-110">Audioclient. h, Audiopolicy. h</span><span class="sxs-lookup"><span data-stu-id="06e0e-110">Audioclient.h, Audiopolicy.h</span></span> |
| [<span data-ttu-id="06e0e-111">API DeviceTopology</span><span class="sxs-lookup"><span data-stu-id="06e0e-111">DeviceTopology API</span></span>](devicetopology-api.md) | <span data-ttu-id="06e0e-112">Devicetopology. h</span><span class="sxs-lookup"><span data-stu-id="06e0e-112">Devicetopology.h</span></span>             |
| [<span data-ttu-id="06e0e-113">API EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="06e0e-113">EndpointVolume API</span></span>](endpointvolume-api.md) | <span data-ttu-id="06e0e-114">Endpointvolume. h</span><span class="sxs-lookup"><span data-stu-id="06e0e-114">Endpointvolume.h</span></span>             |



 

<span data-ttu-id="06e0e-115">Un altro file di intestazione, Audiosessiontypes. h, definisce le costanti usate da WASAPI.</span><span class="sxs-lookup"><span data-stu-id="06e0e-115">Another header file, Audiosessiontypes.h, defines constants that are used by WASAPI.</span></span> <span data-ttu-id="06e0e-116">Questi file di intestazione si trovano nella directory% MSSdk% \\ include, dove% MSSdk% è la directory radice dell'installazione del Windows SDK nel computer.</span><span class="sxs-lookup"><span data-stu-id="06e0e-116">These header files are located in the directory %MSSdk%\\include, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>

<span data-ttu-id="06e0e-117">Ogni API nella tabella precedente è costituita da un set di interfacce COM correlate.</span><span class="sxs-lookup"><span data-stu-id="06e0e-117">Each API in the preceding table consists of a set of related COM interfaces.</span></span> <span data-ttu-id="06e0e-118">Poiché alcuni aspetti del flusso audio dipendono dalla bassa latenza e dalla sincronizzazione precisa, le implementazioni delle API MMDevice, WASAPI, DeviceTopology e EndpointVolume non utilizzano il Framework Microsoft .NET o l'ambiente di esecuzione gestita.</span><span class="sxs-lookup"><span data-stu-id="06e0e-118">Because some aspects of audio streaming depend on low latency and precise synchronization, the implementations of the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs do not use the Microsoft .NET Framework or managed-execution environment.</span></span>

<span data-ttu-id="06e0e-119">Le API audio principali vengono implementate nei componenti di sistema in modalità utente Audioses.dll e Mmdevapi.dll.</span><span class="sxs-lookup"><span data-stu-id="06e0e-119">The Core Audio APIs are implemented in the user-mode system components Audioses.dll and Mmdevapi.dll.</span></span> <span data-ttu-id="06e0e-120">Le applicazioni client non accedono direttamente ai punti di ingresso di queste dll.</span><span class="sxs-lookup"><span data-stu-id="06e0e-120">Client applications do not access the entry points in these DLLs directly.</span></span> <span data-ttu-id="06e0e-121">Al contrario, i client chiamano la funzione **CoCreateInstance** o **CoCreateInstanceEx** per ottenere l'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) dell'oggetto della classe MMDeviceEnumerator.</span><span class="sxs-lookup"><span data-stu-id="06e0e-121">Instead, clients call the **CoCreateInstance** or **CoCreateInstanceEx** function to obtain the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface of the MMDeviceEnumerator class object.</span></span> <span data-ttu-id="06e0e-122">Questo oggetto enumera i [dispositivi dell'endpoint audio](audio-endpoint-devices.md) nel sistema.</span><span class="sxs-lookup"><span data-stu-id="06e0e-122">This object enumerates the [audio endpoint devices](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="06e0e-123">L'interfaccia **IMMDeviceEnumerator** fa parte dell'API MMDevice.</span><span class="sxs-lookup"><span data-stu-id="06e0e-123">The **IMMDeviceEnumerator** interface is part of the MMDevice API.</span></span> <span data-ttu-id="06e0e-124">Da questa interfaccia, i client possono ottenere direttamente o indirettamente le altre interfacce nell'API MMDevice, inclusa l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) .</span><span class="sxs-lookup"><span data-stu-id="06e0e-124">From this interface, clients can directly or indirectly obtain the other interfaces in the MMDevice API, including the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span> <span data-ttu-id="06e0e-125">**IMMDevice** rappresenta un dispositivo dell'endpoint audio specifico.</span><span class="sxs-lookup"><span data-stu-id="06e0e-125">**IMMDevice** represents a particular audio endpoint device.</span></span> <span data-ttu-id="06e0e-126">Tramite **IMMDevice**, i client possono ottenere direttamente o indirettamente le interfacce specifiche del dispositivo in WASAPI, l'API DeviceTopology e l'API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="06e0e-126">Through **IMMDevice**, clients can directly or indirectly obtain the device-specific interfaces in WASAPI, the DeviceTopology API, and the EndpointVolume API.</span></span> <span data-ttu-id="06e0e-127">Per ulteriori informazioni su **CoCreateInstance** e **CoCreateInstanceEx**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="06e0e-127">For more information about **CoCreateInstance** and **CoCreateInstanceEx**, see the Windows SDK documentation.</span></span> <span data-ttu-id="06e0e-128">Per altre informazioni sull'accesso alle interfacce nelle API principali dell'audio, vedere [enumerazione dei dispositivi audio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="06e0e-128">For more information about accessing the interfaces in the Core Audio APIs, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06e0e-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06e0e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06e0e-130">Informazioni sulle API audio di Windows Core</span><span class="sxs-lookup"><span data-stu-id="06e0e-130">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



