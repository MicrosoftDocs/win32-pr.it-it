---
description: .
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Libreria del registro di sistema offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a473bde729a0047a56d7ad0fdec1c0e3133ea103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304562"
---
# <a name="offline-registry-library"></a><span data-ttu-id="0571f-103">Libreria del registro di sistema offline</span><span class="sxs-lookup"><span data-stu-id="0571f-103">Offline Registry Library</span></span>

## <a name="purpose"></a><span data-ttu-id="0571f-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="0571f-104">Purpose</span></span>

<span data-ttu-id="0571f-105">La libreria del registro di sistema offline (Offreg.dll) viene usata per modificare un hive del registro di sistema all'esterno del registro di sistema attivo.</span><span class="sxs-lookup"><span data-stu-id="0571f-105">The offline registry library (Offreg.dll) is used to modify a registry hive outside the active system registry.</span></span> <span data-ttu-id="0571f-106">Questa libreria è destinata agli scenari di aggiornamento del registro di sistema, come la manutenzione di un'immagine del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0571f-106">This library is intended for registry update scenarios such as servicing an operating system image.</span></span> <span data-ttu-id="0571f-107">La libreria supporta i formati hive del registro di sistema a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0571f-107">The library supports registry hive formats starting with Windows Vista.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="0571f-108">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="0571f-108">Developer audience</span></span>

<span data-ttu-id="0571f-109">Questa tecnologia è destinata agli OEM (Original Equipment Manufacturer), ai fornitori di software antivirus e antimalware e ad altri sviluppatori di applicazioni che devono essere in grado di analizzare i file hive del registro di sistema senza caricarli nel registro di sistema attivo.</span><span class="sxs-lookup"><span data-stu-id="0571f-109">This technology is for original equipment manufacturers (OEMs), antivirus and antimalware software vendors, and other application developers who must be able to parse registry hive files without loading them into the active registry.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="0571f-110">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="0571f-110">Run-time requirements</span></span>

<span data-ttu-id="0571f-111">La libreria del registro di sistema offline viene fornita come libreria di collegamento dinamico (DLL) ridistribuibile binario.</span><span class="sxs-lookup"><span data-stu-id="0571f-111">The offline registry library is provided as a binary redistributable dynamic-link library (DLL).</span></span> <span data-ttu-id="0571f-112">Questa libreria viene eseguita nelle seguenti versioni di Windows:</span><span class="sxs-lookup"><span data-stu-id="0571f-112">This library runs on the following versions of Windows:</span></span>

<dl> <span data-ttu-id="0571f-113">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0571f-113">Windows Server 2016</span></span>  
<span data-ttu-id="0571f-114">Windows 10</span><span class="sxs-lookup"><span data-stu-id="0571f-114">Windows 10</span></span>  
<span data-ttu-id="0571f-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0571f-115">Windows 8.1</span></span>  
<span data-ttu-id="0571f-116">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0571f-116">Windows Server 2012 R2</span></span>  
<span data-ttu-id="0571f-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0571f-117">Windows 8</span></span>  
<span data-ttu-id="0571f-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0571f-118">Windows Server 2012</span></span>  
<span data-ttu-id="0571f-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0571f-119">Windows 7</span></span>  
<span data-ttu-id="0571f-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0571f-120">Windows Server 2008 R2</span></span>  
<span data-ttu-id="0571f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0571f-121">Windows Server 2008</span></span>  
<span data-ttu-id="0571f-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0571f-122">Windows Vista</span></span>  
</dl>

<span data-ttu-id="0571f-123">Le applicazioni devono essere collegate a Offreg.dll tramite il collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="0571f-123">Applications should link to Offreg.dll using dynamic linking.</span></span>

<span data-ttu-id="0571f-124">Offreg.dll viene fornito in Windows Driver Kit (WDK) per Windows 10 e versioni precedenti del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="0571f-124">Offreg.dll is provided in the Windows Driver Kit (WDK) for Windows 10 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="0571f-125">Per informazioni su come ottenere il WDK, vedere [come ottenere WDK e WLK](/windows-hardware/drivers/download-the-wdk) oppure visitare il sito Web degli [abbonamenti MSDN](https://msdn.microsoft.com/subscriptions/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0571f-125">For information about obtaining the WDK, see [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) or visit the [MSDN Subscriptions](https://msdn.microsoft.com/subscriptions/default.aspx) website.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0571f-126">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="0571f-126">In this section</span></span>

-   [<span data-ttu-id="0571f-127">**Informazioni sulla libreria del registro di sistema offline**</span><span class="sxs-lookup"><span data-stu-id="0571f-127">**About the Offline Registry Library**</span></span>](about-the-offline-registry-library.md)
-   [<span data-ttu-id="0571f-128">**Funzioni della libreria del registro di sistema offline**</span><span class="sxs-lookup"><span data-stu-id="0571f-128">**Offline Registry Library Functions**</span></span>](offline-registry-library-functions.md)

 

 
