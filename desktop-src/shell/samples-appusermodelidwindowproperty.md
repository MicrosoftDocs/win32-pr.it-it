---
description: Viene illustrato come controllare il comportamento di raggruppamento della barra delle applicazioni per le finestre di un'applicazione tramite la proprietà System.AppUserModel.ID.
title: Esempio di proprietà delle finestre ID modello utente applicazione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 42544992248143c95ae905db39fe854b27751862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980343"
---
# <a name="application-user-model-id-appid-window-property-sample"></a><span data-ttu-id="c0366-103">Esempio di proprietà della finestra ID modello utente applicazione (AppID)</span><span class="sxs-lookup"><span data-stu-id="c0366-103">Application User Model ID (AppID) Window Property Sample</span></span>

<span data-ttu-id="c0366-104">Viene illustrato come controllare il comportamento di raggruppamento della barra delle applicazioni per le finestre di un'applicazione tramite la proprietà [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="c0366-104">Demonstrates how to control the taskbar grouping behavior of an application's windows through the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property.</span></span>

<span data-ttu-id="c0366-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c0366-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c0366-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0366-106">Description</span></span>](#description)
-   [<span data-ttu-id="c0366-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0366-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c0366-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c0366-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c0366-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c0366-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c0366-110">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c0366-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="c0366-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0366-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="c0366-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0366-112">Description</span></span>

<span data-ttu-id="c0366-113">In questo esempio viene illustrato come impostare la proprietà [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) tramite l'utilizzo dell'implementazione di [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) della finestra, ottenuta tramite [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span><span class="sxs-lookup"><span data-stu-id="c0366-113">This sample shows how to set the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property through the use of the window's [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, which is obtained through [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0366-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0366-114">Requirements</span></span>



| <span data-ttu-id="c0366-115">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c0366-115">Product</span></span>                                | <span data-ttu-id="c0366-116">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="c0366-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="c0366-117">Windows</span><span class="sxs-lookup"><span data-stu-id="c0366-117">Windows</span></span>                                | <span data-ttu-id="c0366-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0366-118">Windows 7</span></span>               |
| <span data-ttu-id="c0366-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="c0366-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="c0366-120">7.0</span><span class="sxs-lookup"><span data-stu-id="c0366-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c0366-121">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c0366-121">Downloading the Sample</span></span>

| <span data-ttu-id="c0366-122">Location</span><span class="sxs-lookup"><span data-stu-id="c0366-122">Location</span></span>      | <span data-ttu-id="c0366-123">URL percorso</span><span class="sxs-lookup"><span data-stu-id="c0366-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0366-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="c0366-124">GitHub</span></span>  | [<span data-ttu-id="c0366-125">Esempio AppUserModelIDWindowProperty</span><span class="sxs-lookup"><span data-stu-id="c0366-125">AppUserModelIDWindowProperty sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a><span data-ttu-id="c0366-126">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c0366-126">Building the Sample</span></span>

<span data-ttu-id="c0366-127">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="c0366-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="c0366-128">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **AppUserModelIDWindowProperty** .</span><span class="sxs-lookup"><span data-stu-id="c0366-128">Open the command prompt window and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="c0366-129">Immettere `msbuild AppUserModelIDWindowProperty.sln`.</span><span class="sxs-lookup"><span data-stu-id="c0366-129">Enter `msbuild AppUserModelIDWindowProperty.sln`.</span></span>

<span data-ttu-id="c0366-130">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="c0366-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="c0366-131">Aprire Esplora risorse e passare alla directory del progetto **AppUserModelIDWindowProperty** .</span><span class="sxs-lookup"><span data-stu-id="c0366-131">Open Windows Explorer and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="c0366-132">Fare doppio clic sull'icona per il file AppUserModelIDWindowProperty. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c0366-132">Double-click the icon for the AppUserModelIDWindowProperty.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="c0366-133">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="c0366-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c0366-134">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c0366-134">Running the Sample</span></span>

1.  <span data-ttu-id="c0366-135">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="c0366-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="c0366-136">Nella riga di comando, immettere `AppUserModelIDWindowProperty.exe` .</span><span class="sxs-lookup"><span data-stu-id="c0366-136">At the command line, enter `AppUserModelIDWindowProperty.exe`.</span></span> <span data-ttu-id="c0366-137">In alternativa, in Esplora risorse fare doppio clic sull'icona per AppUserModelIDWindowProperty.exe.</span><span class="sxs-lookup"><span data-stu-id="c0366-137">Alternatively, from Windows Explorer double-click the icon for AppUserModelIDWindowProperty.exe.</span></span>
3.  <span data-ttu-id="c0366-138">Per dimostrare l'effetto degli ID del modello utente dell'applicazione (AppUserModelIDs) sul raggruppamento della barra delle applicazioni, avviare almeno tre istanze dell'applicazione nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="c0366-138">To demonstrate the effect Application User Model IDs (AppUserModelIDs) have on taskbar grouping, launch at least three instances of the application at the same time.</span></span>
4.  <span data-ttu-id="c0366-139">Usare il menu per impostare un AppUserModelID diverso in ognuna delle tre finestre.</span><span class="sxs-lookup"><span data-stu-id="c0366-139">Use the menu to set a different AppUserModelID on each of the three windows.</span></span> <span data-ttu-id="c0366-140">Si noti che ogni AppUserModelID separato genera un pulsante della barra delle applicazioni separato e che Windows può modificare la propria identità in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c0366-140">Notice that each separate AppUserModelID results in a separate taskbar button and that windows can change their identity at runtime.</span></span>
5.  <span data-ttu-id="c0366-141">Impostare almeno due finestre sul secondo AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="c0366-141">Set at least two windows to the second AppUserModelID.</span></span> <span data-ttu-id="c0366-142">Si noti che entrambi si spostano nello stesso gruppo di barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c0366-142">Notice that they both move into the same taskbar group.</span></span>
6.  <span data-ttu-id="c0366-143">Per aprire la **barra delle applicazioni e il menu Start** , fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere **Proprietà** dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="c0366-143">Open the **Taskbar and Start Menu Properties** window by right-clicking the taskbar and selecting **Properties** in the context menu.</span></span> <span data-ttu-id="c0366-144">Modificare i **pulsanti della barra delle applicazioni:** elenco a discesa tra le **combinazioni quando la barra delle applicazioni è piena** e **non combinare mai** i valori.</span><span class="sxs-lookup"><span data-stu-id="c0366-144">Change the **Taskbar buttons:** drop-down between the **Combine when taskbar is full** and **Never combine** values.</span></span> <span data-ttu-id="c0366-145">Si noti che ogni finestra può ottenere un pulsante separato, ma che i pulsanti sono raggruppati in base a AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="c0366-145">Notice that each window can get a separate button, but that the buttons are grouped by AppUserModelID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0366-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0366-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0366-147">ID modello utente applicazione (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="c0366-147">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
