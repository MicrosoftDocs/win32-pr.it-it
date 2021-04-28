---
description: Libreria del Registro di sistema offline
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Libreria del Registro di sistema offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1aa5acdd7904516608413ff973e60e81c296c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089249"
---
# <a name="offline-registry-library"></a><span data-ttu-id="bce69-103">Libreria del Registro di sistema offline</span><span class="sxs-lookup"><span data-stu-id="bce69-103">Offline Registry Library</span></span>

## <a name="purpose"></a><span data-ttu-id="bce69-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="bce69-104">Purpose</span></span>

<span data-ttu-id="bce69-105">La libreria del Registro di sistema offline (Offreg.dll) viene usata per modificare un hive del Registro di sistema all'esterno del Registro di sistema attivo.</span><span class="sxs-lookup"><span data-stu-id="bce69-105">The offline registry library (Offreg.dll) is used to modify a registry hive outside the active system registry.</span></span> <span data-ttu-id="bce69-106">Questa libreria è destinata agli scenari di aggiornamento del Registro di sistema, ad esempio la manutenzione di un'immagine del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bce69-106">This library is intended for registry update scenarios such as servicing an operating system image.</span></span> <span data-ttu-id="bce69-107">La libreria supporta i formati hive del Registro di sistema a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bce69-107">The library supports registry hive formats starting with Windows Vista.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bce69-108">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="bce69-108">Developer audience</span></span>

<span data-ttu-id="bce69-109">Questa tecnologia è per i produttori di apparecchiature originali (OEM), i fornitori di software antivirus e antimalware e altri sviluppatori di applicazioni che devono essere in grado di analizzare i file hive del Registro di sistema senza caricarli nel Registro di sistema attivo.</span><span class="sxs-lookup"><span data-stu-id="bce69-109">This technology is for original equipment manufacturers (OEMs), antivirus and antimalware software vendors, and other application developers who must be able to parse registry hive files without loading them into the active registry.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="bce69-110">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="bce69-110">Run-time requirements</span></span>

<span data-ttu-id="bce69-111">La libreria del Registro di sistema offline viene fornita come libreria a collegamento dinamico (DLL) ridistribuibile binaria.</span><span class="sxs-lookup"><span data-stu-id="bce69-111">The offline registry library is provided as a binary redistributable dynamic-link library (DLL).</span></span> <span data-ttu-id="bce69-112">Questa libreria viene eseguita nelle versioni seguenti di Windows:</span><span class="sxs-lookup"><span data-stu-id="bce69-112">This library runs on the following versions of Windows:</span></span>

<dl> <span data-ttu-id="bce69-113">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bce69-113">Windows Server 2016</span></span>  
<span data-ttu-id="bce69-114">Windows 10</span><span class="sxs-lookup"><span data-stu-id="bce69-114">Windows 10</span></span>  
<span data-ttu-id="bce69-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bce69-115">Windows 8.1</span></span>  
<span data-ttu-id="bce69-116">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bce69-116">Windows Server 2012 R2</span></span>  
<span data-ttu-id="bce69-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bce69-117">Windows 8</span></span>  
<span data-ttu-id="bce69-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bce69-118">Windows Server 2012</span></span>  
<span data-ttu-id="bce69-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bce69-119">Windows 7</span></span>  
<span data-ttu-id="bce69-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bce69-120">Windows Server 2008 R2</span></span>  
<span data-ttu-id="bce69-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bce69-121">Windows Server 2008</span></span>  
<span data-ttu-id="bce69-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bce69-122">Windows Vista</span></span>  
</dl>

<span data-ttu-id="bce69-123">Le applicazioni devono collegarsi a Offreg.dll tramite il collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="bce69-123">Applications should link to Offreg.dll using dynamic linking.</span></span>

<span data-ttu-id="bce69-124">Offreg.dll viene fornito in Windows Driver Kit (WDK) (WDK) per Windows 10 e versioni precedenti del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="bce69-124">Offreg.dll is provided in the Windows Driver Kit (WDK) for Windows 10 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="bce69-125">Per informazioni su come ottenere wdk, vedere [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) (Come ottenere WDK e WLK) o visitare il sito Web delle sottoscrizioni [MSDN.](https://msdn.microsoft.com/subscriptions/default.aspx)</span><span class="sxs-lookup"><span data-stu-id="bce69-125">For information about obtaining the WDK, see [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) or visit the [MSDN Subscriptions](https://msdn.microsoft.com/subscriptions/default.aspx) website.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bce69-126">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="bce69-126">In this section</span></span>

-   [<span data-ttu-id="bce69-127">**Informazioni sulla libreria del Registro di sistema offline**</span><span class="sxs-lookup"><span data-stu-id="bce69-127">**About the Offline Registry Library**</span></span>](about-the-offline-registry-library.md)
-   [<span data-ttu-id="bce69-128">**Funzioni della libreria del Registro di sistema offline**</span><span class="sxs-lookup"><span data-stu-id="bce69-128">**Offline Registry Library Functions**</span></span>](offline-registry-library-functions.md)

 

 
