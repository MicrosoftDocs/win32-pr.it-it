---
description: Viene illustrato come utilizzare le API della shell \_ NotifyIcon e shell \_ NotifyIconGetRect per visualizzare un'icona di notifica.
title: Esempio NotificationIcon
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979834"
---
# <a name="notificationicon-sample"></a><span data-ttu-id="de2d4-103">Esempio NotificationIcon</span><span class="sxs-lookup"><span data-stu-id="de2d4-103">NotificationIcon Sample</span></span>

<span data-ttu-id="de2d4-104">Viene illustrato come utilizzare le API della shell [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) e [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) per visualizzare un'icona di notifica.</span><span class="sxs-lookup"><span data-stu-id="de2d4-104">Demonstrates how to use the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) APIs to display a notification icon.</span></span>

<span data-ttu-id="de2d4-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="de2d4-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="de2d4-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de2d4-106">Description</span></span>](#description)
-   [<span data-ttu-id="de2d4-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de2d4-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="de2d4-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="de2d4-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="de2d4-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="de2d4-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="de2d4-110">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="de2d4-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="de2d4-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de2d4-111">Description</span></span>

<span data-ttu-id="de2d4-112">Oltre all'utilizzo della shell [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) e della [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) per visualizzare un'icona di notifica, in questo esempio viene illustrato come visualizzare una finestra del riquadro a comparsa, un menu di scelta rapida e una notifica dell'aerostato avanzati.</span><span class="sxs-lookup"><span data-stu-id="de2d4-112">In addition to the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) and [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) to display a notification icon, this sample also demonstrates how to display a rich flyout window, context menu, and balloon notification.</span></span>

> [!Note]  
> <span data-ttu-id="de2d4-113">[**Shell \_ di NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) è disponibile solo in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="de2d4-113">[**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) is only available on Windows 7 and later versions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de2d4-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de2d4-114">Requirements</span></span>



| <span data-ttu-id="de2d4-115">Prodotto</span><span class="sxs-lookup"><span data-stu-id="de2d4-115">Product</span></span>                                | <span data-ttu-id="de2d4-116">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="de2d4-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="de2d4-117">Windows</span><span class="sxs-lookup"><span data-stu-id="de2d4-117">Windows</span></span>                                | <span data-ttu-id="de2d4-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="de2d4-118">Windows 7</span></span>               |
| <span data-ttu-id="de2d4-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="de2d4-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="de2d4-120">7.0</span><span class="sxs-lookup"><span data-stu-id="de2d4-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="de2d4-121">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="de2d4-121">Downloading the Sample</span></span>

| <span data-ttu-id="de2d4-122">Location</span><span class="sxs-lookup"><span data-stu-id="de2d4-122">Location</span></span>      | <span data-ttu-id="de2d4-123">URL percorso</span><span class="sxs-lookup"><span data-stu-id="de2d4-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de2d4-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="de2d4-124">GitHub</span></span>  | [<span data-ttu-id="de2d4-125">Esempio NotificationIcon</span><span class="sxs-lookup"><span data-stu-id="de2d4-125">NotificationIcon sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a><span data-ttu-id="de2d4-126">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="de2d4-126">Building the Sample</span></span>

<span data-ttu-id="de2d4-127">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="de2d4-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="de2d4-128">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **NotificationIcon** .</span><span class="sxs-lookup"><span data-stu-id="de2d4-128">Open the command prompt window and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="de2d4-129">Immettere `msbuild NotificationIcon.sln`.</span><span class="sxs-lookup"><span data-stu-id="de2d4-129">Enter `msbuild NotificationIcon.sln`.</span></span>

<span data-ttu-id="de2d4-130">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="de2d4-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="de2d4-131">Aprire Esplora risorse e passare alla directory del progetto **NotificationIcon** .</span><span class="sxs-lookup"><span data-stu-id="de2d4-131">Open Windows Explorer and navigate to the **NotificationIcon** project directory.</span></span>
2.  <span data-ttu-id="de2d4-132">Fare doppio clic sull'icona per il file NotificationIcon. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="de2d4-132">Double-click the icon for the NotificationIcon.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="de2d4-133">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="de2d4-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="de2d4-134">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="de2d4-134">Running the Sample</span></span>

1.  <span data-ttu-id="de2d4-135">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="de2d4-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="de2d4-136">Nella riga di comando, immettere `NotificationIcon.exe` .</span><span class="sxs-lookup"><span data-stu-id="de2d4-136">At the command line, enter `NotificationIcon.exe`.</span></span> <span data-ttu-id="de2d4-137">In alternativa, in Esplora risorse fare doppio clic sull'icona per NotificationIcon.exe.</span><span class="sxs-lookup"><span data-stu-id="de2d4-137">Alternatively, from Windows Explorer double-click the icon for NotificationIcon.exe.</span></span>

> [!Note]  
> <span data-ttu-id="de2d4-138">Le icone di notifica specificate con un GUID sono protette dallo spoofing convalidando la registrazione di una sola applicazione.</span><span class="sxs-lookup"><span data-stu-id="de2d4-138">Notification icons specified with a GUID are protected against spoofing by validating that only a single application registers them.</span></span> <span data-ttu-id="de2d4-139">Questa registrazione viene eseguita la prima volta che si chiama la shell \_ NotifyIcon (NIM \_ Add,...) e viene archiviato il nome del percorso completo dell'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="de2d4-139">This registration is performed the first time you call Shell\_NotifyIcon(NIM\_ADD, ...) and the full path name of the calling application is stored.</span></span> <span data-ttu-id="de2d4-140">Se successivamente si sposta il file binario in un percorso diverso, il sistema non consentirà di aggiungere di nuovo l'icona.</span><span class="sxs-lookup"><span data-stu-id="de2d4-140">If you later move your binary file to a different location, the system will not allow the icon to be added again.</span></span> <span data-ttu-id="de2d4-141">Per ulteriori informazioni, vedere la pagina relativa all' [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .</span><span class="sxs-lookup"><span data-stu-id="de2d4-141">Please see [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) for more information.</span></span>

 

 

 



