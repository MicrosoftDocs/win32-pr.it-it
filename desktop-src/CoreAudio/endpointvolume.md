---
description: Questa applicazione di esempio usa le API audio principali per modificare il volume del dispositivo, come specificato dall'utente.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483492"
---
# <a name="endpointvolume"></a><span data-ttu-id="9cd8c-103">EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="9cd8c-103">EndpointVolume</span></span>

<span data-ttu-id="9cd8c-104">Questa applicazione di esempio usa le API audio principali per modificare il volume del dispositivo, come specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-104">This sample application uses the Core Audio APIs to change the volume of the device, as specified by the user.</span></span>

<span data-ttu-id="9cd8c-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9cd8c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cd8c-106">Description</span></span>](#description)
-   [<span data-ttu-id="9cd8c-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cd8c-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9cd8c-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9cd8c-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="9cd8c-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9cd8c-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="9cd8c-110">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9cd8c-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="9cd8c-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9cd8c-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="9cd8c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cd8c-112">Description</span></span>

<span data-ttu-id="9cd8c-113">In questo esempio vengono illustrate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-113">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="9cd8c-114">[API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-114">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="9cd8c-115">[API EndpointVolume](endpointvolume-api.md) per controllare i livelli di volume dell'endpoint del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-115">[EndpointVolume API](endpointvolume-api.md) to control volume levels of the device endpoint.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cd8c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cd8c-116">Requirements</span></span>



| <span data-ttu-id="9cd8c-117">Prodotto</span><span class="sxs-lookup"><span data-stu-id="9cd8c-117">Product</span></span>                                                        | <span data-ttu-id="9cd8c-118">Versione</span><span class="sxs-lookup"><span data-stu-id="9cd8c-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="9cd8c-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="9cd8c-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="9cd8c-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cd8c-120">Windows 7</span></span> |
| <span data-ttu-id="9cd8c-121">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9cd8c-121">Visual Studio</span></span>                                                  | <span data-ttu-id="9cd8c-122">2008</span><span class="sxs-lookup"><span data-stu-id="9cd8c-122">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="9cd8c-123">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9cd8c-123">Downloading the Sample</span></span>

<span data-ttu-id="9cd8c-124">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-124">This sample is available in the following locations.</span></span>



| <span data-ttu-id="9cd8c-125">Location</span><span class="sxs-lookup"><span data-stu-id="9cd8c-125">Location</span></span>    | <span data-ttu-id="9cd8c-126">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="9cd8c-126">Path/URL</span></span>                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd8c-127">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="9cd8c-127">Windows SDK</span></span> | <span data-ttu-id="9cd8c-128">\\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ EndpointVolume \\ ...</span><span class="sxs-lookup"><span data-stu-id="9cd8c-128">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\EndpointVolume\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="9cd8c-129">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9cd8c-129">Building the Sample</span></span>

<span data-ttu-id="9cd8c-130">Per compilare l'esempio x, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="9cd8c-130">To build the x sample, use the following steps:</span></span>

<span data-ttu-id="9cd8c-131">Per compilare l'esempio EndpointVolumeChanger, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="9cd8c-131">To build the EndpointVolumeChanger sample, use the following steps:</span></span>

1.  <span data-ttu-id="9cd8c-132">Aprire la shell CMD per la Windows SDK e passare alla directory di esempio EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-132">Open the CMD shell for the Windows SDK and change to the EndpointVolume sample directory.</span></span>
2.  <span data-ttu-id="9cd8c-133">Eseguire il comando `start EndpointVolumeChanger.sln` nella directory EndpointVolume per aprire il progetto EndpointVolumeChanger nella finestra di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-133">Run the command `start EndpointVolumeChanger.sln` in the EndpointVolume directory to open the EndpointVolumeChanger project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="9cd8c-134">Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** .</span><span class="sxs-lookup"><span data-stu-id="9cd8c-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="9cd8c-135">Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="9cd8c-136">In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, WASAPIEndpointVolume. vcproj.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIEndpointVolume.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="9cd8c-137">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9cd8c-137">Running the Sample</span></span>

<span data-ttu-id="9cd8c-138">Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile EndpointVolumeChanger.exe.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-138">If you build the demo application successfully, an executable file, EndpointVolumeChanger.exe, is generated.</span></span> <span data-ttu-id="9cd8c-139">Per eseguirlo, digitare `EndpointVolumeChanger` in una finestra di comando seguita da argomenti obbligatori o facoltativi.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-139">To run it, type `EndpointVolumeChanger` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="9cd8c-140">Nell'esempio seguente viene illustrato come attivare o disattivare l'impostazione di silenziamento sul dispositivo predefinito della console.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-140">The following example shows how to toggle the mute setting on the default console device.</span></span>

`EndpointVolumeChanger.exe -console -m`

<span data-ttu-id="9cd8c-141">La tabella seguente illustra gli argomenti.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-141">The following table shows the arguments.</span></span>

| <span data-ttu-id="9cd8c-142">Argomento</span><span class="sxs-lookup"><span data-stu-id="9cd8c-142">Argument</span></span>        | <span data-ttu-id="9cd8c-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cd8c-143">Description</span></span>                                                         |
|-----------------|---------------------------------------------------------------------|
| <span data-ttu-id="9cd8c-144">-?</span><span class="sxs-lookup"><span data-stu-id="9cd8c-144">-?</span></span>              | <span data-ttu-id="9cd8c-145">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-145">Shows help.</span></span>                                                         |
| <span data-ttu-id="9cd8c-146">-H</span><span class="sxs-lookup"><span data-stu-id="9cd8c-146">-h</span></span>              | <span data-ttu-id="9cd8c-147">Visualizza la guida.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-147">Shows help.</span></span>                                                         |
| -+              | <span data-ttu-id="9cd8c-148">Incrementa il livello del volume sul dispositivo dell'endpoint audio di un solo passaggio.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-148">Increments the volume level on audio endpoint device by one step.</span></span> <span data-ttu-id="9cd8c-149">.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-149">.</span></span> |
| <span data-ttu-id="9cd8c-150">-su</span><span class="sxs-lookup"><span data-stu-id="9cd8c-150">-up</span></span>             | <span data-ttu-id="9cd8c-151">Incrementa il livello del volume sul dispositivo dell'endpoint audio di un solo passaggio.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-151">Increments the volume level on audio endpoint device by one step.</span></span>   |
| --              | <span data-ttu-id="9cd8c-152">Decrementa del livello del volume sul dispositivo dell'endpoint audio di un solo passaggio.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-152">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="9cd8c-153">-giù</span><span class="sxs-lookup"><span data-stu-id="9cd8c-153">-down</span></span>           | <span data-ttu-id="9cd8c-154">Decrementa del livello del volume sul dispositivo dell'endpoint audio di un solo passaggio.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-154">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="9cd8c-155">-v</span><span class="sxs-lookup"><span data-stu-id="9cd8c-155">-v</span></span>              | <span data-ttu-id="9cd8c-156">Imposta il livello del volume master sul dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-156">Sets the master volume level on the audio endpoint device.</span></span>          |
| <span data-ttu-id="9cd8c-157">-Console</span><span class="sxs-lookup"><span data-stu-id="9cd8c-157">-console</span></span>        | <span data-ttu-id="9cd8c-158">Usare il dispositivo console predefinito.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-158">Use the default console device.</span></span>                                     |
| <span data-ttu-id="9cd8c-159">-comunicazioni</span><span class="sxs-lookup"><span data-stu-id="9cd8c-159">-communications</span></span> | <span data-ttu-id="9cd8c-160">Usare il dispositivo di comunicazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-160">Use the default communication device.</span></span>                               |
| <span data-ttu-id="9cd8c-161">-Multimedia</span><span class="sxs-lookup"><span data-stu-id="9cd8c-161">-multimedia</span></span>     | <span data-ttu-id="9cd8c-162">Usare il dispositivo multimediale predefinito.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-162">Use the default multimedia device.</span></span>                                  |
| <span data-ttu-id="9cd8c-163">-endpoint</span><span class="sxs-lookup"><span data-stu-id="9cd8c-163">-endpoint</span></span>       | <span data-ttu-id="9cd8c-164">Usare l'identificatore dell'endpoint specificato nel valore dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-164">Use the endpoint identifier specified in the switch value.</span></span>          |



 

<span data-ttu-id="9cd8c-165">Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e chiede all'utente di selezionare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device.</span></span> <span data-ttu-id="9cd8c-166">Dopo che l'utente ha specificato il dispositivo, l'applicazione Visualizza le impostazioni correnti del volume per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-166">After the user specifies the device, the application displays the current volume settings for the endpoint.</span></span> <span data-ttu-id="9cd8c-167">Il volume può essere controllato usando le opzioni descritte nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="9cd8c-167">The volume can be controlled by using the switches described in the preceding table.</span></span>

<span data-ttu-id="9cd8c-168">Per altre informazioni sul controllo dei livelli di volume dei dispositivi dell'endpoint audio, vedere [API EndpointVolume](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="9cd8c-168">For more information about controlling the volume levels of audio endpoint devices, see [EndpointVolume API](endpointvolume-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cd8c-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9cd8c-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cd8c-170">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="9cd8c-170">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



