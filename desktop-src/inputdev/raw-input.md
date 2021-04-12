---
title: Input non elaborato
description: In questa sezione viene descritto il modo in cui il sistema fornisce input non elaborato all'applicazione e il modo in cui un'applicazione riceve ed elabora tale input.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Interfaccia utente di Windows, input utente
- Interfaccia utente di Windows, input non elaborato
- input utente, input non elaborato
- acquisizione dell'input dell'utente, input non elaborato
- input non elaborato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88de70dd2b635cf7dda90f23686b9916c99be4f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398953"
---
# <a name="raw-input"></a>Input non elaborato

In questa sezione viene descritto il modo in cui il sistema fornisce input non elaborato all'applicazione e il modo in cui un'applicazione riceve ed elabora tale input. L'input non elaborato viene talvolta definito input generico.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                           | Descrizione                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Informazioni sull'input non elaborato](about-raw-input.md)         | Viene illustrato l'input dell'utente da dispositivi quali joystick, touch screen e microfoni.<br/> |
| [Uso dell'input non elaborato](using-raw-input.md)         | Fornisce il codice di esempio per le attività relative all'input non elaborato.<br/>                                |
| [Riferimento input non elaborato](raw-input-reference.md) | Contiene il riferimento all'API.<br/>                                                          |



 

### <a name="functions"></a>Funzioni



| Nome                                                                 | Descrizione                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | Chiama la procedura di input non elaborato predefinita per fornire l'elaborazione predefinita per tutti i messaggi di input non elaborati che un'applicazione non elabora. Questa funzione garantisce che ogni messaggio venga elaborato. [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) viene chiamato con gli stessi parametri ricevuti dalla routine della finestra. <br/> |
| [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | Esegue una lettura con memorizzazione nel buffer dei dati di input non elaborati.<br/>                                                                                                                                                                                                                                                              |
| [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | Ottiene l'input non elaborato dal dispositivo specificato.<br/>                                                                                                                                                                                                                                                                |
| [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | Ottiene informazioni sul dispositivo di input non elaborato.<br/>                                                                                                                                                                                                                                                                 |
| [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | Enumera i dispositivi di input non elaborati collegati al sistema. <br/>                                                                                                                                                                                                                                                    |
| [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | Ottiene le informazioni sui dispositivi di input non elaborati per l'applicazione corrente.<br/>                                                                                                                                                                                                                                |
| [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | Registra i dispositivi che forniscono i dati di input non elaborati.<br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a>Macro



| Nome                                                            | Descrizione                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**OTTENERE \_ il \_ codice rawinput \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | Ottiene il codice di input da *wParam* nell' [**\_ input WM**](wm-input.md).<br/>                              |
| [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | Ottiene la posizione della struttura successiva in una matrice di strutture [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) . <br/> |



 

### <a name="notifications"></a>Notifiche



| Nome                                                        | Descrizione                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_input WM**](wm-input.md)                               | Inviato alla finestra che sta ricevendo l'input non elaborato. <br/>            |
| [**\_modifica del \_ dispositivo di input WM \_**](wm-input-device-change.md) | Inviato alla finestra registrata per ricevere input non elaborato. <br/> |



 

### <a name="structures"></a>Strutture



| Nome                                                            | Descrizione                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**RAWHID**](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | Descrive il formato dell'input non elaborato da un dispositivo di interfaccia umana (HID). <br/> |
| [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | Contiene l'input non elaborato da un dispositivo. <br/>                                      |
| [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | Definisce le informazioni per i dispositivi di input non elaborati. <br/>                             |
| [**RAWINPUTDEVICELIST**](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | Contiene informazioni su un dispositivo di input non elaborato.<br/>                              |
| [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | Contiene le informazioni di intestazione che fanno parte dei dati di input non elaborati. <br/>        |
| [**RAWKEYBOARD**](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | Contiene informazioni sullo stato della tastiera. <br/>                      |
| [**RAWMOUSE**](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | Contiene informazioni sullo stato del mouse. <br/>                         |
| [**\_informazioni sul dispositivo RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | Definisce i dati di input non elaborati provenienti da qualsiasi dispositivo. <br/>                         |
| [**\_informazioni sul dispositivo RID \_ \_ nascoste**](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | Definisce i dati di input non elaborati provenienti dall'oggetto nascosto specificato. <br/>                  |
| [**\_ \_ tastiera informazioni sul dispositivo RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | Definisce i dati di input non elaborati provenienti dalla tastiera specificata. <br/>             |
| [**\_ \_ mouse informazioni sul dispositivo RID \_**](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | Definisce i dati di input non elaborati provenienti dal mouse specificato.<br/>                 |



 

 

