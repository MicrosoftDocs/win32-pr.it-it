---
description: Windows 10 consente all'applicazione di ottimizzare il consumo di energia quando è in esecuzione in un dispositivo mobile.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Novità del risparmio energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312006"
---
# <a name="whats-new-in-power-management"></a><span data-ttu-id="a38c8-103">Novità di Risparmio energia</span><span class="sxs-lookup"><span data-stu-id="a38c8-103">What's New in Power Management</span></span>

<span data-ttu-id="a38c8-104">Windows 10 consente all'applicazione di ottimizzare il consumo di energia quando viene eseguito in un dispositivo mobile.</span><span class="sxs-lookup"><span data-stu-id="a38c8-104">Windows 10 helps your application optimize power consumption when it's running on a mobile device.</span></span>

## <a name="battery-saver"></a><span data-ttu-id="a38c8-105">Risparmia batteria</span><span class="sxs-lookup"><span data-stu-id="a38c8-105">Battery saver</span></span>

<span data-ttu-id="a38c8-106">In questa versione, l'applicazione può ricevere una notifica quando lo screen saver è attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="a38c8-106">In this release, your application can be notified when battery saver is turned on or off.</span></span> <span data-ttu-id="a38c8-107">Rispondendo alle mutevoli condizioni di alimentazione, l'applicazione può collaborare con lo screen saver per risparmiare energia e contribuire a estendere la durata della batteria.</span><span class="sxs-lookup"><span data-stu-id="a38c8-107">By responding to changing power conditions, your application can work in concert with battery saver to save energy and help extend battery life.</span></span> <span data-ttu-id="a38c8-108">Per informazioni generali sul risparmio di batteria, vedere [batteria saver (nelle linee guida del componente hardware)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="a38c8-108">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="a38c8-109">[**GUID \_ \_ \_ Stato risparmio energia**](power-setting-guids.md) : usare questo nuovo GUID con la funzione [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) per ricevere una notifica quando lo screen saver della batteria è attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="a38c8-109">[**GUID\_POWER\_SAVING\_STATUS**](power-setting-guids.md) : Use this new GUID with the [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) function to be notified when battery saver is turned on or off.</span></span>

-   <span data-ttu-id="a38c8-110">[**Sistema \_ di \_Stato di alimentazione**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : questa struttura è stata aggiornata per supportare il risparmio di batterie.</span><span class="sxs-lookup"><span data-stu-id="a38c8-110">[**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : This structure has been updated to support battery saver.</span></span> <span data-ttu-id="a38c8-111">Il quarto membro, **SystemStatusFlag** (denominato in precedenza **Reserved1**), ora indica se il risparmio di batteria è impegnato o meno.</span><span class="sxs-lookup"><span data-stu-id="a38c8-111">The fourth member, **SystemStatusFlag** (previously named **Reserved1**), now indicates if battery saver is engaged or not.</span></span> <span data-ttu-id="a38c8-112">Utilizzare la funzione [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) per recuperare un puntatore a questa struttura.</span><span class="sxs-lookup"><span data-stu-id="a38c8-112">Use the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve a pointer to this structure.</span></span>

 

 
