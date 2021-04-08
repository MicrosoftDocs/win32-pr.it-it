---
description: Questo esempio usa le API audio principali per implementare una visualizzazione sullo schermo che mostra le modifiche del volume al flusso di output che riproduce il dispositivo dell'endpoint di rendering audio predefinito.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: OSD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c4c04daf5d2dd333a25150821a831695e06a06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049216"
---
# <a name="osd"></a><span data-ttu-id="834ec-103">OSD</span><span class="sxs-lookup"><span data-stu-id="834ec-103">OSD</span></span>

<span data-ttu-id="834ec-104">Questo esempio usa le API audio principali per implementare una visualizzazione sullo schermo che mostra le modifiche del volume al flusso di output che riproduce il dispositivo dell'endpoint di rendering audio predefinito.</span><span class="sxs-lookup"><span data-stu-id="834ec-104">This sample uses the Core Audio APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="834ec-105">La visualizzazione sullo schermo viene visualizzata quando l'utente regola il livello del volume nel programma di controllo del volume di Windows, Sndvol.exe e scompare dopo che il livello del volume rimane invariato per un breve periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="834ec-105">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span>

<span data-ttu-id="834ec-106">Questo argomento contiene le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="834ec-106">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="834ec-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="834ec-107">Description</span></span>](#description)
-   [<span data-ttu-id="834ec-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="834ec-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="834ec-109">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="834ec-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="834ec-110">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="834ec-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="834ec-111">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="834ec-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="834ec-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="834ec-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="834ec-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="834ec-113">Description</span></span>

<span data-ttu-id="834ec-114">In questo esempio vengono illustrate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="834ec-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="834ec-115">[API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.</span><span class="sxs-lookup"><span data-stu-id="834ec-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="834ec-116">[API EndpointVolume](endpointvolume-api.md) audio</span><span class="sxs-lookup"><span data-stu-id="834ec-116">Audio [EndpointVolume API](endpointvolume-api.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="834ec-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="834ec-117">Requirements</span></span>



| <span data-ttu-id="834ec-118">Prodotto</span><span class="sxs-lookup"><span data-stu-id="834ec-118">Product</span></span>                                                        | <span data-ttu-id="834ec-119">Versione</span><span class="sxs-lookup"><span data-stu-id="834ec-119">Version</span></span>                |
|----------------------------------------------------------------|------------------------|
| [<span data-ttu-id="834ec-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="834ec-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="834ec-121">Windows Vista o versioni successive</span><span class="sxs-lookup"><span data-stu-id="834ec-121">Windows Vista or later</span></span> |
| <span data-ttu-id="834ec-122">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="834ec-122">Visual Studio</span></span>                                                  | <span data-ttu-id="834ec-123">2005 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="834ec-123">2005 or later</span></span>          |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="834ec-124">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="834ec-124">Downloading the Sample</span></span>

<span data-ttu-id="834ec-125">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="834ec-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="834ec-126">Location</span><span class="sxs-lookup"><span data-stu-id="834ec-126">Location</span></span>    | <span data-ttu-id="834ec-127">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="834ec-127">Path/URL</span></span>                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="834ec-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="834ec-128">Windows SDK</span></span> | <span data-ttu-id="834ec-129">\\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ OSD \\ ...</span><span class="sxs-lookup"><span data-stu-id="834ec-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\OSD\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="834ec-130">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="834ec-130">Building the Sample</span></span>

1.  <span data-ttu-id="834ec-131">Aprire la shell CMD per la Windows SDK e passare alla directory di esempio OSD.</span><span class="sxs-lookup"><span data-stu-id="834ec-131">Open the CMD shell for the Windows SDK and change to the OSD sample directory.</span></span>
2.  <span data-ttu-id="834ec-132">Eseguire il comando "Start OSD. sln" nella directory OSD per aprire il progetto OSD nella finestra di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="834ec-132">Run the command "start OSD.sln" in the OSD directory to open the OSD project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="834ec-133">Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** .</span><span class="sxs-lookup"><span data-stu-id="834ec-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="834ec-134">Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="834ec-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="834ec-135">In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto OSD. vcproj.</span><span class="sxs-lookup"><span data-stu-id="834ec-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, OSD.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="834ec-136">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="834ec-136">Running the Sample</span></span>

1.  <span data-ttu-id="834ec-137">Eseguire il file eseguibile OSD, OSD.exe, in Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="834ec-137">Run the OSD executable file, OSD.exe, in Windows Vista or later.</span></span> <span data-ttu-id="834ec-138">Si noti che non viene visualizzata un'icona della barra delle applicazioni o una finestra per l'applicazione, ma è possibile vedere il processo in esecuzione utilizzando TaskMgr.exe.</span><span class="sxs-lookup"><span data-stu-id="834ec-138">Note that you will not see a system tray icon or a window for the application, but you can see the process running using TaskMgr.exe.</span></span>
2.  <span data-ttu-id="834ec-139">Eseguire sndvol.exe per modificare il volume o il mute oppure modificare il volume utilizzando i controlli della tastiera o un controllo nascosto.</span><span class="sxs-lookup"><span data-stu-id="834ec-139">Run sndvol.exe to change the volume or mute, or change the volume using keyboard controls or an HID control.</span></span> <span data-ttu-id="834ec-140">Verrà visualizzata l'interfaccia utente OSD.</span><span class="sxs-lookup"><span data-stu-id="834ec-140">The OSD user interface is displayed.</span></span>
3.  <span data-ttu-id="834ec-141">Per uscire dall'applicazione, eseguire TaskMgr.exe, evidenziare il processo di OSD.exe e fare clic su **Termina processo**.</span><span class="sxs-lookup"><span data-stu-id="834ec-141">To exit the application, run TaskMgr.exe, highlight the OSD.exe process and click **End Process**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="834ec-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="834ec-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="834ec-143">Esempi di SDK che usano le API audio principali</span><span class="sxs-lookup"><span data-stu-id="834ec-143">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



