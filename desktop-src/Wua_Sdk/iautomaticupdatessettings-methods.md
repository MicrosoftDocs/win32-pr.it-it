---
description: L'interfaccia IAutomaticUpdatesSettings definisce i metodi seguenti.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Metodi IAutomaticUpdatesSettings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880390"
---
# <a name="iautomaticupdatessettings-methods"></a><span data-ttu-id="f5ed9-103">Metodi IAutomaticUpdatesSettings</span><span class="sxs-lookup"><span data-stu-id="f5ed9-103">IAutomaticUpdatesSettings Methods</span></span>

<span data-ttu-id="f5ed9-104">L'interfaccia [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) definisce i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5ed9-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following methods.</span></span>



| <span data-ttu-id="f5ed9-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="f5ed9-105">Method</span></span>                                               | <span data-ttu-id="f5ed9-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5ed9-106">Description</span></span>                                      |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="f5ed9-107">**Aggiorna**</span><span class="sxs-lookup"><span data-stu-id="f5ed9-107">**Refresh**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | <span data-ttu-id="f5ed9-108">Recupera le impostazioni di Aggiornamenti automatici più recenti.</span><span class="sxs-lookup"><span data-stu-id="f5ed9-108">Retrieves the latest Automatic Updates settings.</span></span> |
| [<span data-ttu-id="f5ed9-109">**Salva**</span><span class="sxs-lookup"><span data-stu-id="f5ed9-109">**Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | <span data-ttu-id="f5ed9-110">Applica le impostazioni di Aggiornamenti automatici correnti.</span><span class="sxs-lookup"><span data-stu-id="f5ed9-110">Applies the current Automatic Updates settings.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="f5ed9-111">In Windows RT non è più possibile usare il metodo [**IAutomaticUpdatesSettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) per configurare le impostazioni Windows Update a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="f5ed9-111">On Windows RT, you can no longer use the [**IAutomaticUpdatesSettings::Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) method to configure Windows Update settings programmatically.</span></span> <span data-ttu-id="f5ed9-112">L'operazione di configurazione non riesce se si usa **Save** per impostare un valore diverso da 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).</span><span class="sxs-lookup"><span data-stu-id="f5ed9-112">The configuration operation fails if you use **Save** to set any value other than 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).</span></span>

 

 

 



