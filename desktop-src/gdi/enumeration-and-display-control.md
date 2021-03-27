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
# <a name="enumeration-and-display-control"></a>Enumerazione e controllo di visualizzazione

Per enumerare tutti i dispositivi nel computer, chiamare la funzione [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) . Le informazioni restituite indicano anche quale monitoraggio fa parte del desktop.

Per enumerare i dispositivi sul desktop che intersecano un'area di ritaglio, chiamare [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors). Viene restituito l'handle HMONITOR per ogni monitoraggio, che viene usato con [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa). Per enumerare tutti i dispositivi nello schermo virtuale, usare **EnumDisplayMonitors**. come illustrato nel codice seguente:


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



Per ottenere informazioni su un dispositivo di visualizzazione, usare [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) o [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).

La funzione [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) viene usata per controllare i dispositivi di visualizzazione nel computer. Può modificare la configurazione dei dispositivi, ad esempio specificando la posizione di un monitoraggio sul desktop virtuale e modificando la profondità di bit di qualsiasi visualizzazione. In genere, un'applicazione non utilizza questa funzione. Per aggiungere un monitor di visualizzazione a un sistema a più monitor a livello di codice, impostare **DEVMODE. dmFields** sulla \_ posizione DM e specificare una posizione (usando **DEVMODE. dmPosition** ) per il monitoraggio da aggiungere che sia adiacente ad almeno un pixel dell'area di visualizzazione di un monitor esistente. Per scollegare il monitoraggio, impostare **DEVMODE. dmFields** sulla \_ posizione DM e impostare **DEVMODE. DmPelsWidth** e **DEVMODE. dmPelsHeight** su zero.

Il codice seguente illustra come scollegare tutti i dispositivi di visualizzazione secondari dal desktop:


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



Per ogni dispositivo di visualizzazione, l'applicazione può salvare le informazioni nel registro di sistema che descrivono i parametri di configurazione per il dispositivo, nonché i parametri di percorso. L'applicazione può inoltre determinare quali visualizzazioni fanno parte del desktop e quali non lo sono, tramite il \_ dispositivo di visualizzazione \_ collegato \_ al \_ flag del desktop nella struttura del [**\_ dispositivo di visualizzazione**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) . Una volta archiviate tutte le informazioni di configurazione nel registro di sistema, l'applicazione può chiamare nuovamente [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) per modificare dinamicamente le impostazioni, senza che sia necessario riavviare.

 

 



