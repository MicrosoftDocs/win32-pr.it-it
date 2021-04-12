---
title: Riferimento DPI alto
description: .
ms.assetid: 07A2D45E-721C-4DA8-82A5-38B2FB94BC6D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec59f34aa5ed036d7f4376cb3d170b5d7849f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398872"
---
# <a name="high-dpi-reference"></a>Riferimento DPI alto

## <a name="functions"></a>Funzioni



|                                                                                          |                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Argomento**                                                                                | **Descrizione**                                                                                                                                                   |
| [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi)                             | Variante di [AdjustWindowRectEx](/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex) che restituisce i valori ridimensionati a un valore dpi specifico.       |
| [**AreDpiAwarenessContextsEqual**](/windows/desktop/api/Winuser/nf-winuser-aredpiawarenesscontextsequal)                     | Determina se due valori del [**\_ \_ contesto di riconoscimento dpi**](dpi-awareness-context.md) sono equivalenti.                                                            |
| [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)                           | Abilita il ridimensionamento automatico dell'area non client della finestra di primo livello specificata.                                                                               |
| [**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getawarenessfromdpiawarenesscontext)       | Recupera il valore di [**\_ riconoscimento dpi**](/windows/desktop/api/windef/ne-windef-dpi_awareness) da un [**\_ \_ contesto di consapevolezza dpi**](dpi-awareness-context.md)                                       |
| [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)                                             | Esegue una query sulle informazioni DPI associate a un monitoraggio.                                                                                                            |
| [**GetDpiForSystem**](/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem)                                               | Restituisce il valore DPI del sistema.                                                                                                                                           |
| [**GetDpiForWindow**](/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow)                                               | Restituisce il valore DPI corrente per la finestra specificata.                                                                                                                 |
| [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)                                 | Recupera la modalità di virtualizzazione DPI del processo specificato.                                                                                                   |
| [**GetSystemMetricsForDpi**](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)                                 | Variante di [GetSystemMetrics](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) che restituisce i valori ridimensionati a un valore dpi specifico.         |
| [**GetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getthreaddpiawarenesscontext)                     | Recupera il contesto di riconoscimento DPI attivo per il thread corrente.                                                                                                |
| [**GetWindowDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getwindowdpiawarenesscontext)                     | Recupera il contesto di consapevolezza DPI per una finestra.                                                                                                                 |
| [**IsValidDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-isvaliddpiawarenesscontext)                         | Determina se un [**\_ \_ contesto di riconoscimento dpi**](dpi-awareness-context.md) è valido e supportato dal sistema corrente.                                            |
| [**LogicalToPhysicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi) | Converte un punto in una finestra da coordinate logiche a coordinate fisiche, indipendentemente dalla conoscenza DPI del chiamante.                                   |
| [**PhysicalToLogicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi) | Converte un punto in una finestra dalle coordinate fisiche in coordinate logiche, indipendentemente dalla conoscenza DPI del chiamante.                                   |
| [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)                                 | Imposta la modalità di virtualizzazione DPI per il processo corrente.                                                                                                         |
| [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)                     | Modifica il contesto di riconoscimento DPI attivo per il thread corrente.                                                                                                  |
| [**SystemParametersInfoForDpi**](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)                         | Variante di [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) che restituisce i valori ridimensionati a un valore dpi specifico.     |
| [**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)                   | Imposta il contesto di riconoscimento DPI per il processo corrente.                                                                                                           |
| [**SetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior)                         | Esegue l'override del comportamento predefinito di ridimensionamento DPI per monitoraggio di una finestra di dialogo.                                                                                               |
| [**GetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogdpichangebehavior)                         | Recupera il comportamento di ridimensionamento DPI per monitoraggio di una finestra di dialogo.                                                                                                       |
| [**SetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior)                     | Esegue l'override del comportamento predefinito di ridimensionamento DPI per monitoraggio di una finestra figlio in una finestra di dialogo.                                                                             |
| [**GetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior)                     | Recupera qualsiasi override del comportamento di scalabilità DPI per monitoraggio di una finestra figlio in una finestra di dialogo.                                                                           |
| [**OpenThemeDataForDpi**](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedatafordpi)                                       | Variante di [OpenThemeData](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata) che apre gli handle di tema associati a un valore dpi specifico. |
| [**GetSystemDpiForProcess**](/windows/desktop/api/winuser/nf-winuser-getsystemdpiforprocess)                                 | Recupera il valore DPI di sistema associato a un processo specificato.                                                                                                         |
| [**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)                   | Recupera il valore DPI da un handle del [ \_ \_ contesto di consapevolezza dpi](dpi-awareness-context.md) specificato.                                                                       |
| [**SetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior)                       | Esegue l'override del comportamento di hosting DPI predefinito del thread corrente.                                                                                                 |
| [**GetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior)                       | Recupera il comportamento di hosting DPI del thread corrente.                                                                                                         |
| [**GetWindowDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior)                       | Recupera il comportamento di hosting DPI della finestra specificata.                                                                                                       |



 

## <a name="types"></a>Tipi



|                                                                            |                                                                                        |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Argomento**                                                                  | **Descrizione**                                                                        |
| [**\_riconoscimento dpi**](/windows/desktop/api/windef/ne-windef-dpi_awareness)                                    | Rappresenta le modalità di virtualizzazione delle coordinate DPI.                                        |
| [**\_contesto di consapevolezza dpi \_**](dpi-awareness-context.md)                   | Token che rappresenta una modalità di virtualizzazione DPI e comportamenti associati.           |
| [**\_comportamenti di \_ \_ modifica dpi del controllo \_ finestra di dialogo**](/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors) | Descrive le sostituzioni del comportamento di scalabilità DPI per monitor per le finestre figlio all'interno delle finestre di dialogo. |
| [**\_comportamenti di \_ modifica \_ dpi della finestra di dialogo**](/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors)      | Descrive le sostituzioni del comportamento di scalabilità DPI per monitor per le finestre di dialogo.                      |
| [**tipo di monitoraggio \_ dpi \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-monitor_dpi_type)                 | Rappresenta il tipo di DPI associato a un monitoraggio.                                  |
| [**\_riconoscimento dpi \_ processo**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)                   | Rappresenta la modalità di virtualizzazione delle coordinate DPI di un processo.                        |
| [**\_comportamento host \_ dpi**](/windows/win32/api/windef/ne-windef-dpi_hosting_behavior)                    | Rappresenta il comportamento di hosting DPI per una finestra.                                      |



 

## <a name="messages"></a>Messaggi



|                                                                    |                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Argomento**                                                          | **Descrizione**                                                                                                                         |
| [**\_DPICHANGED WM**](wm-dpichanged.md)                            | Notifica a una finestra di primo livello che il relativo valore DPI è stato modificato.                                                                                   |
| [**\_BEFOREPARENT DPICHANGED \_ WM**](wm-dpichanged-beforeparent.md) | Notifica a una finestra figlio che è stato modificato il valore DPI associato alla finestra che lo contiene. Recapitato prima della notifica della finestra padre. |
| [**\_AFTERPARENT DPICHANGED \_ WM**](wm-dpichanged-afterparent.md)   | Notifica a una finestra figlio che è stato modificato il valore DPI associato alla finestra che lo contiene. Recapitato dopo la notifica della finestra padre.  |
| [**\_GETDPISCALEDSIZE WM**](wm-getdpiscaledsize.md)                | Consente di ridimensionare le finestre di primo livello in modo *non lineare* in risposta alle modifiche DPI.                                                           |



 

 

 