---
title: Esempio CustomAccServer
description: .
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c047bde41bdf4a486e14ce6f293113a41ae9e285
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398674"
---
# <a name="customaccserver-sample"></a><span data-ttu-id="81610-103">Esempio CustomAccServer</span><span class="sxs-lookup"><span data-stu-id="81610-103">CustomAccServer Sample</span></span>

<span data-ttu-id="81610-104">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="81610-104">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="81610-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81610-105">Description</span></span>](#description)
-   [<span data-ttu-id="81610-106">Informazioni sul download</span><span class="sxs-lookup"><span data-stu-id="81610-106">Download Information</span></span>](#download-information)
-   [<span data-ttu-id="81610-107">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="81610-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="81610-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="81610-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="81610-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="81610-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="81610-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81610-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="81610-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81610-111">Description</span></span>

<span data-ttu-id="81610-112">Questo esempio illustra come implementare un server Microsoft Active Accessibility per un controllo personalizzato semplice.</span><span class="sxs-lookup"><span data-stu-id="81610-112">This sample shows how to implement a Microsoft Active Accessibility server for a simple custom control.</span></span> <span data-ttu-id="81610-113">L'oggetto accessibile per il controllo è costituito dall'elemento radice (casella di riepilogo) e dai relativi elementi figlio (elementi dell'elenco).</span><span class="sxs-lookup"><span data-stu-id="81610-113">The accessible object for the control consists of the root element (a list box) and its children (the list items.)</span></span>

## <a name="download-information"></a><span data-ttu-id="81610-114">Informazioni sul download</span><span class="sxs-lookup"><span data-stu-id="81610-114">Download Information</span></span>

<span data-ttu-id="81610-115">L'esempio CustomAccServer viene installato come parte del [Software Development Kit (SDK) di Microsoft Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) ed è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="81610-115">The CustomAccServer sample is installed as part of the [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="81610-116">Location</span><span class="sxs-lookup"><span data-stu-id="81610-116">Location</span></span>    | <span data-ttu-id="81610-117">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="81610-117">Path/URL</span></span>                                                                           |
|-------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81610-118">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="81610-118">Windows SDK</span></span> | <span data-ttu-id="81610-119">% Programmi% \\ Microsoft SDK \\ numero di versione di Windows \\ \[ \] \\ esempi \\ WinUI \\ MSAA</span><span class="sxs-lookup"><span data-stu-id="81610-119">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\msaa</span></span> |



 

## <a name="minimum-requirements"></a><span data-ttu-id="81610-120">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="81610-120">Minimum Requirements</span></span>



| <span data-ttu-id="81610-121">Prodotto</span><span class="sxs-lookup"><span data-stu-id="81610-121">Product</span></span>          | <span data-ttu-id="81610-122">Versione</span><span class="sxs-lookup"><span data-stu-id="81610-122">Version</span></span>                         |
|------------------|---------------------------------|
| <span data-ttu-id="81610-123">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="81610-123">Operating System</span></span> | <span data-ttu-id="81610-124">Windows XP, Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="81610-124">Windows XP, Windows Server 2003</span></span> |
| <span data-ttu-id="81610-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="81610-125">Windows SDK</span></span>      | <span data-ttu-id="81610-126">7.0</span><span class="sxs-lookup"><span data-stu-id="81610-126">7.0</span></span>                             |
| <span data-ttu-id="81610-127">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="81610-127">Visual Studio</span></span>    | <span data-ttu-id="81610-128">2008</span><span class="sxs-lookup"><span data-stu-id="81610-128">2008</span></span>                            |



 

## <a name="building-the-sample"></a><span data-ttu-id="81610-129">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="81610-129">Building the Sample</span></span>

<span data-ttu-id="81610-130">Per compilare l'esempio con Visual Studio 2008:</span><span class="sxs-lookup"><span data-stu-id="81610-130">To build the sample using Visual Studio 2008:</span></span>

1.  <span data-ttu-id="81610-131">Eseguire lo strumento di configurazione di Microsoft Windows Software Development Kit (SDK) fornito con l'SDK per aggiungere directory di inclusione SDK a Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="81610-131">Run the Microsoft Windows Software Development Kit (SDK) Configuration Tool provided with the SDK to add SDK include directories to Visual Studio.</span></span>
2.  <span data-ttu-id="81610-132">Aprire Esplora risorse e passare alla directory del progetto.</span><span class="sxs-lookup"><span data-stu-id="81610-132">Open Windows Explorer and navigate to the project directory.</span></span>
3.  <span data-ttu-id="81610-133">Fare doppio clic sull'icona del file con estensione sln (soluzione) per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="81610-133">Double-click the icon for the .sln (solution) file to open the project in Visual Studio.</span></span>
4.  <span data-ttu-id="81610-134">Scegliere **Compila soluzione** dal menu **Compila** per compilare la soluzione.</span><span class="sxs-lookup"><span data-stu-id="81610-134">On the **Build** menu, select **Build Solution** to build the solution.</span></span> <span data-ttu-id="81610-135">L'applicazione verrà compilata nella \\ directory di debug o di \\ versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="81610-135">The application will be built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="81610-136">Per compilare l'esempio dalla riga di comando, vedere compilazione di esempi nelle note sulla versione di Windows SDK nel percorso seguente:% Program Files% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ReleaseNotes.htm</span><span class="sxs-lookup"><span data-stu-id="81610-136">To build the sample from the command line, see Building Samples in the Windows SDK release notes at the following location: %Program Files%\\Microsoft SDKs\\Windows\\v7.0\\ReleaseNotes.htm</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="81610-137">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="81610-137">Running the Sample</span></span>

<span data-ttu-id="81610-138">Per eseguire l'esempio:</span><span class="sxs-lookup"><span data-stu-id="81610-138">To run the sample:</span></span>

1.  <span data-ttu-id="81610-139">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="81610-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="81610-140">Digitare AccServer.exe dalla riga di comando oppure fare doppio clic sull'icona AccServer.exe per avviarla da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="81610-140">Type AccServer.exe at the command line, or double-click the icon for AccServer.exe to launch it from Windows Explorer.</span></span>

<span data-ttu-id="81610-141">Per eseguire da Visual Studio, premere F5 o fare clic su **Avvia debug** dal menu **debug** .</span><span class="sxs-lookup"><span data-stu-id="81610-141">To run from Visual Studio, press F5 or click **Start Debugging** from the **Debug** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81610-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81610-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81610-143">Esempi</span><span class="sxs-lookup"><span data-stu-id="81610-143">Samples</span></span>](samples.md)
</dt> </dl>

 

 




