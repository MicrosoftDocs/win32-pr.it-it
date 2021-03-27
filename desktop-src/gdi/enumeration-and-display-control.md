---
description: Per enumerare tutti i dispositivi nel computer, chiamare la funzione EnumDisplayDevices. Le informazioni restituite indicano anche quale monitoraggio fa parte del desktop.
ms.assetid: 834dee04-66fa-42eb-adff-c08a74c6cea8
title: Enumerazione e controllo di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8cdfd5e3b1c6ebb5ff0d4ebdfa1ab44b45c2c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049727"
---
# <a name="enumeration-and-display-control"></a><span data-ttu-id="e7cc8-104">Enumerazione e controllo di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="e7cc8-104">Enumeration and Display Control</span></span>

<span data-ttu-id="e7cc8-105">Per enumerare tutti i dispositivi nel computer, chiamare la funzione [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) .</span><span class="sxs-lookup"><span data-stu-id="e7cc8-105">To enumerate all the devices on the computer, call the [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) function.</span></span> <span data-ttu-id="e7cc8-106">Le informazioni restituite indicano anche quale monitoraggio fa parte del desktop.</span><span class="sxs-lookup"><span data-stu-id="e7cc8-106">The information that is returned also indicates which monitor is part of the desktop.</span></span>

<span data-ttu-id="e7cc8-107">Per enumerare i dispositivi sul desktop che intersecano un'area di ritaglio, chiamare [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors).</span><span class="sxs-lookup"><span data-stu-id="e7cc8-107">To enumerate the devices on the desktop that intersect a clipping region, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors).</span></span> <span data-ttu-id="e7cc8-108">Viene restituito l'handle HMONITOR per ogni monitoraggio, che viene usato con [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span><span class="sxs-lookup"><span data-stu-id="e7cc8-108">This returns the HMONITOR handle to each monitor, which is used with [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span> <span data-ttu-id="e7cc8-109">Per enumerare tutti i dispositivi nello schermo virtuale, usare **EnumDisplayMonitors**.</span><span class="sxs-lookup"><span data-stu-id="e7cc8-109">To enumerate all the devices in the virtual screen, use **EnumDisplayMonitors**.</span></span> <span data-ttu-id="e7cc8-110">come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e7cc8-110">as shown in the following code:</span></span>


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



<span data-ttu-id="e7cc8-111">Per ottenere informazioni su un dispositivo di visualizzazione, usare [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) o [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).</span><span class="sxs-lookup"><span data-stu-id="e7cc8-111">To get information about a display device, use [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) or [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).</span></span>

<span data-ttu-id="e7cc8-112">La funzione [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) viene usata per controllare i dispositivi di visualizzazione nel computer.</span><span class="sxs-lookup"><span data-stu-id="e7cc8-112">The [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) function is used to control the display devices on the computer.</span></span> <span data-ttu-id="e7cc8-113">Può modificare la configurazione dei dispositivi, ad esempio specificando la posizione di un monitoraggio sul desktop virtuale e modificando la profondità di bit di qualsiasi visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e7cc8-113">It can modify the configuration of the devices, such as specifying the position of a monitor on the virtual desktop and changing the bit depth of any display.</span></span> <span data-ttu-id="e7cc8-114">In genere, un'applicazione non utilizza questa funzione.</span><span class="sxs-lookup"><span data-stu-id="e7cc8-114">Typically, an application does not use this function.</span></span> <span data-ttu-id="e7cc8-115">Per aggiungere un monitor di visualizzazione a un sistema a più monitor a livello di codice, impostare **DEVMODE. dmFields** sulla \_ posizione DM e specificare una posizione (usando **DEVMODE. dmPosition** ) per il monitoraggio da aggiungere che sia adiacente ad almeno un pixel dell'area di visualizzazione di un monitor esistente.</span><span class="sxs-lookup"><span data-stu-id="e7cc8-115">To add a display monitor to a multiple-monitor system programmatically, set **DEVMODE.dmFields** to DM\_POSITION and specify a position (using **DEVMODE.dmPosition** ) for the monitor you are adding that is adjacent to at least one pixel of the display area of an existing monitor.</span></span> <span data-ttu-id="e7cc8-116">Per scollegare il monitoraggio, impostare **DEVMODE. dmFields** sulla \_ posizione DM e impostare **DEVMODE. DmPelsWidth** e **DEVMODE. dmPelsHeight** su zero.</span><span class="sxs-lookup"><span data-stu-id="e7cc8-116">To detach the monitor, set **DEVMODE.dmFields** to DM\_POSITION and set **DEVMODE.dmPelsWidth** and **DEVMODE.dmPelsHeight** to zero.</span></span>

<span data-ttu-id="e7cc8-117">Il codice seguente illustra come scollegare tutti i dispositivi di visualizzazione secondari dal desktop:</span><span class="sxs-lookup"><span data-stu-id="e7cc8-117">The following code demonstrates how to detach all secondary display devices from the desktop:</span></span>


```
void DetachDisplay()
{
    BOOL            FoundSecondaryDisp = FALSE;
    DWORD           DispNum = 0;
    DISPLAY_DEVICE  DisplayDevice;
    LONG            Result;
    TCHAR           szTemp[200];
    int             i = 0;
    DEVMODE   defaultMode;

    // initialize DisplayDevice
    ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
    DisplayDevice.cb = sizeof(DisplayDevice);

    // get all display devices
    while (EnumDisplayDevices(NULL, DispNum, &DisplayDevice, 0))
        {
        ZeroMemory(&defaultMode, sizeof(DEVMODE));
        defaultMode.dmSize = sizeof(DEVMODE);
        if ( !EnumDisplaySettings((LPSTR)DisplayDevice.DeviceName, ENUM_REGISTRY_SETTINGS, &defaultMode) )
                  OutputDebugString("Store default failed\n");

        if ((DisplayDevice.StateFlags & DISPLAY_DEVICE_ATTACHED_TO_DESKTOP) &&
            !(DisplayDevice.StateFlags & DISPLAY_DEVICE_PRIMARY_DEVICE))
            {
            DEVMODE    DevMode;
            ZeroMemory(&DevMode, sizeof(DevMode));
            DevMode.dmSize = sizeof(DevMode);
            DevMode.dmFields = DM_PELSWIDTH | DM_PELSHEIGHT | DM_BITSPERPEL | DM_POSITION
                        | DM_DISPLAYFREQUENCY | DM_DISPLAYFLAGS ;
            Result = ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName, 
                                            &DevMode,
                                            NULL,
                                            CDS_UPDATEREGISTRY,
                                            NULL);

            //The code below shows how to re-attach the secondary displays to the desktop

            //ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName,
            //                       &defaultMode,
            //                       NULL,
            //                       CDS_UPDATEREGISTRY,
            //                       NULL);

            }

        // Reinit DisplayDevice just to be extra clean

        ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
        DisplayDevice.cb = sizeof(DisplayDevice);
        DispNum++;
        } // end while for all display devices
}
```



<span data-ttu-id="e7cc8-118">Per ogni dispositivo di visualizzazione, l'applicazione può salvare le informazioni nel registro di sistema che descrivono i parametri di configurazione per il dispositivo, nonché i parametri di percorso.</span><span class="sxs-lookup"><span data-stu-id="e7cc8-118">For each display device, the application can save information in the registry that describes the configuration parameters for the device, as well as location parameters.</span></span> <span data-ttu-id="e7cc8-119">L'applicazione può inoltre determinare quali visualizzazioni fanno parte del desktop e quali non lo sono, tramite il \_ dispositivo di visualizzazione \_ collegato \_ al \_ flag del desktop nella struttura del [**\_ dispositivo di visualizzazione**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .</span><span class="sxs-lookup"><span data-stu-id="e7cc8-119">The application can also determine which displays are part of the desktop, and which are not, through the DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span> <span data-ttu-id="e7cc8-120">Una volta archiviate tutte le informazioni di configurazione nel registro di sistema, l'applicazione può chiamare nuovamente [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) per modificare dinamicamente le impostazioni, senza che sia necessario riavviare.</span><span class="sxs-lookup"><span data-stu-id="e7cc8-120">Once all the configuration information is stored in the registry, the application can call [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) again to dynamically change the settings, with no restart required.</span></span>

 

 



