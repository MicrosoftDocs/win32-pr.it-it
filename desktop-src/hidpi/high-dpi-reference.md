---
title: Informazioni di riferimento su valori DPI elevati
description: Informazioni di riferimento su valori DPI elevati
ms.assetid: 07A2D45E-721C-4DA8-82A5-38B2FB94BC6D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c6a9302541683dbf97c06194285f9e8cfcf3c0
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118416"
---
# <a name="high-dpi-reference"></a>Informazioni di riferimento su valori DPI elevati

## <a name="functions"></a>Funzioni



| Argomento                                                                                         |Descrizione                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi)                             | Variante di [AdjustWindowRectEx](/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex) che restituisce valori ridimensionati in base a un valore DPI specifico.       |
| [**AreDpiAwarenessContextsEqual**](/windows/desktop/api/Winuser/nf-winuser-aredpiawarenesscontextsequal)                     | Determina se due [**valori DPI \_ AWARENESS \_ CONTEXT**](dpi-awareness-context.md) sono equivalenti.                                                            |
| [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)                           | Abilita il ridimensionamento automatico dell'area non client della finestra di primo livello specificata.                                                                               |
| [**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getawarenessfromdpiawarenesscontext)       | Recupera il valore [**DPI \_ AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness) da un [**contesto di \_ \_ consapevolezza DPI**](dpi-awareness-context.md)                                       |
| [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)                                             | Esegue una query sulle informazioni DPI associate a un monitoraggio.                                                                                                            |
| [**GetDpiForSystem**](/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem)                                               | Restituisce il valore DPI di sistema.                                                                                                                                           |
| [**GetDpiForWindow**](/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow)                                               | Restituisce l'oggetto DPI corrente per la finestra specificata.                                                                                                                 |
| [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)                                 | Recupera la modalità di virtualizzazione DPI del processo specificato.                                                                                                   |
| [**GetSystemMetricsForDpi**](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)                                 | Variante di [GetSystemMetrics](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) che restituisce valori ridimensionati in base a un valore DPI specifico.         |
| [**GetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getthreaddpiawarenesscontext)                     | Recupera il contesto di riconoscimento DPI attivo per il thread corrente.                                                                                                |
| [**GetWindowDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getwindowdpiawarenesscontext)                     | Recupera il contesto di riconoscimento DPI per una finestra.                                                                                                                 |
| [**IsValidDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-isvaliddpiawarenesscontext)                         | Determina se un [**contesto DPI \_ AWARENESS \_**](dpi-awareness-context.md) è valido e supportato dal sistema corrente.                                            |
| [**LogicalToPhysicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi) | Converte un punto in una finestra da coordinate logiche in coordinate fisiche, indipendentemente dal riconoscimento DPI del chiamante.                                   |
| [**PhysicalToLogicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi) | Converte un punto in una finestra da coordinate fisiche in coordinate logiche, indipendentemente dal riconoscimento DPI del chiamante.                                   |
| [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)                                 | Imposta la modalità di virtualizzazione DPI per il processo corrente.                                                                                                         |
| [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)                     | Modifica il contesto di riconoscimento DPI attivo per il thread corrente.                                                                                                  |
| [**SystemParametersInfoForDpi**](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)                         | Variante di [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) che restituisce valori ridimensionati in base a un valore DPI specifico.     |
| [**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)                   | Imposta il contesto di riconoscimento DPI per il processo corrente.                                                                                                           |
| [**SetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior)                         | Esegue l'override del comportamento di ridimensionamento DPI per monitoraggio predefinito di una finestra di dialogo.                                                                                               |
| [**GetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogdpichangebehavior)                         | Recupera il comportamento di ridimensionamento DPI per monitoraggio di una finestra di dialogo.                                                                                                       |
| [**SetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior)                     | Esegue l'override del comportamento di ridimensionamento DPI per monitoraggio predefinito di una finestra figlio in una finestra di dialogo.                                                                             |
| [**GetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior)                     | Recupera tutti gli override del comportamento di ridimensionamento DPI per monitoraggio di una finestra figlio in una finestra di dialogo.                                                                           |
| [**OpenThemeDataForDpi**](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedatafordpi)                                       | Variante di [OpenThemeData che apre](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata) gli handle del tema associati a un valore DPI specifico. |
| [**GetSystemDpiForProcess**](/windows/desktop/api/winuser/nf-winuser-getsystemdpiforprocess)                                 | Recupera il valore DPI di sistema associato a un determinato processo.                                                                                                         |
| [**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)                   | Recupera il valore DPI da un handle [DPI \_ AWARENESS \_ CONTEXT](dpi-awareness-context.md) specificato.                                                                       |
| [**SetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior)                       | Esegue l'override del comportamento di hosting DPI predefinito del thread corrente.                                                                                                 |
| [**GetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior)                       | Recupera il comportamento di hosting DPI del thread corrente.                                                                                                         |
| [**GetWindowDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior)                       | Recupera il comportamento di hosting DPI della finestra specificata.                                                                                                       |



 

## <a name="types"></a>Tipi



| Argomento                                                                           |Descrizione                                                                                        |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**CONSAPEVOLEZZA DPI \_**](/windows/desktop/api/windef/ne-windef-dpi_awareness)                                    | Rappresenta le modalità di virtualizzazione delle coordinate DPI.                                        |
| [**CONTESTO DI CONSAPEVOLEZZA DPI \_ \_**](dpi-awareness-context.md)                   | Token che rappresenta una modalità di virtualizzazione DPI e i comportamenti associati.           |
| [**COMPORTAMENTI \_ DI MODIFICA \_ DPI DEL CONTROLLO \_ \_ DIALOG**](/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors) | Descrive le sostituzioni del comportamento di ridimensionamento DPI per ogni monitoraggio per le finestre figlio all'interno di finestre di dialogo. |
| [**COMPORTAMENTI \_ DI MODIFICA DPI DELLA FINESTRA DI \_ \_ DIALOGO**](/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors)      | Descrive le sostituzioni del comportamento di ridimensionamento DPI per ogni monitoraggio per i dialoghe.                      |
| [**MONITORARE \_ IL TIPO DI \_ DPI**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-monitor_dpi_type)                 | Rappresenta il tipo di DPI associato a un monitoraggio.                                  |
| [**ELABORARE \_ LA CONSAPEVOLEZZA DPI \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)                   | Rappresenta la modalità di virtualizzazione delle coordinate DPI di un processo.                        |
| [**COMPORTAMENTO DI \_ HOSTING \_ DPI**](/windows/win32/api/windef/ne-windef-dpi_hosting_behavior)                    | Rappresenta il comportamento di hosting DPI per una finestra.                                      |



 

## <a name="messages"></a>Messaggi



| Argomento                                                                   | Descrizione                                                                                                                                        |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DPICHANGED**](wm-dpichanged.md)                            | Notifica a una finestra di primo livello che il valore DPI è stato modificato.                                                                                   |
| [**WM \_ DPICHANGED \_ BEFOREPARENT**](wm-dpichanged-beforeparent.md) | Notifica a una finestra figlio che il valore DPI associato alla finestra contenitore è stato modificato. Recapitato prima che la finestra padre venga notificata. |
| [**WM \_ DPICHANGED \_ AFTERPARENT**](wm-dpichanged-afterparent.md)   | Notifica a una finestra figlio che il valore DPI associato alla finestra contenitore è stato modificato. Recapitato dopo la notifica della finestra padre.  |
| [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md)                | Consente alle finestre di primo livello di ridimensionarsi *in modo non lineare* in risposta alle modifiche DPI.                                                           |



 

 

 
