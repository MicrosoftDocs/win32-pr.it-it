---
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le funzioni dello stack di input del dispositivo puntatore.
ms.assetid: 44942954-3EA6-4C33-8CF1-E8BF72A914CB
title: Funzioni (stack di input del dispositivo puntatore)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: cfba2a0011747402af81d1f1379076282b65ca74
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334031"
---
# <a name="pointer-device-input-stack-functions"></a>Funzioni dello stack di input del dispositivo puntatore

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le funzioni [dello stack di input del dispositivo puntatore](pointer-device-stack-portal.md) .

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|---|---|
| [**CreateSyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-createsyntheticpointerdevice)<br/> | Configura il dispositivo di inserimento del puntatore per l'applicazione chiamante e inizializza il numero massimo di puntatori simultanei che l'app può inserire.<br/> |
| [**DestroySyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-destroysyntheticpointerdevice)<br/> | Elimina il dispositivo di inserimento del puntatore specificato.<br/> |
| [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice)<br/> | Ottiene informazioni sul dispositivo puntatore.<br/> |
| [**GetPointerDeviceCursors**](/windows/win32/api/winuser/nf-winuser-getpointerdevicecursors)<br/> | Ottiene gli ID del cursore di cui è stato eseguito il mapping ai cursori associati a un dispositivo puntatore.<br/> |
| [**GetPointerDeviceProperties**](/windows/win32/api/winuser/nf-winuser-getpointerdeviceproperties)<br/> | Ottiene le proprietà del dispositivo che non sono incluse nella struttura di [**\_ \_ informazioni sul dispositivo del puntatore**](/previous-versions/windows/desktop/api) . <br/> |
| [**GetPointerDeviceRects**](/windows/win32/api/winuser/nf-winuser-getpointerdevicerects)<br/> | Ottiene l'intervallo x e y per il dispositivo puntatore (in HIMETRIC) e l'intervallo x e y (risoluzione corrente) per la visualizzazione a cui è stato eseguito il mapping del dispositivo puntatore. <br/> |
| [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices)<br/> | Ottiene informazioni sui dispositivi del puntatore collegati al sistema.<br/> |
| [**GetRawPointerDeviceData**](/windows/win32/api/winuser/nf-winuser-getrawpointerdevicedata)<br/> | Ottiene i dati di input non elaborati dal dispositivo puntatore. <br/> |
| [**InjectSyntheticPointerInput**](/windows/win32/api/winuser/nf-winuser-injectsyntheticpointerinput)<br/> | Simula l'input del puntatore (Pen o touch).<br/> |
| [**RegisterPointerDeviceNotifications**](/windows/win32/api/winuser/nf-winuser-registerpointerdevicenotifications)<br/> | Registra una finestra per elaborare le notifiche del dispositivo [**WM_POINTERDEVICECHANGE**](../inputmsg/wm-pointerdevicechange.md), [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md)e [**WM_POINTERDEVICEOUTOFRANGE**](../inputmsg/wm-pointerdeviceoutofrange.md) puntatore.<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Riferimento allo stack di input del dispositivo puntatore](unified-input-stack-reference.md)
