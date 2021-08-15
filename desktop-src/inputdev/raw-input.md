---
title: Input non elaborato
description: Questa sezione descrive come il sistema fornisce input non elaborato all'applicazione e come un'applicazione riceve ed elabora tale input.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Windows Interfaccia utente,input utente
- Windows Interfaccia utente,input non elaborato
- input utente, input non elaborato
- acquisizione di input utente, input non elaborato
- input non elaborato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e26d67f2b014ce22c2d01cb4738cca4e041c59e417a216f0d75ffef6e6e4b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482757"
---
# <a name="raw-input"></a>Input non elaborato

Questa sezione descrive come il sistema fornisce input non elaborato all'applicazione e come un'applicazione riceve ed elabora tale input. L'input non elaborato viene talvolta definito input generico.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                           | Descrizione                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Informazioni sull'input non elaborato](about-raw-input.md)         | Illustra l'input dell'utente da dispositivi come i joystick, i touch screen e i microfoni.<br/> |
| [Uso dell'input non elaborato](using-raw-input.md)         | Fornisce codice di esempio per le attività relative all'input non elaborato.<br/>                                |
| [Informazioni di riferimento su input non elaborato](raw-input-reference.md) | Contiene il riferimento all'API.<br/>                                                          |



 

### <a name="functions"></a>Funzioni



| Nome                                                                 | Descrizione                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | Chiama la procedura di input non elaborata predefinita per fornire l'elaborazione predefinita per tutti i messaggi di input non elaborati che un'applicazione non elabora. Questa funzione garantisce che ogni messaggio sia elaborato. [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) viene chiamato con gli stessi parametri ricevuti dalla routine della finestra. <br/> |
| [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | Esegue una lettura memorizzata nel buffer dei dati di input non elaborati.<br/>                                                                                                                                                                                                                                                              |
| [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | Ottiene l'input non elaborato dal dispositivo specificato.<br/>                                                                                                                                                                                                                                                                |
| [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | Ottiene informazioni sul dispositivo di input non elaborato.<br/>                                                                                                                                                                                                                                                                 |
| [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | Enumera i dispositivi di input non elaborati collegati al sistema. <br/>                                                                                                                                                                                                                                                    |
| [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | Ottiene le informazioni sui dispositivi di input non elaborati per l'applicazione corrente.<br/>                                                                                                                                                                                                                                |
| [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | Registra i dispositivi che forniscono i dati di input non elaborati.<br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a>Macro



| Nome                                                            | Descrizione                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**OTTENERE \_ IL CODICE RAWINPUT \_ \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | Ottiene il codice di input *da wParam* in [**WM \_ INPUT.**](wm-input.md)<br/>                              |
| [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | Ottiene la posizione della struttura successiva in una matrice di [**strutture RAWINPUT.**](/windows/win32/api/winuser/ns-winuser-rawinput) <br/> |



 

### <a name="notifications"></a>Notifiche



| Nome                                                        | Descrizione                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [**WM \_ INPUT**](wm-input.md)                               | Inviato alla finestra che riceve input non elaborato. <br/>            |
| [**MODIFICA \_ DEL DISPOSITIVO DI INPUT \_ \_ WM**](wm-input-device-change.md) | Inviato alla finestra registrata per ricevere input non elaborato. <br/> |



 

### <a name="structures"></a>Strutture



| Nome                                                            | Descrizione                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**RAWHID**](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | Descrive il formato dell'input non elaborato da un dispositivo HID (Human Interface Device). <br/> |
| [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | Contiene l'input non elaborato da un dispositivo. <br/>                                      |
| [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | Definisce le informazioni per i dispositivi di input non elaborati. <br/>                             |
| [**RAWINPUTDEVICELIST**](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | Contiene informazioni su un dispositivo di input non elaborato.<br/>                              |
| [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | Contiene le informazioni di intestazione che fanno parte dei dati di input non elaborati. <br/>        |
| [**RAWKEYBOARD**](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | Contiene informazioni sullo stato della tastiera. <br/>                      |
| [**RAWMOUSE**](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | Contiene informazioni sullo stato del mouse. <br/>                         |
| [**INFORMAZIONI \_ SUL \_ DISPOSITIVO RID**](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | Definisce i dati di input non elaborati provenienti da qualsiasi dispositivo. <br/>                         |
| [**RID \_ DEVICE \_ INFO \_ HID**](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | Definisce i dati di input non elaborati provenienti dall'HID specificato. <br/>                  |
| [**RID \_ DEVICE \_ INFO \_ KEYBOARD**](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | Definisce i dati di input non elaborati provenienti dalla tastiera specificata. <br/>             |
| [**RID \_ DEVICE \_ INFO \_ MOUSE**](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | Definisce i dati di input non elaborati provenienti dal mouse specificato.<br/>                 |



 

 

