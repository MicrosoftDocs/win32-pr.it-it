---
description: Viene illustrato come registrare un verbo che estende il &\# 0034; Sync&\# 0034; e &\# 0034; Condividere&\# 0034; verbi nella barra dei comandi di Esplora risorse.
title: Sincronizzare e condividere i verbi
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980751"
---
# <a name="sync-and-share-verbs"></a><span data-ttu-id="e1f54-103">Sincronizzare e condividere i verbi</span><span class="sxs-lookup"><span data-stu-id="e1f54-103">Sync and Share Verbs</span></span>

<span data-ttu-id="e1f54-104">Viene illustrato come registrare un verbo che estende i verbi "Sync" e "Share" nella barra dei comandi di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="e1f54-104">Demonstrates how to register a verb that extends the "Sync" and "Share" verbs in the Windows Explorer Command Bar.</span></span>

<span data-ttu-id="e1f54-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e1f54-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e1f54-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1f54-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e1f54-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="e1f54-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="e1f54-108">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="e1f54-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="e1f54-109">Rimozione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="e1f54-109">Removing the Sample</span></span>](#removing-the-sample)

## <a name="requirements"></a><span data-ttu-id="e1f54-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1f54-110">Requirements</span></span>



| <span data-ttu-id="e1f54-111">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e1f54-111">Product</span></span>                                | <span data-ttu-id="e1f54-112">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="e1f54-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="e1f54-113">Windows</span><span class="sxs-lookup"><span data-stu-id="e1f54-113">Windows</span></span>                                | <span data-ttu-id="e1f54-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1f54-114">Windows 7</span></span>               |
| <span data-ttu-id="e1f54-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="e1f54-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="e1f54-116">7.0</span><span class="sxs-lookup"><span data-stu-id="e1f54-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e1f54-117">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="e1f54-117">Downloading the Sample</span></span>

| <span data-ttu-id="e1f54-118">Location</span><span class="sxs-lookup"><span data-stu-id="e1f54-118">Location</span></span>      | <span data-ttu-id="e1f54-119">URL percorso</span><span class="sxs-lookup"><span data-stu-id="e1f54-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f54-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="e1f54-120">GitHub</span></span>  | [<span data-ttu-id="e1f54-121">Esempio SyncAndShareVerbs</span><span class="sxs-lookup"><span data-stu-id="e1f54-121">SyncAndShareVerbs sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a><span data-ttu-id="e1f54-122">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="e1f54-122">Running the Sample</span></span>

<span data-ttu-id="e1f54-123">Per eseguire l'esempio (sincronizzazione):</span><span class="sxs-lookup"><span data-stu-id="e1f54-123">To run the sample (sync):</span></span>

1.  <span data-ttu-id="e1f54-124">Passare alla directory che contiene il `sync.reg` file</span><span class="sxs-lookup"><span data-stu-id="e1f54-124">Navigate to the directory that contains the `sync.reg` file</span></span>
2.  <span data-ttu-id="e1f54-125">Digitare `sync.reg ` nella riga di comando oppure fare doppio clic sull'icona per `sync.reg` registrarla.</span><span class="sxs-lookup"><span data-stu-id="e1f54-125">Type `sync.reg ` at the command line, or double-click the icon for `sync.reg` register it.</span></span>
3.  <span data-ttu-id="e1f54-126">Aprire Esplora risorse e selezionare un file.</span><span class="sxs-lookup"><span data-stu-id="e1f54-126">Open the Windows Explorer and select a file.</span></span>
4.  <span data-ttu-id="e1f54-127">Fare clic sull'opzione **Sincronizza** sulla barra dei comandi e selezionare una sottoopzione, ad esempio **Paint**.</span><span class="sxs-lookup"><span data-stu-id="e1f54-127">Click the **Sync** option in the Command Bar and select a suboption such as **Paint**.</span></span>

<span data-ttu-id="e1f54-128">Per eseguire l'esempio (share):</span><span class="sxs-lookup"><span data-stu-id="e1f54-128">To run the sample (share):</span></span>

1.  <span data-ttu-id="e1f54-129">Passare alla directory che contiene il `share.reg` file.</span><span class="sxs-lookup"><span data-stu-id="e1f54-129">Navigate to the directory that contains the `share.reg` file.</span></span>
2.  <span data-ttu-id="e1f54-130">Digitare `share.reg` nella riga di comando oppure fare doppio clic sull'icona per `share.reg` registrarla.</span><span class="sxs-lookup"><span data-stu-id="e1f54-130">Type `share.reg` at the command line, or double-click the icon for `share.reg` register it.</span></span>
3.  <span data-ttu-id="e1f54-131">Aprire Esplora risorse e selezionare un file.</span><span class="sxs-lookup"><span data-stu-id="e1f54-131">Open Windows Explorer and select a file.</span></span> <span data-ttu-id="e1f54-132">Fare clic sull'opzione **Condividi** sulla barra dei comandi.</span><span class="sxs-lookup"><span data-stu-id="e1f54-132">Click the **Share** option in the Command Bar.</span></span>
4.  <span data-ttu-id="e1f54-133">Fare clic sull'opzione **Condividi con** nella barra dei comandi e selezionare una sottoopzione, ad esempio **Paint**.</span><span class="sxs-lookup"><span data-stu-id="e1f54-133">Click the **Share with** option in the Command Bar and select a suboption such as **Paint**.</span></span>

## <a name="removing-the-sample"></a><span data-ttu-id="e1f54-134">Rimozione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="e1f54-134">Removing the Sample</span></span>

<span data-ttu-id="e1f54-135">Per rimuovere l'esempio (sincronizzazione):</span><span class="sxs-lookup"><span data-stu-id="e1f54-135">To remove the sample (sync):</span></span>

1.  <span data-ttu-id="e1f54-136">Passare alla directory che contiene il file Uninstallsync. reg.</span><span class="sxs-lookup"><span data-stu-id="e1f54-136">Navigate to the directory that contains the Uninstallsync.reg file.</span></span>
2.  <span data-ttu-id="e1f54-137">Digitare `uninstallsync.reg` nella riga di comando oppure fare doppio clic sull'icona relativa a `uninstallsync.reg` .</span><span class="sxs-lookup"><span data-stu-id="e1f54-137">Type `uninstallsync.reg` at the command line, or double-click the icon for `uninstallsync.reg`.</span></span>

<span data-ttu-id="e1f54-138">Per rimuovere l'esempio (share):</span><span class="sxs-lookup"><span data-stu-id="e1f54-138">To remove the sample (share):</span></span>

1.  <span data-ttu-id="e1f54-139">Passare alla directory che contiene il file Uninstallshare. reg.</span><span class="sxs-lookup"><span data-stu-id="e1f54-139">Navigate to the directory that contains the Uninstallshare.reg file.</span></span>
2.  <span data-ttu-id="e1f54-140">Digitare `uninstallshare.reg` nella riga di comando oppure fare doppio clic sull'icona per `uninstallshare.reg.`</span><span class="sxs-lookup"><span data-stu-id="e1f54-140">Type `uninstallshare.reg` at the command line, or double-click the icon for `uninstallshare.reg.`</span></span>

 

 



