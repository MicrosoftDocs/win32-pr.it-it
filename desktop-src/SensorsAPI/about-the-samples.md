---
description: Il Windows SDK include utili esempi di codice e strumenti che consentono di comprendere e usare la piattaforma del sensore e della posizione di Windows e le API correlate.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: Informazioni sugli esempi e sugli strumenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126ec5e07829cfd17c2b07313bb104140c6fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884262"
---
# <a name="about-the-samples-and-tools"></a><span data-ttu-id="234a0-103">Informazioni sugli esempi e sugli strumenti</span><span class="sxs-lookup"><span data-stu-id="234a0-103">About the Samples and Tools</span></span>

<span data-ttu-id="234a0-104">Il Windows SDK include utili esempi di codice e strumenti che consentono di comprendere e usare la piattaforma del sensore e della posizione di Windows e le API correlate.</span><span class="sxs-lookup"><span data-stu-id="234a0-104">The Windows SDK includes useful code samples and tools to help you understand and use the Windows Sensor and Location platform and related APIs.</span></span>

## <a name="samples"></a><span data-ttu-id="234a0-105">Esempi</span><span class="sxs-lookup"><span data-stu-id="234a0-105">Samples</span></span>

<span data-ttu-id="234a0-106">Il Windows SDK include i seguenti esempi di API per i sensori.</span><span class="sxs-lookup"><span data-stu-id="234a0-106">The Windows SDK includes the following Sensor API samples.</span></span> <span data-ttu-id="234a0-107">È possibile trovare gli esempi di API per i sensori nella cartella denominata \\ Samples \\ WinUI \\ Sensors, in cui è stato installato il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="234a0-107">You can find the Sensor API samples in the folder named \\Samples\\winui\\Sensors, where you installed the Windows SDK.</span></span> <span data-ttu-id="234a0-108">Se, ad esempio, è stato installato il Windows SDK sull'unità C, gli esempi sono disponibili nella cartella seguente: C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ WinUI \\ sensori.</span><span class="sxs-lookup"><span data-stu-id="234a0-108">For example, if you installed the Windows SDK on drive C, you would find the samples in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\winui\\Sensors.</span></span>



