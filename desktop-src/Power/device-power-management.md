---
description: L'API per la potenza del dispositivo consente di determinare facilmente quali dispositivi sono in grado di riattivare il sistema da uno stato di sospensione e quali Stati di sospensione supportano il risveglio dei dispositivi. Per ulteriori informazioni sugli stati di sospensione, vedere la pagina relativa agli Stati di alimentazione del sistema.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Risparmio energia del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967498"
---
# <a name="device-power-management"></a><span data-ttu-id="2eedf-104">Risparmio energia del dispositivo</span><span class="sxs-lookup"><span data-stu-id="2eedf-104">Device Power Management</span></span>

<span data-ttu-id="2eedf-105">L'API per la potenza del dispositivo consente di determinare facilmente quali dispositivi sono in grado di riattivare il sistema da uno stato di sospensione e quali Stati di sospensione supportano il risveglio dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="2eedf-105">The Device Power API makes it easy to determine which devices are able to wake the system from a sleep state, and which sleep states those devices support waking from.</span></span> <span data-ttu-id="2eedf-106">Per ulteriori informazioni sugli stati di sospensione, vedere la pagina relativa [agli Stati di alimentazione del sistema](system-power-states.md).</span><span class="sxs-lookup"><span data-stu-id="2eedf-106">For more information about sleep states, see [System Power States](system-power-states.md).</span></span>

<span data-ttu-id="2eedf-107">La funzione [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) può essere usata per eseguire ricerche nell'elenco dei dispositivi che soddisfano i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="2eedf-107">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function can be used to search the device list for devices that match specified criteria.</span></span> <span data-ttu-id="2eedf-108">I criteri possono includere la capacità del dispositivo di supportare uno stato del sistema o riattivare da tale stato.</span><span class="sxs-lookup"><span data-stu-id="2eedf-108">The criteria may include the device's ability to support a system state, or wake from that state.</span></span> <span data-ttu-id="2eedf-109">I flag attualmente supportati sono reperibili in WinNT. h e DevPower. h.</span><span class="sxs-lookup"><span data-stu-id="2eedf-109">Currently supported flags can be found in WinNT.h and DevPower.h.</span></span>

<span data-ttu-id="2eedf-110">La funzione [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) Abilita o Disabilita un dispositivo specificato per riattivare il sistema da uno stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="2eedf-110">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function enables or disables a specified device from waking the system from a sleep state.</span></span>

<span data-ttu-id="2eedf-111">L'API per l'alimentazione del dispositivo consente agli sviluppatori di creare un'esperienza utente migliore offrendo all'utente informazioni aggiuntive sulle operazioni svolte dal sistema e un maggiore controllo sui dispositivi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="2eedf-111">The Device Power API allows developers to create a better user experience by giving the user more information about what the system is doing, and more control over the devices in the system.</span></span> <span data-ttu-id="2eedf-112">La potenza del dispositivo è utile nelle situazioni in cui il consumo di energia è fondamentale, ad esempio nei dispositivi portatili in esecuzione sulle batterie.</span><span class="sxs-lookup"><span data-stu-id="2eedf-112">Device Power is useful in situations where power consumption is critical, such as in portable devices running on batteries.</span></span> <span data-ttu-id="2eedf-113">Ad esempio, lo schema di risparmio energia usato in un computer desktop potrebbe non essere lo schema ottimale per un computer portatile, quindi è possibile che l'utente desideri disabilitare la riattivazione del sistema da parte di alcuni dispositivi.</span><span class="sxs-lookup"><span data-stu-id="2eedf-113">For example, the power management scheme used in a desktop computer may not be the optimal scheme for a laptop computer, so the user may want to disable certain devices from waking the system.</span></span> <span data-ttu-id="2eedf-114">In questo modo è possibile ridurre l'energia perché i dispositivi disabilitati non risulteranno più potenti quando il sistema è in modalità sospensione.</span><span class="sxs-lookup"><span data-stu-id="2eedf-114">This can conserve energy because the disabled devices will not draw power while the system is in sleep mode.</span></span>

<span data-ttu-id="2eedf-115">Per un esempio, vedere [uso dell'API per la potenza del dispositivo](using-the-device-power-api.md).</span><span class="sxs-lookup"><span data-stu-id="2eedf-115">For an example, see [Using the Device Power API](using-the-device-power-api.md).</span></span>

 

 



