---
title: Novità di Windows Vista
description: La versione 1.0 di Gestione colori immagine (ICM) è stata fornita in Microsoft Windows 95 e offre funzionalità di base per la gestione dei colori all'interno Windows contesti di dispositivo.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Windows Sistema colori (WCS), Windows Vista
- WCS (Windows Color System),Windows Vista
- gestione dei colori delle immagini, Windows Vista
- gestione dei colori, Windows Vista
- colori, Windows Vista
- Windows Sistema colori (WCS), sistemi operativi
- WCS (Windows Color System),sistemi operativi
- gestione dei colori delle immagini, sistemi operativi
- gestione dei colori, sistemi operativi
- colori, sistemi operativi
- Gestione colori immagine (ICM)
- ICM (Gestione colori immagine)
- Windows Gestione dei colori di Vista
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3f6c3313a1b7ca78f0f4d3436d7bb2017b0fa794291b4bd765651aa0321166d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670737"
---
# <a name="whats-new-in-windows-vista"></a>Novità di Windows Vista

La versione 1.0 di Gestione colori immagine (ICM) è stata fornita in Microsoft Windows 95 e offre funzionalità di base per la gestione dei colori all'interno Windows contesti di dispositivo.

ICM versione 2.0 è stata recapitata in Windows 98, Windows Millennium Edition, Windows 2000 e WindowsXP ed è stata inclusa un'ampia gamma di nuove funzioni che implementavano la gestione dei colori al di fuori dei contesti di dispositivo. Queste nuove funzioni erano adatte per requisiti di gestione dei colori più impegnativi e hanno offerto alle applicazioni un maggiore controllo sul processo di gestione dei colori.

Con il rilascio di Windows Vista, ICM 2.0 è ora incluso in Windows Color System (WCS) 1.0, che aggiunge altre funzionalità. La tabella seguente elenca le nuove API (Application Programming Interface) disponibili in Windows Vista.

## <a name="new-api-shipping-in-windows-vista"></a>Nuova distribuzione di API in Windows Vista



Enumerazioni

Nome API

Intestazione

Libreria

[**COLORDATATYPE**](/windows/win32/api/icm/ne-icm-colordatatype)

icm.h

mscms.lib

[**COLORPROFILESUBTYPE**](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

icm.h

mscms.lib

[**COLORPROFILETYPE**](/windows/win32/api/icm/ne-icm-colorprofiletype)

icm.h

mscms.lib

[**AMBITO DI \_ GESTIONE DEI \_ PROFILI WCS \_**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

icm.h

mscms.lib



 



Funzioni

Nome API

Intestazione

Libreria

[**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

icm.h

mscms.lib

[**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

icm.h

mscms.lib

[**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

icm.h

mscms.lib

[**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

icm.h

mscms.lib

[**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

icm.h

mscms.lib

[**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

icm.h

mscms.lib

[**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

icm.h

mscms.lib

[**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

icm.h

mscms.lib

[**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

icm.h

mscms.lib

[**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

icm.h

mscms.lib

[**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

icm.h

mscms.lib

[**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

icm.h

mscms.lib

[**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

icm.h

mscms.lib

[**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

icm.h

mscms.lib

[**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

icm.h

mscms.lib



 



Interfacce e relative funzioni

Nome API

Intestazione

Libreria

[**IDeviceModelPlugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

WcsPlugIn.h

N/A

[**IDeviceModelPlugin::ColorimetricToDeviceColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

WcsPlugIn.h

N/A

[**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

WcsPlugIn.h

N/A

[**IDeviceModelPlugin::D eviceToColorimetricColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

WcsPlugIn.h

N/A

[**IDeviceModelPlugin::GetGamutBoundaryMesh**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

WcsPlugIn.h

N/A

[**IDeviceModelPlugin::GetGamutBoundaryMeshSize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

WcsPlugIn.h

N/A

[**IDeviceModelPlugin::GetNeutralAxis**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

WcsPlugIn.h

N/A

[**IDeviceModelPlugin::GetNeutralAxisSize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

WcsPlugIn.h

N/A

[**IDeviceModelPlugin::GetNumChannels**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

WcsPlugIn.h

N/A

[**IDeviceModelPlugin::GetPrimarySamples**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

WcsPlugIn.h

N/A

[**IDeviceModelPlugin::Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

WcsPlugIn.h

N/A

[**IDeviceModelPlugin::SetTransformDeviceModelInfo**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

WcsPlugIn.h

N/A

[**IGamutMapModelPlugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

WcsPlugIn.h

N/A

[**IGamutMapModelPlugin::Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

WcsPlugIn.h

N/A

[**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

WcsPlugIn.h

N/A



 



Strutture

Nome API

Intestazione

Libreria

[**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

WcsPlugIn.h

N/A

[**GamutBoundaryDescription**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

WcsPlugIn.h

N/A

[**XYZColorF**](https://www.bing.com/search?q=**XYZColorF**)

WcsPlugIn.h

N/A

[**JChColorF**](https://www.bing.com/search?q=**JChColorF**)

WcsPlugIn.h

N/A

[**JabColorF**](https://www.bing.com/search?q=**JabColorF**)

WcsPlugIn.h

N/A

[**GamutShell**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

WcsPlugIn.h

N/A

[**GamutShellTriangle**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

WcsPlugIn.h

N/A

[**PrimaryJabColors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

WcsPlugIn.h

N/A

[**PrimaryXYZColors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

WcsPlugIn.h

N/D



 

 

 