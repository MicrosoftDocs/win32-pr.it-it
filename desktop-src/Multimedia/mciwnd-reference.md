---
title: Riferimento a MCIWnd
description: Riferimento a MCIWnd
ms.assetid: 11fba6bb-17f1-4fbe-b148-4755a3c6216a
keywords:
- MCI (Media Control Interface), Guida di riferimento a MCIWnd
- Classe della finestra MCIWnd, riferimento
- Finestra di MCIWnd, riferimento
- Riferimento a MCIWnd, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76333f38a5dec3edaadcae69777703ebea61296f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471059"
---
# <a name="mciwnd-reference"></a>Riferimento a MCIWnd

In questa sezione vengono descritte le funzioni, i messaggi e le macro associate alla classe della finestra MCIWnd. Questi elementi vengono raggruppati come indicato di seguito.

## <a name="window-management"></a>Gestione finestre

-   [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
-   [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
-   [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
-   [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass)

## <a name="file-and-device-management"></a>Gestione di file e dispositivi

-   [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose)
-   [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy)
-   [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
-   [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
-   [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
-   [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog)
-   [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave)
-   [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog)

## <a name="playback-options"></a>Opzioni di riproduzione

-   [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
-   [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay)
-   [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
-   [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
-   [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
-   [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
-   [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)

## <a name="recording"></a>Registrazione

-   [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord)

## <a name="positioning"></a>Posizionamento

-   [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)
-   [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
-   [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
-   [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
-   [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
-   [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
-   [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome)
-   [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
-   [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep)

## <a name="pause-and-resume-playback"></a>Sospendere e riprendere la riproduzione

-   [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
-   [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay)
-   [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
-   [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
-   [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
-   [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
-   [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)

## <a name="performance-tuning"></a>Ottimizzazione delle prestazioni

-   [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
-   [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
-   [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
-   [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
-   [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
-   [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)

## <a name="image-and-palette-adjustments"></a>Regolazioni di immagini e tavolozza

-   [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
-   [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
-   [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
-   [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
-   [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource)
-   [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
-   [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)

## <a name="event-and-error-notification"></a>Notifica degli eventi e degli errori

-   [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
-   [**\_NOTIFYERROR MCIWNDM**](mciwndm-notifyerror.md)
-   [**\_NOTIFYMEDIA MCIWNDM**](mciwndm-notifymedia.md)
-   [**\_NOTIFYMODE MCIWNDM**](mciwndm-notifymode.md)
-   [**\_NOTIFYPOS MCIWNDM**](mciwndm-notifypos.md)
-   [**\_NOTIFYSIZE MCIWNDM**](mciwndm-notifysize.md)

## <a name="time-formats"></a>Formati di ora

-   [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
-   [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
-   [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
-   [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
-   [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)

## <a name="status-updates"></a>Aggiornamenti dello stato

-   [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
-   [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
-   [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
-   [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
-   [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)

## <a name="device-capabilities"></a>Funzionalità del dispositivo

-   [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
-   [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
-   [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
-   [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
-   [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
-   [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)

## <a name="mci-device-settings"></a>Impostazioni del dispositivo MCI

-   [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
-   [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice)
-   [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
-   [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
-   [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)

## <a name="mci-command-string-interface"></a>Interfaccia Command-String MCI

-   [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
-   [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classe della finestra MCIWnd](mciwnd-window-class.md)
</dt> </dl>

 

 




