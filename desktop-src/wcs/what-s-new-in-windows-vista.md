---
title: Novità di Windows Vista
description: La versione 1,0 di gestione colori immagine (ICM) è stata distribuita in Microsoft Windows 95 e fornisce funzionalità di base per la gestione dei colori nei contesti di dispositivi Windows.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Windows Color System (WCS), Windows Vista
- WCS (Windows Color System), Windows Vista
- Gestione colori immagine, Windows Vista
- gestione dei colori, Windows Vista
- colori, Windows Vista
- Sistema di colori Windows (WCS), sistemi operativi
- WCS (sistema di colori Windows), sistemi operativi
- Gestione colori immagine, sistemi operativi
- gestione dei colori, sistemi operativi
- colori, sistemi operativi
- Gestione colori immagine (ICM)
- ICM (gestione colori immagine)
- Gestione dei colori di Windows Vista
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320205"
---
# <a name="whats-new-in-windows-vista"></a>Novità di Windows Vista

La versione 1,0 di gestione colori immagine (ICM) è stata distribuita in Microsoft Windows 95 e fornisce funzionalità di base per la gestione dei colori nei contesti di dispositivi Windows.

ICM versione 2,0 è stato fornito in Windows 98, Windows Millennium Edition, Windows 2000 e WindowsXP ed è stata inclusa un'ampia gamma di nuove funzioni che implementavano la gestione dei colori all'esterno dei contesti di dispositivo. Queste nuove funzioni erano adatte per requisiti di gestione dei colori più complessi e davano alle applicazioni un maggiore controllo sul processo di gestione dei colori.

Con il rilascio di Windows Vista, ICM 2,0 è ora incluso in Windows Color System (WCS) 1,0, che aggiunge altre funzionalità. Nella tabella seguente sono elencate le nuove API (Application Programming Interface) fornite in Windows Vista.

## <a name="new-api-shipping-in-windows-vista"></a>Nuove API per la distribuzione in Windows Vista



Enumerazioni

Nome API

Intestazione

Libreria

[**COLORDATATYPE**](/windows/win32/api/icm/ne-icm-colordatatype)

ICM. h

mscms. lib

[**COLORPROFILESUBTYPE**](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

ICM. h

mscms. lib

[**COLORPROFILETYPE**](/windows/win32/api/icm/ne-icm-colorprofiletype)

ICM. h

mscms. lib

[**\_ambito di \_ gestione del profilo WCS \_**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

ICM. h

mscms. lib



 



Funzioni

Nome API

Intestazione

Libreria

[**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

ICM. h

mscms. lib

[**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

ICM. h

mscms. lib

[**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

ICM. h

mscms. lib

[**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

ICM. h

mscms. lib

[**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

ICM. h

mscms. lib

[**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

ICM. h

mscms. lib

[**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

ICM. h

mscms. lib

[**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

ICM. h

mscms. lib

[**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

ICM. h

mscms. lib

[**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

ICM. h

mscms. lib

[**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

ICM. h

mscms. lib

[**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

ICM. h

mscms. lib

[**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

ICM. h

mscms. lib

[**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

ICM. h

mscms. lib

[**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

ICM. h

mscms. lib



 



Interfacce e relative funzioni

Nome API

Intestazione

Libreria

[**IDeviceModelPlugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::ColorimetricToDeviceColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::D eviceToColorimetricColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetGamutBoundaryMesh**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetGamutBoundaryMeshSize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetNeutralAxis**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetNeutralAxisSize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetNumChannels**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::GetPrimarySamples**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin:: Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

WcsPlugIn. h

N/D

[**IDeviceModelPlugin::SetTransformDeviceModelInfo**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

WcsPlugIn. h

N/D

[**IGamutMapModelPlugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

WcsPlugIn. h

N/D

[**IGamutMapModelPlugin:: Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

WcsPlugIn. h

N/D

[**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

WcsPlugIn. h

N/D



 



Strutture

Nome API

Intestazione

Libreria

[**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

WcsPlugIn. h

N/D

[**GamutBoundaryDescription**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

WcsPlugIn. h

N/D

[**XYZColorF**](https://www.bing.com/search?q=**XYZColorF**)

WcsPlugIn. h

N/D

[**JChColorF**](https://www.bing.com/search?q=**JChColorF**)

WcsPlugIn. h

N/D

[**JabColorF**](https://www.bing.com/search?q=**JabColorF**)

WcsPlugIn. h

N/D

[**GamutShell**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

WcsPlugIn. h

N/D

[**GamutShellTriangle**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

WcsPlugIn. h

N/D

[**PrimaryJabColors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

WcsPlugIn. h

N/D

[**PrimaryXYZColors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

WcsPlugIn. h

N/D



 

 

 