| <span data-ttu-id="234a0-109">Nome esempio</span><span class="sxs-lookup"><span data-stu-id="234a0-109">Sample name</span></span>       | <span data-ttu-id="234a0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="234a0-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="234a0-111">AmbientLightAware</span><span class="sxs-lookup"><span data-stu-id="234a0-111">AmbientLightAware</span></span> | <span data-ttu-id="234a0-112">Questo esempio MFC illustra come usare l'API del sensore leggendo i dati dai sensori di luce di ambiente sul computer e modificando le dimensioni del testo in base alle condizioni di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="234a0-112">This MFC sample shows how to use the Sensor API by reading data from ambient light sensors on the computer and changing text size according to the lighting conditions.</span></span> <span data-ttu-id="234a0-113">È possibile visualizzare il codice che illustra come gestire gli eventi e come richiedere le autorizzazioni utente.</span><span class="sxs-lookup"><span data-stu-id="234a0-113">You can see code that shows how to manage events and how to request user permissions.</span></span> <span data-ttu-id="234a0-114">È anche possibile vedere un esempio di come gestire l'interfaccia utente in base a condizioni di illuminazione diverse.</span><span class="sxs-lookup"><span data-stu-id="234a0-114">You can also see an example of how to manage the user interface based on varying lighting conditions.</span></span> <span data-ttu-id="234a0-115">Per ulteriori informazioni, vedere [creazione di Light-Aware interfacce utente](creating-light-aware-user-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="234a0-115">For more information, see [Creating Light-Aware User Interfaces](creating-light-aware-user-interfaces.md).</span></span><br/> <span data-ttu-id="234a0-116">Per compilare questo esempio, è necessario che Visual Studio 2008 sia installato.</span><span class="sxs-lookup"><span data-stu-id="234a0-116">You must have Visual Studio 2008 installed to build this sample.</span></span><br/> |



 

<span data-ttu-id="234a0-117">Per ulteriori informazioni, vedere il file denominato ReadMe.txt incluso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="234a0-117">For more information, see the file named ReadMe.txt that is included with the sample.</span></span>

<span data-ttu-id="234a0-118">È anche possibile scaricare l'esempio AmbientLightAware da Code Gallery.</span><span class="sxs-lookup"><span data-stu-id="234a0-118">You can also download the AmbientLightAware sample from Code Gallery.</span></span> <span data-ttu-id="234a0-119">Per ulteriori informazioni, vedere la pagina di download con rilevamento [chiaro di ambiente](/samples/browse/?redirectedfrom=MSDN-samples) .</span><span class="sxs-lookup"><span data-stu-id="234a0-119">For more information, see the [Ambient Light Aware](/samples/browse/?redirectedfrom=MSDN-samples) download page.</span></span>

## <a name="tools"></a><span data-ttu-id="234a0-120">Strumenti</span><span class="sxs-lookup"><span data-stu-id="234a0-120">Tools</span></span>

<span data-ttu-id="234a0-121">Il Windows SDK include un sensore di luce virtuale che è possibile usare per simulare un dispositivo sensore di luce basato su hardware.</span><span class="sxs-lookup"><span data-stu-id="234a0-121">The Windows SDK includes a virtual light sensor that you can use to simulate a hardware-based light sensor device.</span></span> <span data-ttu-id="234a0-122">È possibile usare questo strumento per fornire dati all'esempio AmbientLightAware per vedere come funziona il codice nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="234a0-122">You can use this tool to provide data to the AmbientLightAware sample to see how the code in the sample works.</span></span>

<span data-ttu-id="234a0-123">La tabella seguente descrive i file che è necessario usare per eseguire il sensore di luce virtuale.</span><span class="sxs-lookup"><span data-stu-id="234a0-123">The following table describes the files you must use to run the virtual light sensor.</span></span> <span data-ttu-id="234a0-124">È possibile trovare questi file nella cartella denominata bin, in cui è stato installato il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="234a0-124">You can find these files in the folder named Bin, where you installed the Windows SDK.</span></span> <span data-ttu-id="234a0-125">Se, ad esempio, è stato installato il Windows SDK sull'unità C in un computer a 32 bit, i file del sensore di luce virtuale saranno disponibili nella cartella seguente: C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ bin.</span><span class="sxs-lookup"><span data-stu-id="234a0-125">For example, if you installed the Windows SDK on drive C on a 32-bit computer, you would find the virtual light sensor files in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Bin.</span></span> <span data-ttu-id="234a0-126">Nei computer a 64 bit, è necessario utilizzare la versione a 64 bit dello strumento.</span><span class="sxs-lookup"><span data-stu-id="234a0-126">On 64-bit computers, you must use the 64-bit version of the tool.</span></span> <span data-ttu-id="234a0-127">Nella Windows SDK gli strumenti a 64 bit si trovano nella sottocartella denominata x64.</span><span class="sxs-lookup"><span data-stu-id="234a0-127">In the Windows SDK, 64-bit tools are located in the subfolder named x64.</span></span>



| <span data-ttu-id="234a0-128">Nome file</span><span class="sxs-lookup"><span data-stu-id="234a0-128">File name</span></span>                    | <span data-ttu-id="234a0-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="234a0-129">Description</span></span>                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="234a0-130">VirtualLightSensor.exe</span><span class="sxs-lookup"><span data-stu-id="234a0-130">VirtualLightSensor.exe</span></span>       | <span data-ttu-id="234a0-131">Questo programma fornisce un controllo dispositivo di scorrimento che consente di modificare il livello dei dati leggeri segnalati dal sensore virtuale.</span><span class="sxs-lookup"><span data-stu-id="234a0-131">This program provides a slider control that enables you to change the level of the light data that the virtual sensor reports.</span></span> |
| <span data-ttu-id="234a0-132">VirtualLightSensorDriver.dll</span><span class="sxs-lookup"><span data-stu-id="234a0-132">VirtualLightSensorDriver.dll</span></span> | <span data-ttu-id="234a0-133">Driver del sensore logico che simula un sensore di luminosità.</span><span class="sxs-lookup"><span data-stu-id="234a0-133">The logical sensor driver that simulates a light sensor.</span></span>                                                                       |
| <span data-ttu-id="234a0-134">VirtualLightSensorDriver. inf</span><span class="sxs-lookup"><span data-stu-id="234a0-134">VirtualLightSensorDriver.inf</span></span> | <span data-ttu-id="234a0-135">File INF per il driver del sensore di luce virtuale.</span><span class="sxs-lookup"><span data-stu-id="234a0-135">The INF file for the virtual light sensor driver.</span></span>                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a><span data-ttu-id="234a0-136">Installazione del sensore di luce virtuale</span><span class="sxs-lookup"><span data-stu-id="234a0-136">Installing the Virtual Light Sensor</span></span>

<span data-ttu-id="234a0-137">Prima di usare l'applicazione Virtual Light Sensor, è necessario installare il driver del sensore logico.</span><span class="sxs-lookup"><span data-stu-id="234a0-137">Before you use the virtual light sensor application, you must install the logical sensor driver.</span></span> <span data-ttu-id="234a0-138">A tale scopo, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="234a0-138">Follow these steps:</span></span>

1.  <span data-ttu-id="234a0-139">Aprire una finestra di comando come amministratore.</span><span class="sxs-lookup"><span data-stu-id="234a0-139">Open a command window as an administrator.</span></span>
2.  <span data-ttu-id="234a0-140">Passare alla cartella bin Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="234a0-140">Change to the Windows SDK Bin folder.</span></span>
3.  <span data-ttu-id="234a0-141">Digitare **pnputil-a VirtualLightSensorDriver. inf**.</span><span class="sxs-lookup"><span data-stu-id="234a0-141">Type **pnputil -a VirtualLightSensorDriver.inf**.</span></span>
4.  <span data-ttu-id="234a0-142">Quando richiesto, fare clic su **installa comunque il software driver**.</span><span class="sxs-lookup"><span data-stu-id="234a0-142">When prompted, click **Install this driver software anyway**.</span></span>
5.  <span data-ttu-id="234a0-143">Attendere che la finestra di comando segnali che il driver è stato installato correttamente.</span><span class="sxs-lookup"><span data-stu-id="234a0-143">Wait for the command window to report that the driver was successfully installed.</span></span>

### <a name="running-the-virtual-light-sensor"></a><span data-ttu-id="234a0-144">Esecuzione del sensore di luce virtuale</span><span class="sxs-lookup"><span data-stu-id="234a0-144">Running the Virtual Light Sensor</span></span>

<span data-ttu-id="234a0-145">Per eseguire il sensore di luce virtuale, è sufficiente fare doppio clic sul file exe.</span><span class="sxs-lookup"><span data-stu-id="234a0-145">To run the virtual light sensor, simply double-click the .exe file.</span></span> <span data-ttu-id="234a0-146">Assicurarsi di abilitare il sensore quando richiesto.</span><span class="sxs-lookup"><span data-stu-id="234a0-146">Be sure to enable the sensor, when prompted.</span></span>

<span data-ttu-id="234a0-147">Quando si esegue il programma, è possibile notare che si verifica un ritardo prima che il sensore diventi disponibile.</span><span class="sxs-lookup"><span data-stu-id="234a0-147">When you run the program, you may notice that there is a delay before the sensor becomes available.</span></span> <span data-ttu-id="234a0-148">L'interfaccia utente del sensore di luce virtuale visualizzerà il messaggio "Waiting" sulla barra del titolo mentre Gestione sensori logici creerà un nodo del dispositivo per il sensore logico.</span><span class="sxs-lookup"><span data-stu-id="234a0-148">The virtual light sensor user interface will display the message "Waiting" in the title bar while the logical sensor manager creates a device node for the logical sensor.</span></span> <span data-ttu-id="234a0-149">Quando il messaggio in attesa scompare, è possibile usare il dispositivo di scorrimento per impostare il livello di output Lux per il sensore di luce virtuale.</span><span class="sxs-lookup"><span data-stu-id="234a0-149">After the waiting message goes away, you can use the slider to set the lux output level for the virtual light sensor.</span></span>

<span data-ttu-id="234a0-150">La figura seguente mostra l'interfaccia utente del sensore di luce virtuale nello stato pronto.</span><span class="sxs-lookup"><span data-stu-id="234a0-150">The following image shows the virtual light sensor user interface in its ready state.</span></span>

![interfaccia utente del sensore di luce virtuale](images/virtuallightsensor.png)

## <a name="related-topics"></a><span data-ttu-id="234a0-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="234a0-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="234a0-153">Informazioni sui sensori logici</span><span class="sxs-lookup"><span data-stu-id="234a0-153">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> <dt>

[<span data-ttu-id="234a0-154">**\_categoria sensore \_ chiaro**</span><span class="sxs-lookup"><span data-stu-id="234a0-154">**SENSOR\_CATEGORY\_LIGHT**</span></span>](sensor-category-light.md)
</dt> </dl>

 

