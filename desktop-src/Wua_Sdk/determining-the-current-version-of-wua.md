---
description: Determinare la versione di Windows Update Agent (WUA) prima di usarla.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Determinazione della versione corrente di WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309732"
---
# <a name="determining-the-current-version-of-wua"></a><span data-ttu-id="75d79-103">Determinazione della versione corrente di WUA</span><span class="sxs-lookup"><span data-stu-id="75d79-103">Determining the Current Version of WUA</span></span>

<span data-ttu-id="75d79-104">Per informazioni generali sull'aggiornamento del WUA, incluse le istruzioni dettagliate per determinare a livello di codice dall'interno dell'app se la versione di WUA in esecuzione nel computer soddisfa le esigenze, vedere [aggiornamento dell'agente di Windows Update](updating-the-windows-update-agent.md).</span><span class="sxs-lookup"><span data-stu-id="75d79-104">For general information on updating the WUA, including step by step instructions to programmatically determine from within your app whether the version of WUA that is running on the computer meets your needs, see [Updating the Windows Update Agent](updating-the-windows-update-agent.md).</span></span>

<span data-ttu-id="75d79-105">Nelle versioni di Windows precedenti a Windows 7 e Windows Server 2008 R2, è necessario determinare la versione installata di Windows Update Agent (WUA) prima di usarla.</span><span class="sxs-lookup"><span data-stu-id="75d79-105">On versions of Windows prior to Windows 7 and Windows Server 2008 R2, you should determine the installed version of Windows Update Agent (WUA) before you use it.</span></span> <span data-ttu-id="75d79-106">La versione corrente di WUA è determinata dalla versione del Wuaueng.dll in esecuzione nella \\ sottodirectory System32 dell'installazione di Windows corrente.</span><span class="sxs-lookup"><span data-stu-id="75d79-106">The current version of WUA is determined by the version of the Wuaueng.dll that is running in the \\System32 subdirectory of the current Windows installation.</span></span> <span data-ttu-id="75d79-107">Se la versione di Wuaueng.dll è la versione 5.4.3790.1000 o successiva, WUA è installato.</span><span class="sxs-lookup"><span data-stu-id="75d79-107">If the version of Wuaueng.dll is version 5.4.3790.1000 or a later version, WUA is installed.</span></span> <span data-ttu-id="75d79-108">Una versione precedente A 5.4.3790.1000 indica che è installato software Update Services (SUS) 1,0.</span><span class="sxs-lookup"><span data-stu-id="75d79-108">A version that is earlier than 5.4.3790.1000 indicates that Software Update Services (SUS) 1.0 is installed.</span></span>

<span data-ttu-id="75d79-109">Quando viene effettuata una chiamata a SUS 1,0 usando l'API WUA, viene restituito un **HRESULT** di Wu \_ E \_ au \_ LEGACYSERVER.</span><span class="sxs-lookup"><span data-stu-id="75d79-109">When a call is made to SUS 1.0 by using the WUA API, an **HRESULT** of WU\_E\_AU\_LEGACYSERVER is returned.</span></span>

<span data-ttu-id="75d79-110">È anche possibile usare il metodo [**IWindowsUpdateAgentInfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) per recuperare la versione del file corrente di Wuapi.dll in esecuzione in un computer.</span><span class="sxs-lookup"><span data-stu-id="75d79-110">You can also use the [**IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) method to retrieve the current file version of Wuapi.dll that is running on a computer.</span></span> <span data-ttu-id="75d79-111">L'interfaccia [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) non è supportata in WUA 1,0.</span><span class="sxs-lookup"><span data-stu-id="75d79-111">The [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) interface is not supported in WUA 1.0.</span></span>
