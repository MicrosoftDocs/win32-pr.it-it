---
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le funzioni pointer device input stack.
ms.assetid: 44942954-3EA6-4C33-8CF1-E8BF72A914CB
title: Funzioni (stack di input del dispositivo puntatore)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 5101847d78f396edcb317986ab3d95d578dabdfe12197531787115f49c9a69a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611741"
---
# <a name="pointer-device-input-stack-functions"></a>Funzioni dello stack di input del dispositivo puntatore

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le funzioni [pointer device input stack.](pointer-device-stack-portal.md)

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|---|---|
| [**CreateSyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-createsyntheticpointerdevice)<br/> | Configura il dispositivo di inserimento dei puntatori per l'applicazione chiamante e inizializza il numero massimo di puntatori simultanei che l'app può inserire.<br/> |
| [**DestroySyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-destroysyntheticpointerdevice)<br/> | Elimina il dispositivo di inserimento del puntatore specificato.<br/> |
| [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice)<br/> | Ottiene informazioni sul dispositivo puntatore.<br/> |
| [**GetPointerDeviceCursors**](/windows/win32/api/winuser/nf-winuser-getpointerdevicecursors)<br/> | Ottiene gli ID cursore di cui è stato eseguito il mapping ai cursori associati a un dispositivo puntatore.<br/> |
| [**GetPointerDeviceProperties**](/windows/win32/api/winuser/nf-winuser-getpointerdeviceproperties)<br/> | Ottiene le proprietà del dispositivo che non sono incluse nella struttura [**POINTER \_ DEVICE \_ INFO.**](/previous-versions/windows/desktop/api) <br/> |
| [**GetPointerDeviceRects**](/windows/win32/api/winuser/nf-winuser-getpointerdevicerects)<br/> | Ottiene l'intervallo x e y per il dispositivo puntatore (in himetric) e l'intervallo x e y (risoluzione corrente) per la visualizzazione a cui è mappato il dispositivo puntatore. <br/> |
| [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices)<br/> | Ottiene informazioni sui dispositivi puntatore collegati al sistema.<br/> |
| [**GetRawPointerDeviceData**](/windows/win32/api/winuser/nf-winuser-getrawpointerdevicedata)<br/> | Ottiene i dati di input non elaborati dal dispositivo puntatore. <br/> |
| [**InjectSyntheticPointerInput**](/windows/win32/api/winuser/nf-winuser-injectsyntheticpointerinput)<br/> | Simula l'input del puntatore (penna o tocco).<br/> |
| [**RegisterPointerDeviceNotifications**](/windows/win32/api/winuser/nf-winuser-registerpointerdevicenotifications)<br/> | Registra una finestra per elaborare le [**WM_POINTERDEVICECHANGE,**](../inputmsg/wm-pointerdevicechange.md) [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md) [**e**](../inputmsg/wm-pointerdeviceoutofrange.md) WM_POINTERDEVICEOUTOFRANGE dispositivo puntatore.<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Informazioni di riferimento sullo stack di input del dispositivo puntatore](unified-input-stack-reference.md)
