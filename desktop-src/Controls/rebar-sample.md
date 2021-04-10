---
title: Esempio di Rebar
ms.assetid: f26c0819-523d-42a5-be2f-3cd75748b4a6
description: 'Altre informazioni su: esempio di Rebar'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72b58a66c22b0ef8cc60d97c0965a8ae29a20fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965947"
---
# <a name="rebar-sample"></a><span data-ttu-id="b947d-103">Esempio di Rebar</span><span class="sxs-lookup"><span data-stu-id="b947d-103">Rebar Sample</span></span>

<span data-ttu-id="b947d-104">Questo argomento descrive l'esempio di codice rebar di esempio.</span><span class="sxs-lookup"><span data-stu-id="b947d-104">This topic describes the Rebar Sample code sample.</span></span> <span data-ttu-id="b947d-105">Contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b947d-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="b947d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b947d-106">Description</span></span>](#description)
-   [<span data-ttu-id="b947d-107">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="b947d-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="b947d-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b947d-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b947d-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b947d-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b947d-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b947d-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="b947d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b947d-111">Description</span></span>

<span data-ttu-id="b947d-112">Nell'esempio Rebar viene illustrato come implementare un semplice controllo Common Rebar in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b947d-112">The Rebar Sample shows how to implement a simple rebar common control in an application.</span></span> <span data-ttu-id="b947d-113">In questo esempio viene creato un controllo Rebar con due bande.</span><span class="sxs-lookup"><span data-stu-id="b947d-113">This example creates a rebar control that has two bands.</span></span> <span data-ttu-id="b947d-114">Uno contiene una casella combinata e l'altro contiene un pulsante di push.</span><span class="sxs-lookup"><span data-stu-id="b947d-114">One contains a combo box and the other contains a push button.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="b947d-115">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="b947d-115">Minimum Requirements</span></span>



| <span data-ttu-id="b947d-116">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b947d-116">Product</span></span>          | <span data-ttu-id="b947d-117">Versione</span><span class="sxs-lookup"><span data-stu-id="b947d-117">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="b947d-118">DLL</span><span class="sxs-lookup"><span data-stu-id="b947d-118">DLL</span></span>              | <span data-ttu-id="b947d-119">comctl32.dll versione 4,71</span><span class="sxs-lookup"><span data-stu-id="b947d-119">comctl32.dll version 4.71</span></span>             |
| <span data-ttu-id="b947d-120">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b947d-120">Operating System</span></span> | <span data-ttu-id="b947d-121">Windows 95 con Internet Explorer 4,0</span><span class="sxs-lookup"><span data-stu-id="b947d-121">Windows 95 with Internet Explorer 4.0</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b947d-122">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b947d-122">Downloading the Sample</span></span>

<span data-ttu-id="b947d-123">L'esempio Rebar viene installato come parte di [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) ed è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="b947d-123">The Rebar Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="b947d-124">Location</span><span class="sxs-lookup"><span data-stu-id="b947d-124">Location</span></span>    | <span data-ttu-id="b947d-125">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="b947d-125">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b947d-126">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="b947d-126">Windows SDK</span></span> | <span data-ttu-id="b947d-127">% Program Files% \\ Microsoft SDK \\ numero di versione di Windows \\ \[ \] \\ esempi \\ WinUI \\ controlli \\ \\ Rebar comune</span><span class="sxs-lookup"><span data-stu-id="b947d-127">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\rebar</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="b947d-128">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b947d-128">Building the Sample</span></span>

<span data-ttu-id="b947d-129">Per compilare l'esempio utilizzando il prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="b947d-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="b947d-130">Aprire la finestra del prompt dei comandi e passare alla directory del progetto.</span><span class="sxs-lookup"><span data-stu-id="b947d-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="b947d-131">Immettere `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="b947d-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="b947d-132">Per compilare l'esempio con Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="b947d-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="b947d-133">Aprire Esplora risorse e passare alla directory del progetto.</span><span class="sxs-lookup"><span data-stu-id="b947d-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="b947d-134">Fare doppio clic sull'icona del file con estensione vcproj per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b947d-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="b947d-135">Scegliere **Compila soluzione** dal menu **Compila** per compilare la soluzione.</span><span class="sxs-lookup"><span data-stu-id="b947d-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b947d-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b947d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b947d-137">Controlli Rebar</span><span class="sxs-lookup"><span data-stu-id="b947d-137">Rebar Controls</span></span>](rebar-controls.md)
</dt> </dl>

 

 




