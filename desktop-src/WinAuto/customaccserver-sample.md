---
title: Esempio di CustomAccServer
description: Esempio di CustomAccServer
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f8ee7d82361177af07aa7ad53a6137c39bc38
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088009"
---
# <a name="customaccserver-sample"></a><span data-ttu-id="17be6-103">Esempio di CustomAccServer</span><span class="sxs-lookup"><span data-stu-id="17be6-103">CustomAccServer Sample</span></span>

<span data-ttu-id="17be6-104">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="17be6-104">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="17be6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17be6-105">Description</span></span>](#description)
-   [<span data-ttu-id="17be6-106">Informazioni sul download</span><span class="sxs-lookup"><span data-stu-id="17be6-106">Download Information</span></span>](#download-information)
-   [<span data-ttu-id="17be6-107">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="17be6-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="17be6-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="17be6-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="17be6-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="17be6-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="17be6-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17be6-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="17be6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17be6-111">Description</span></span>

<span data-ttu-id="17be6-112">In questo esempio viene illustrato come implementare un Microsoft Active Accessibility server per un controllo personalizzato semplice.</span><span class="sxs-lookup"><span data-stu-id="17be6-112">This sample shows how to implement a Microsoft Active Accessibility server for a simple custom control.</span></span> <span data-ttu-id="17be6-113">L'oggetto accessibile per il controllo è costituito dall'elemento radice (una casella di riepilogo) e dai relativi elementi figlio (gli elementi elenco).</span><span class="sxs-lookup"><span data-stu-id="17be6-113">The accessible object for the control consists of the root element (a list box) and its children (the list items.)</span></span>

## <a name="download-information"></a><span data-ttu-id="17be6-114">Informazioni sul download</span><span class="sxs-lookup"><span data-stu-id="17be6-114">Download Information</span></span>

<span data-ttu-id="17be6-115">L'esempio CustomAccServer viene installato come parte di [Microsoft Windows Software Development Kit (Windows SDK) (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) ed è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="17be6-115">The CustomAccServer sample is installed as part of the [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="17be6-116">Località</span><span class="sxs-lookup"><span data-stu-id="17be6-116">Location</span></span>    | <span data-ttu-id="17be6-117">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="17be6-117">Path/URL</span></span>                                                                           |
|-------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17be6-118">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="17be6-118">Windows SDK</span></span> | <span data-ttu-id="17be6-119">%Programmi% \\ Microsoft SDKs Numero di \\ versione di Windows Esempi \\ \[ \] \\ \\ winui \\ msaa</span><span class="sxs-lookup"><span data-stu-id="17be6-119">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\msaa</span></span> |



 

## <a name="minimum-requirements"></a><span data-ttu-id="17be6-120">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="17be6-120">Minimum Requirements</span></span>



| <span data-ttu-id="17be6-121">Prodotto</span><span class="sxs-lookup"><span data-stu-id="17be6-121">Product</span></span>          | <span data-ttu-id="17be6-122">Versione</span><span class="sxs-lookup"><span data-stu-id="17be6-122">Version</span></span>                         |
|------------------|---------------------------------|
| <span data-ttu-id="17be6-123">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="17be6-123">Operating System</span></span> | <span data-ttu-id="17be6-124">Windows XP, Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17be6-124">Windows XP, Windows Server 2003</span></span> |
| <span data-ttu-id="17be6-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="17be6-125">Windows SDK</span></span>      | <span data-ttu-id="17be6-126">7.0</span><span class="sxs-lookup"><span data-stu-id="17be6-126">7.0</span></span>                             |
| <span data-ttu-id="17be6-127">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="17be6-127">Visual Studio</span></span>    | <span data-ttu-id="17be6-128">2008</span><span class="sxs-lookup"><span data-stu-id="17be6-128">2008</span></span>                            |



 

## <a name="building-the-sample"></a><span data-ttu-id="17be6-129">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="17be6-129">Building the Sample</span></span>

<span data-ttu-id="17be6-130">Per compilare l'esempio Visual Studio 2008:</span><span class="sxs-lookup"><span data-stu-id="17be6-130">To build the sample using Visual Studio 2008:</span></span>

1.  <span data-ttu-id="17be6-131">Eseguire lo strumento di configurazione microsoft Windows Software Development Kit (Windows SDK) (SDK) fornito con l'SDK per aggiungere le directory di inclusione dell'SDK Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="17be6-131">Run the Microsoft Windows Software Development Kit (SDK) Configuration Tool provided with the SDK to add SDK include directories to Visual Studio.</span></span>
2.  <span data-ttu-id="17be6-132">Aprire Esplora risorse e passare alla directory del progetto.</span><span class="sxs-lookup"><span data-stu-id="17be6-132">Open Windows Explorer and navigate to the project directory.</span></span>
3.  <span data-ttu-id="17be6-133">Fare doppio clic sull'icona per il file con estensione sln (soluzione) per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="17be6-133">Double-click the icon for the .sln (solution) file to open the project in Visual Studio.</span></span>
4.  <span data-ttu-id="17be6-134">Scegliere **Compila** soluzione dal menu Compila **per** compilare la soluzione.</span><span class="sxs-lookup"><span data-stu-id="17be6-134">On the **Build** menu, select **Build Solution** to build the solution.</span></span> <span data-ttu-id="17be6-135">L'applicazione verrà compilata nella \\ directory Debug o Release \\ predefinita.</span><span class="sxs-lookup"><span data-stu-id="17be6-135">The application will be built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="17be6-136">Per compilare l'esempio dalla riga di comando, vedere Building Samples (Compilazione di esempi) nelle note sulla versione di Windows SDK nel percorso seguente: %Program Files% \\ Microsoft SDKs \\ Windows \\ v7.0 \\ReleaseNotes.htm</span><span class="sxs-lookup"><span data-stu-id="17be6-136">To build the sample from the command line, see Building Samples in the Windows SDK release notes at the following location: %Program Files%\\Microsoft SDKs\\Windows\\v7.0\\ReleaseNotes.htm</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="17be6-137">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="17be6-137">Running the Sample</span></span>

<span data-ttu-id="17be6-138">Per eseguire l'esempio:</span><span class="sxs-lookup"><span data-stu-id="17be6-138">To run the sample:</span></span>

1.  <span data-ttu-id="17be6-139">Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="17be6-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="17be6-140">Digitare AccServer.exe nella riga di comando oppure fare doppio clic sull'icona per AccServer.exe per avviarla da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="17be6-140">Type AccServer.exe at the command line, or double-click the icon for AccServer.exe to launch it from Windows Explorer.</span></span>

<span data-ttu-id="17be6-141">Per eseguire da Visual Studio, premere F5 o scegliere **Avvia** debug dal menu **Debug.**</span><span class="sxs-lookup"><span data-stu-id="17be6-141">To run from Visual Studio, press F5 or click **Start Debugging** from the **Debug** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17be6-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17be6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17be6-143">Esempi</span><span class="sxs-lookup"><span data-stu-id="17be6-143">Samples</span></span>](samples.md)
</dt> </dl>

 

 




