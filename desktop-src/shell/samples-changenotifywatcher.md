---
description: Viene illustrato come ascoltare le notifiche di modifica della shell su una cartella o un elemento nello spazio dei nomi di Esplora risorse.
title: Esempio di Watcher per notifiche di modifica
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232712"
---
# <a name="change-notify-watcher-sample"></a><span data-ttu-id="f4e94-103">Esempio di Watcher per notifiche di modifica</span><span class="sxs-lookup"><span data-stu-id="f4e94-103">Change Notify Watcher Sample</span></span>

<span data-ttu-id="f4e94-104">Viene illustrato come ascoltare le notifiche di modifica della shell su una cartella o un elemento nello spazio dei nomi di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="f4e94-104">Demonstrates how to listen to Shell change notifications on a folder or item in the Windows Explorer namespace.</span></span>

<span data-ttu-id="f4e94-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f4e94-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f4e94-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4e94-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f4e94-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f4e94-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="f4e94-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f4e94-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f4e94-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f4e94-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="f4e94-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4e94-110">Requirements</span></span>



| <span data-ttu-id="f4e94-111">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f4e94-111">Product</span></span>                                | <span data-ttu-id="f4e94-112">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="f4e94-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="f4e94-113">Windows</span><span class="sxs-lookup"><span data-stu-id="f4e94-113">Windows</span></span>                                | <span data-ttu-id="f4e94-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4e94-114">Windows Vista</span></span>           |
| <span data-ttu-id="f4e94-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="f4e94-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="f4e94-116">7.0</span><span class="sxs-lookup"><span data-stu-id="f4e94-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f4e94-117">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f4e94-117">Downloading the Sample</span></span>

| <span data-ttu-id="f4e94-118">Location</span><span class="sxs-lookup"><span data-stu-id="f4e94-118">Location</span></span>      | <span data-ttu-id="f4e94-119">URL percorso</span><span class="sxs-lookup"><span data-stu-id="f4e94-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e94-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="f4e94-120">GitHub</span></span>  | [<span data-ttu-id="f4e94-121">Esempio ChangeNotifyWatcher</span><span class="sxs-lookup"><span data-stu-id="f4e94-121">ChangeNotifyWatcher sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a><span data-ttu-id="f4e94-122">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f4e94-122">Building the Sample</span></span>

<span data-ttu-id="f4e94-123">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="f4e94-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="f4e94-124">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **ChangeNotifyWatcher** .</span><span class="sxs-lookup"><span data-stu-id="f4e94-124">Open the command prompt window and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="f4e94-125">Immettere `msbuild ChangeNotifyWatcher.sln`.</span><span class="sxs-lookup"><span data-stu-id="f4e94-125">Enter `msbuild ChangeNotifyWatcher.sln`.</span></span>

<span data-ttu-id="f4e94-126">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="f4e94-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="f4e94-127">Aprire Esplora risorse e passare alla directory del progetto **ChangeNotifyWatcher** .</span><span class="sxs-lookup"><span data-stu-id="f4e94-127">Open Windows Explorer and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="f4e94-128">Fare doppio clic sull'icona per il file ChangeNotifyWatcher. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f4e94-128">Double-click the icon for the ChangeNotifyWatcher.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="f4e94-129">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="f4e94-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="f4e94-130">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f4e94-130">Running the Sample</span></span>

1.  <span data-ttu-id="f4e94-131">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="f4e94-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="f4e94-132">Al prompt dei comandi digitare `ChangeNotifyWatcher.exe`.</span><span class="sxs-lookup"><span data-stu-id="f4e94-132">At the command prompt, enter `ChangeNotifyWatcher.exe`.</span></span> <span data-ttu-id="f4e94-133">In alternativa, in Esplora risorse fare doppio clic sull'icona per ChangeNotifyWatcher.exe.</span><span class="sxs-lookup"><span data-stu-id="f4e94-133">Alternatively, from Windows Explorer double-click the icon for ChangeNotifyWatcher.exe.</span></span>
3.  <span data-ttu-id="f4e94-134">Per illustrare l'effetto, gli ID del modello utente dell'applicazione (AppUserModelIDs) selezionano una cartella da controllare facendo clic su **"pick..."** o usando il trascinamento della selezione in una cartella da una finestra di Esplora risorse nella visualizzazione elenco dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="f4e94-134">To demonstrate the effect, Application User Model IDs (AppUserModelIDs) select a folder to watch by either clicking **"Pick..."** or by using drag-and-drop on a folder from a Windows Explorer window into the sample's list view.</span></span>

 

 



