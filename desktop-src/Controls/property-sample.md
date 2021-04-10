---
title: Esempio di proprietà
ms.assetid: 44642d32-2cbc-4dd9-bccc-15924f310539
description: 'Ulteriori informazioni su: esempio di proprietà'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c11fda9b133ca6fa3b2f9942d8d48bec3a9e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125976"
---
# <a name="property-sample"></a><span data-ttu-id="94102-103">Esempio di proprietà</span><span class="sxs-lookup"><span data-stu-id="94102-103">Property Sample</span></span>

<span data-ttu-id="94102-104">Questo argomento descrive l'esempio di codice di esempio della proprietà.</span><span class="sxs-lookup"><span data-stu-id="94102-104">This topic describes the Property Sample code sample.</span></span> <span data-ttu-id="94102-105">Contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="94102-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="94102-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94102-106">Description</span></span>](#description)
-   [<span data-ttu-id="94102-107">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="94102-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="94102-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="94102-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="94102-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="94102-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="94102-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94102-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="94102-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94102-111">Description</span></span>

<span data-ttu-id="94102-112">Nell'esempio di proprietà viene illustrato come implementare tre stili diversi di finestre delle proprietà: modale, non modale e procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="94102-112">The Property Sample shows how to implement three different styles of property sheets: modal, modeless, and wizard.</span></span> <span data-ttu-id="94102-113">Viene inoltre illustrato come utilizzare la funzione [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) per modificare la finestra di dialogo della finestra delle proprietà prima o dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="94102-113">It also shows how to use the [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) function to modify the property sheet dialog before or after it is created.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="94102-114">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="94102-114">Minimum Requirements</span></span>



| <span data-ttu-id="94102-115">Prodotto</span><span class="sxs-lookup"><span data-stu-id="94102-115">Product</span></span>          | <span data-ttu-id="94102-116">Versione</span><span class="sxs-lookup"><span data-stu-id="94102-116">Version</span></span>                              |
|------------------|--------------------------------------|
| <span data-ttu-id="94102-117">DLL</span><span class="sxs-lookup"><span data-stu-id="94102-117">DLL</span></span>              | <span data-ttu-id="94102-118">comctl32.dll versione 4,0</span><span class="sxs-lookup"><span data-stu-id="94102-118">comctl32.dll version 4.0</span></span>             |
| <span data-ttu-id="94102-119">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="94102-119">Operating System</span></span> | <span data-ttu-id="94102-120">Windows 95, Microsoft Windows NT 3,1</span><span class="sxs-lookup"><span data-stu-id="94102-120">Windows 95, Microsoft Windows NT 3.1</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="94102-121">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="94102-121">Downloading the Sample</span></span>

<span data-ttu-id="94102-122">L'esempio di proprietà viene installato come parte di [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) ed è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="94102-122">The Property Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="94102-123">Location</span><span class="sxs-lookup"><span data-stu-id="94102-123">Location</span></span>    | <span data-ttu-id="94102-124">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="94102-124">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94102-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="94102-125">Windows SDK</span></span> | <span data-ttu-id="94102-126">% Program Files% \\ Microsoft SDK \\ numero di versione di Windows \\ \[ \] \\ esempi \\ WinUI \\ controlli di \\ \\ Proprietà comuni</span><span class="sxs-lookup"><span data-stu-id="94102-126">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\property</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="94102-127">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="94102-127">Building the Sample</span></span>

<span data-ttu-id="94102-128">Per compilare l'esempio utilizzando il prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="94102-128">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="94102-129">Aprire la finestra del prompt dei comandi e passare alla directory del progetto.</span><span class="sxs-lookup"><span data-stu-id="94102-129">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="94102-130">Immettere `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="94102-130">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="94102-131">Per compilare l'esempio con Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="94102-131">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="94102-132">Aprire Esplora risorse e passare alla directory del progetto.</span><span class="sxs-lookup"><span data-stu-id="94102-132">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="94102-133">Fare doppio clic sull'icona del file con estensione vcproj per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="94102-133">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="94102-134">Scegliere **Compila soluzione** dal menu **Compila** per compilare la soluzione.</span><span class="sxs-lookup"><span data-stu-id="94102-134">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94102-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94102-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94102-136">Informazioni sulle finestre delle proprietà</span><span class="sxs-lookup"><span data-stu-id="94102-136">About Property Sheets</span></span>](property-sheets.md)
</dt> </dl>

 

 




