---
title: Disabilitazione delle funzionalità di Servizi Desktop remoto
description: Per una maggiore sicurezza, è possibile scegliere di disabilitare Servizi Desktop remoto funzionalità.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/01/2020
ms.locfileid: "103963639"
---
# <a name="disabling-remote-desktop-services-features"></a><span data-ttu-id="7f226-103">Disabilitazione delle funzionalità di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="7f226-103">Disabling Remote Desktop Services features</span></span>

<span data-ttu-id="7f226-104">Per una maggiore sicurezza, è possibile scegliere di disabilitare Servizi Desktop remoto funzionalità come il reindirizzamento degli Appunti e il reindirizzamento della stampante per i client che si connettono ai server di host sessione Desktop remoto (host sessione Desktop remoto) utilizzando il Desktop remoto controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="7f226-104">For enhanced security, you might choose to disable Remote Desktop Services features such as clipboard redirection and printer redirection for clients that connect to Remote Desktop Session Host (RD Session Host) servers using the Remote Desktop ActiveX Control.</span></span>

<span data-ttu-id="7f226-105">**Per disabilitare le funzionalità di Servizi Desktop remoto**</span><span class="sxs-lookup"><span data-stu-id="7f226-105">**To disable Remote Desktop Services features**</span></span>

1.  <span data-ttu-id="7f226-106">Modificare il registro di sistema del computer client e aggiungere le chiavi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f226-106">Edit the registry of the client computer and add the following keys:</span></span>

    -   <span data-ttu-id="7f226-107">**\_Computer locale \_ HKEY \\ software \\ Microsoft \\ Terminal Server \\ DisableClipboardRedirection**</span><span class="sxs-lookup"><span data-stu-id="7f226-107">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableClipboardRedirection**</span></span>
    -   <span data-ttu-id="7f226-108">**\_Computer locale \_ HKEY \\ software \\ Microsoft \\ Terminal Server \\ DisableDriveRedirection**</span><span class="sxs-lookup"><span data-stu-id="7f226-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableDriveRedirection**</span></span>
    -   <span data-ttu-id="7f226-109">**\_Computer locale \_ HKEY \\ software \\ Microsoft \\ Terminal Server \\ DisablePrinterRedirection**</span><span class="sxs-lookup"><span data-stu-id="7f226-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisablePrinterRedirection**</span></span>

2.  <span data-ttu-id="7f226-110">Impostare il valore di entrambe le chiavi su **reg \_ DWORD** 1.</span><span class="sxs-lookup"><span data-stu-id="7f226-110">Set the value of both keys to **REG\_DWORD** 1.</span></span>

 

 




