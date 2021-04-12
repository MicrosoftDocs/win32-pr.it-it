---
description: Funzioni utilizzate per gestire le cartelle montate.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funzioni cartella montata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346081"
---
# <a name="mounted-folder-functions"></a><span data-ttu-id="e32fe-103">Funzioni cartella montata</span><span class="sxs-lookup"><span data-stu-id="e32fe-103">Mounted Folder Functions</span></span>

<span data-ttu-id="e32fe-104">Le funzioni della cartella montata possono essere divise in tre gruppi, ovvero funzioni generiche, funzioni usate per analizzare i volumi e funzioni usate per analizzare un volume per le cartelle montate.</span><span class="sxs-lookup"><span data-stu-id="e32fe-104">The mounted folder functions can be divided into three groups: general-purpose functions, functions used to scan for volumes, and functions used to scan a volume for mounted folders.</span></span>

## <a name="general-purpose-mounted-folder-functions"></a><span data-ttu-id="e32fe-105">Funzioni della cartella montata General-Purpose</span><span class="sxs-lookup"><span data-stu-id="e32fe-105">General-Purpose Mounted Folder Functions</span></span>



| <span data-ttu-id="e32fe-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="e32fe-106">Function</span></span>                                                                     | <span data-ttu-id="e32fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e32fe-107">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e32fe-108">**DeleteVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="e32fe-108">**DeleteVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | <span data-ttu-id="e32fe-109">Elimina una lettera di unità o una cartella montata.</span><span class="sxs-lookup"><span data-stu-id="e32fe-109">Deletes a drive letter or mounted folder.</span></span>                                                                                                                   |
| [<span data-ttu-id="e32fe-110">**GetVolumeNameForVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="e32fe-110">**GetVolumeNameForVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | <span data-ttu-id="e32fe-111">Recupera il percorso GUID del volume associato al punto di montaggio del volume specificato (lettera di unità, percorso GUID volume o cartella montata).</span><span class="sxs-lookup"><span data-stu-id="e32fe-111">Retrieves the volume GUID path for the volume that is associated with the specified volume mount point (drive letter, volume GUID path, or mounted folder).</span></span> |
| [<span data-ttu-id="e32fe-112">**GetVolumePathName**</span><span class="sxs-lookup"><span data-stu-id="e32fe-112">**GetVolumePathName**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | <span data-ttu-id="e32fe-113">Recupera la cartella montata associata al volume specificato.</span><span class="sxs-lookup"><span data-stu-id="e32fe-113">Retrieves the mounted folder that is associated with the specified volume.</span></span>                                                                                  |
| [<span data-ttu-id="e32fe-114">**SetVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="e32fe-114">**SetVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | <span data-ttu-id="e32fe-115">Associa un volume a una lettera di unità o a una directory in un altro volume.</span><span class="sxs-lookup"><span data-stu-id="e32fe-115">Associates a volume with a drive letter or a directory on another volume.</span></span>                                                                                   |



 

## <a name="volume-scanning-functions"></a><span data-ttu-id="e32fe-116">Funzioni Volume-Scanning</span><span class="sxs-lookup"><span data-stu-id="e32fe-116">Volume-Scanning Functions</span></span>



| <span data-ttu-id="e32fe-117">Funzione</span><span class="sxs-lookup"><span data-stu-id="e32fe-117">Function</span></span>                                   | <span data-ttu-id="e32fe-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e32fe-118">Description</span></span>                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e32fe-119">**FindFirstVolume**</span><span class="sxs-lookup"><span data-stu-id="e32fe-119">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | <span data-ttu-id="e32fe-120">Restituisce il nome di un volume in un computer.</span><span class="sxs-lookup"><span data-stu-id="e32fe-120">Returns the name of a volume on a computer.</span></span> <span data-ttu-id="e32fe-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) viene utilizzato per iniziare a enumerare i volumi di un computer.</span><span class="sxs-lookup"><span data-stu-id="e32fe-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) is used to begin enumerating the volumes of a computer.</span></span> |
| [<span data-ttu-id="e32fe-122">**FindNextVolume**</span><span class="sxs-lookup"><span data-stu-id="e32fe-122">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | <span data-ttu-id="e32fe-123">Continua la ricerca di un volume avviata da una chiamata a [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span><span class="sxs-lookup"><span data-stu-id="e32fe-123">Continues a volume search started by a call to [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span>                                                     |
| [<span data-ttu-id="e32fe-124">**FindVolumeClose**</span><span class="sxs-lookup"><span data-stu-id="e32fe-124">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | <span data-ttu-id="e32fe-125">Chiude una ricerca di volumi.</span><span class="sxs-lookup"><span data-stu-id="e32fe-125">Closes a search for volumes.</span></span>                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a><span data-ttu-id="e32fe-126">Funzioni di analisi della cartella montata</span><span class="sxs-lookup"><span data-stu-id="e32fe-126">Mounted Folder Scanning Functions</span></span>



| <span data-ttu-id="e32fe-127">Funzione</span><span class="sxs-lookup"><span data-stu-id="e32fe-127">Function</span></span>                                                       | <span data-ttu-id="e32fe-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e32fe-128">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e32fe-129">**FindFirstVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="e32fe-129">**FindFirstVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | <span data-ttu-id="e32fe-130">Recupera il nome di una cartella montata nel volume specificato.</span><span class="sxs-lookup"><span data-stu-id="e32fe-130">Retrieves the name of a mounted folder on the specified volume.</span></span> <span data-ttu-id="e32fe-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) viene utilizzato per iniziare l'analisi delle cartelle montate in un volume.</span><span class="sxs-lookup"><span data-stu-id="e32fe-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) is used to begin scanning the mounted folders on a volume.</span></span> |
| [<span data-ttu-id="e32fe-132">**FindNextVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="e32fe-132">**FindNextVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | <span data-ttu-id="e32fe-133">Continua la ricerca di una cartella montata avviata da una chiamata a [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span><span class="sxs-lookup"><span data-stu-id="e32fe-133">Continues a mounted folder search started by a call to [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span></span>                                                                    |
| [<span data-ttu-id="e32fe-134">**FindVolumeMountPointClose**</span><span class="sxs-lookup"><span data-stu-id="e32fe-134">**FindVolumeMountPointClose**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | <span data-ttu-id="e32fe-135">Chiude una ricerca di cartelle montate.</span><span class="sxs-lookup"><span data-stu-id="e32fe-135">Closes a search for mounted folders.</span></span>                                                                                                                                                      |



 

 

 



