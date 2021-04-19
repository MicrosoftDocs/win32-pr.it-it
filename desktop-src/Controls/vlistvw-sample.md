---
title: Esempio VListVW
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 'Altre informazioni su: esempio VListVW'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445f83d08641179f9ee0e5b3aeeee5a613f1f6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305088"
---
# <a name="vlistvw-sample"></a><span data-ttu-id="c5088-103">Esempio VListVW</span><span class="sxs-lookup"><span data-stu-id="c5088-103">VListVW Sample</span></span>

<span data-ttu-id="c5088-104">Questo argomento descrive l'esempio di codice di esempio VListVW.</span><span class="sxs-lookup"><span data-stu-id="c5088-104">This topic describes the VListVW Sample code sample.</span></span> <span data-ttu-id="c5088-105">Contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5088-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="c5088-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5088-106">Description</span></span>](#description)
-   [<span data-ttu-id="c5088-107">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="c5088-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="c5088-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c5088-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c5088-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c5088-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c5088-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5088-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="c5088-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5088-111">Description</span></span>

<span data-ttu-id="c5088-112">Nell'esempio VListVW viene illustrato come implementare un semplice controllo visualizzazione elenco virtuale in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c5088-112">The VListVW Sample shows how to implement a simple virtual list-view control in an application.</span></span> <span data-ttu-id="c5088-113">Un controllo di visualizzazione elenco virtuale è un controllo di visualizzazione elenco standard con lo **stile \_ OWNERDATA di LVS** .</span><span class="sxs-lookup"><span data-stu-id="c5088-113">A virtual list-view control is a standard list-view control with the **LVS\_OWNERDATA** style.</span></span> <span data-ttu-id="c5088-114">In questo esempio viene creato un controllo di visualizzazione elenco che "virtualmente" include 100.000 elementi.</span><span class="sxs-lookup"><span data-stu-id="c5088-114">This example creates a list-view control that "virtually" holds 100,000 items.</span></span> <span data-ttu-id="c5088-115">Gli elementi non vengono mai effettivamente aggiunti.</span><span class="sxs-lookup"><span data-stu-id="c5088-115">The items are never actually added.</span></span> <span data-ttu-id="c5088-116">Al contrario, il controllo di visualizzazione elenco virtuale indica il numero di elementi che contiene con il messaggio [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md) .</span><span class="sxs-lookup"><span data-stu-id="c5088-116">Instead, the virtual list-view control is "told" how many items it contains with the [**LVM\_SETITEMCOUNT**](lvm-setitemcount.md) message.</span></span> <span data-ttu-id="c5088-117">Quando è necessario disegnare un elemento, il controllo elenco-visualizzazione esegue una query sulla finestra padre per visualizzare le informazioni con la notifica [ \_ GETDISPINFO LVN](lvn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c5088-117">When an item needs to be drawn, the list-view control queries the parent window for display information with the [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="c5088-118">Requisiti minimi</span><span class="sxs-lookup"><span data-stu-id="c5088-118">Minimum Requirements</span></span>



| <span data-ttu-id="c5088-119">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c5088-119">Product</span></span>          | <span data-ttu-id="c5088-120">Versione</span><span class="sxs-lookup"><span data-stu-id="c5088-120">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="c5088-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c5088-121">DLL</span></span>              | <span data-ttu-id="c5088-122">comctl32.dll versione 4,70</span><span class="sxs-lookup"><span data-stu-id="c5088-122">comctl32.dll version 4.70</span></span>             |
| <span data-ttu-id="c5088-123">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c5088-123">Operating System</span></span> | <span data-ttu-id="c5088-124">Windows 95, Microsoft Windows NT 3,51</span><span class="sxs-lookup"><span data-stu-id="c5088-124">Windows 95, Microsoft Windows NT 3.51</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c5088-125">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c5088-125">Downloading the Sample</span></span>

<span data-ttu-id="c5088-126">L'esempio VListVW è disponibile in GitHub nel repository di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples).</span><span class="sxs-lookup"><span data-stu-id="c5088-126">The VListVW Sample is available on on github in the [Windows Classic Samples repository](https://github.com/microsoft/Windows-classic-samples).</span></span> <span data-ttu-id="c5088-127">Gli esempi di elementi di controllo di visualizzazione elenco sono disponibili [qui](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)</span><span class="sxs-lookup"><span data-stu-id="c5088-127">The list view control items examples can be found at [here](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="c5088-128">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c5088-128">Building the Sample</span></span>

<span data-ttu-id="c5088-129">Per compilare l'esempio utilizzando il prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="c5088-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="c5088-130">Aprire la finestra del prompt dei comandi e passare alla directory del progetto.</span><span class="sxs-lookup"><span data-stu-id="c5088-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="c5088-131">Immettere `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="c5088-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="c5088-132">Per compilare l'esempio con Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="c5088-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="c5088-133">Aprire Esplora risorse e passare alla directory del progetto.</span><span class="sxs-lookup"><span data-stu-id="c5088-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="c5088-134">Fare doppio clic sull'icona del file con estensione vcproj per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c5088-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="c5088-135">Scegliere **Compila soluzione** dal menu **Compila** per compilare la soluzione.</span><span class="sxs-lookup"><span data-stu-id="c5088-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5088-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5088-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5088-137">Informazioni sui controlli List-View</span><span class="sxs-lookup"><span data-stu-id="c5088-137">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> </dl>

 

 




