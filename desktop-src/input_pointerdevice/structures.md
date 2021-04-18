---
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le strutture dello stack di input del dispositivo puntatore.
ms.assetid: 33DCB172-8D95-4205-AE2E-ADD7F3BF988A
title: Strutture (input del dispositivo puntatore)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 988a66a65581cf97406ace5481f115b15a29329a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334029"
---
# <a name="pointer-device-input-stack-structures"></a>Strutture dello stack di input del dispositivo puntatore

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le strutture [dello stack di input del dispositivo puntatore](pointer-device-stack-portal.md) .

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|---|---|
| [**POINTER_DEVICE_CURSOR_INFO**](/windows/win32/api/winuser/ns-winuser-pointer_device_cursor_info)<br/> | Contiene i mapping degli ID del cursore per i dispositivi puntatore.<br/> |
| [**POINTER_DEVICE_INFO**](/windows/win32/api/winuser/ns-winuser-pointer_device_info)<br/> | Contiene informazioni su un dispositivo puntatore. Una matrice di queste strutture viene restituita dalla funzione [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) . Una singola struttura viene restituita da una chiamata alla funzione [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) . <br/> |
| [**POINTER_DEVICE_PROPERTY**](/windows/win32/api/winuser/ns-winuser-pointer_device_property)<br/> | Contiene le proprietà del dispositivo (elementi globali HID (Human Interface Device) che corrispondono agli utilizzi HID).<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Riferimento allo stack di input del dispositivo puntatore](unified-input-stack-reference.md)
