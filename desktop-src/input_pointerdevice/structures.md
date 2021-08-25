---
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le strutture stack di input del dispositivo puntatore.
ms.assetid: 33DCB172-8D95-4205-AE2E-ADD7F3BF988A
title: Strutture (input dispositivo puntatore)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 042e1582d9c01cc6779ad672fb4935d288d29d8f442011d88e2b967b6adcf50a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830271"
---
# <a name="pointer-device-input-stack-structures"></a>Strutture dello stack di input del dispositivo puntatore

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le [strutture stack di input](pointer-device-stack-portal.md) del dispositivo puntatore.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|---|---|
| [**POINTER_DEVICE_CURSOR_INFO**](/windows/win32/api/winuser/ns-winuser-pointer_device_cursor_info)<br/> | Contiene i mapping degli ID cursore per i dispositivi puntatore.<br/> |
| [**POINTER_DEVICE_INFO**](/windows/win32/api/winuser/ns-winuser-pointer_device_info)<br/> | Contiene informazioni su un dispositivo puntatore. Una matrice di queste strutture viene restituita dalla [**funzione GetPointerDevices.**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) Una singola struttura viene restituita da una chiamata alla [**funzione GetPointerDevice.**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) <br/> |
| [**POINTER_DEVICE_PROPERTY**](/windows/win32/api/winuser/ns-winuser-pointer_device_property)<br/> | Contiene gli elementi globali delle proprietà del dispositivo (HID, Human Interface Device) che corrispondono agli utilizzi HID.<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Informazioni di riferimento sullo stack di input del dispositivo puntatore](unified-input-stack-reference.md)
