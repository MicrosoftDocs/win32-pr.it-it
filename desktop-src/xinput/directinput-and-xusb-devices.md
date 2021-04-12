---
title: Dispositivi DirectInput e XUSB
description: Il driver per la classe del controller comune di Xbox (XUSB) in Windows implementa l'interfaccia in modalità kernel per la DLL XINPUT.
ms.assetid: 8bf47b07-a1b6-7721-2136-3853e72c71ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2b6d2857502c0e0209d94fb6d933618c180fd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339070"
---
# <a name="directinput-and-xusb-devices"></a>Dispositivi DirectInput e XUSB

Il driver per la classe del controller comune di Xbox (XUSB) in Windows implementa l'interfaccia in modalità kernel per la DLL XINPUT. Per offrire un'esperienza ottimale per i titoli legacy che usano l'API [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) con il dispositivo controller comune, il driver esporta anche un'interfaccia di classe HID (Human Interface Device), che viene prelevata da DirectInput. È stato scelto il mapping di XUSB a HID in base a un comportamento tipico in un set di applicazioni di gioco per la versione originale di XINPUT e il mapping per i sottotipi più recenti è stato aggiornato. In questo argomento viene descritto il mapping.

## <a name="human-interface-device-hid"></a>Human Interface Device (HID)

HID standard è uno standard del Comitato USB (Universal Serial Bus) proposto in origine da Microsoft per generalizzare i protocolli per i dispositivi di input. È costituito da un linguaggio di descrizione del codice byte e può esprimere gamepad, topi, joystick, controlli di limitazione e timone e Controller multiasse. Poiché questo standard è così generalizzato, potrebbe essere difficile scrivere software che utilizza l'input da dispositivi arbitrari. Per l'API [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) incentrata sul gioco è stato quindi sviluppato un sottomapping specifico dei tipi per favorire la produzione di hardware per supportare i driver.

- [Definizione di classe dispositivo USB per HID v 1.11](https://www.usb.org/document-library/device-class-definition-hid-111)

> [!Important]
> È anche possibile accedere ai dispositivi di input HID tramite l' [API RawInput](../inputdev/about-raw-input.md) ed elaborare i report di input tramite l' [API HID](/windows-hardware/drivers/hid/introduction-to-hid-concepts) di basso livello, ma il feedback delle vibrazioni non funzionerà come con [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)).

## <a name="mappings"></a>Mapping

Il driver XUSB implementa sia un'interfaccia di classe XUSB che un'interfaccia di classe HID per i dispositivi per supportare l'utilizzo di XINPUT e [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) . Questo mapping è basato sulle informazioni del sottotipo XUSB. Il driver implementa quattro gruppi distinti di mapping.

| Sottotipo XUSB                                      | Mapping                     |
|---------------------------------------------------|-----------------------------|
| XINPUT \_ DEVSUBTYPE \_ Gamepad (sottotipo 1)           | Game pad                     |
| XINPUT \_ DEVSUBTYPE \_ Wheel (sottotipo 2)             | Selettore circolare                       |
| XINPUT \_ DEVSUBTYPE \_ Arcade \_ Stick (sottotipo 3)     | Arcade stick/arcade Pad     |
| XINPUT \_ DEVSUBTYPE \_ Flight \_ Stick (sottotipo 4)     | Volo                |
| XINPUT \_ DEVSUBTYPE \_ Dance \_ Pad (sottotipo 5)        | Impostazione predefinita per qualsiasi nuovo sottotipo |
| XINPUT \_ DEVSUBTYPE \_ Guitar (sottotipo 6)            | Chitarra                      |
| XINPUT \_ DEVSUBTYPE \_ Guitar \_ alternate (sottotipo 7) |                             |
| XINPUT \_ DEVSUBTYPE \_ Drum \_ Kit (sottotipo 8)         |                             |
| XINPUT \_ DEVSUBTYPE \_ Guitar \_ Bass (sottotipo 11)     |                             |
| XINPUT \_ DEVSUBTYPE \_ Arcade \_ Pad (sottotipo 19)      |                             |

> [!Note]  
> I mapping HID seguenti sono statici. Ciò significa che anche se il report sulle funzionalità del dispositivo indica che un determinato pulsante o asse non è supportato, il mapping lo includerà, ma segnalerà sempre uno stato disattivato o un valore centrale.

## <a name="gamepad"></a>Game pad

Questo è il mapping predefinito ed è progettato per il gamepad standard di Xbox Common Controller e viene esposto come tipo di utilizzo HID del *Gamepad* .

| Control                      | Nome utilizzo HID | Pagina utilizzo | ID utilizzo   |
|------------------------------|----------------|------------|------------|
| Left Stick                   | X, Y           | 0x01       | 0x30, 0x31 |
| Right stick                  | RX, Ry         | 0x01       | 0x33, 0x34 |
| Trigger a sinistra + trigger destro | Z\*            | 0x01       | 0x32       |
| D-riempimento in alto, in basso, a sinistra, a destra  | Switch Hat     | 0x01       | 0x39       |
| A                            | Pulsante 1       | 0x09       | 0x01       |
| B                            | Pulsante 2       | 0x09       | 0x02       |
| X                            | Pulsante 3       | 0x09       | 0x03       |
| S                            | Pulsante 4       | 0x09       | 0x04       |
| LB (sinistra Bumper)             | Pulsante 5       | 0x09       | 0x05       |
| RB (Right Bumper)            | Pulsante 6       | 0x09       | 0x06       |
| INDIETRO                         | Pulsante 7       | 0x09       | 0x07       |
| START                        | Pulsante 8       | 0x09       | 0x08       |
| LSB (pulsante a sinistra)      | Pulsante 9       | 0x09       | 0x09       |
| RSB (pulsante destro)     | Pulsante 10      | 0x09       | 0x0A       |

> [!Note]  
> ( \* ): Questa combinazione viene eseguita in modo che la Z mostri il comportamento di centramento previsto dalla maggior parte dei titoli per la rotazione. Ciò significa che non è possibile visualizzare tutti i possibili valori di combinazione di trigger tramite [DIRECTINPUT](/previous-versions/windows/desktop/ee416842(v=vs.85)) e HID.

## <a name="arcade-stickarcade-pad"></a>Arcade stick/arcade Pad

Si tratta del mapping progettato per il controller di arcade stick ed è esposto come tipo di utilizzo HID del *Gamepad* . Il pad Arcade è molto simile a un bastone da Galleria, ma in un fattore di forma più piccolo. Queste progettazioni sostituiscono il trigger Left analogico e il trigger destro con i pulsanti digitali che segnalano il valore minimo e massimo dell'asse.

| Control                     | Nome utilizzo HID | Pagina utilizzo | ID utilizzo |
|-----------------------------|----------------|------------|----------|
| D-riempimento in alto, in basso, a sinistra, a destra | Switch Hat     | 0x01       | 0x39     |
| A                           | Pulsante 1       | 0x09       | 0x01     |
| B                           | Pulsante 2       | 0x09       | 0x02     |
| X                           | Pulsante 3       | 0x09       | 0x03     |
| S                           | Pulsante 4       | 0x09       | 0x04     |
| LB (sinistra Bumper)            | Pulsante 5       | 0x09       | 0x05     |
| RB (Right Bumper)           | Pulsante 6       | 0x09       | 0x06     |
| INDIETRO                        | Pulsante 7       | 0x09       | 0x07     |
| START                       | Pulsante 8       | 0x09       | 0x08     |
| Trigger a sinistra                | Pulsante 9       | 0x09       | 0x09     |
| Trigger a destra               | Pulsante 10      | 0x09       | 0x0A     |

Questi dispositivi possono o meno supportare controlli aggiuntivi, ma non sono esposti dal mapping HID: Left Stick, right stick, LSB (Left Stick Button) e RSB (right stick Button).

## <a name="wheel"></a>Selettore circolare

Questo mapping è progettato per la ruota Xbox Racing ed è esposto come tipo di utilizzo HID del *Gamepad* .

| Control                                                        | Nome utilizzo HID | Pagina utilizzo | ID utilizzo |
|----------------------------------------------------------------|----------------|------------|----------|
| Wheel (Left Stick X)                                           | X              | 0x01       | 0x30     |
| Acceleratore (trigger a destra) + pedale freno (trigger a sinistra) | Z\*            | 0x01       | 0x32     |
| D-riempimento in alto, in basso, a sinistra, a destra                                    | Switch Hat     | 0x01       | 0x39     |
| A                                                              | Pulsante 1       | 0x09       | 0x01     |
| B                                                              | Pulsante 2       | 0x09       | 0x02     |
| X                                                              | Pulsante 3       | 0x09       | 0x03     |
| S                                                              | Pulsante 4       | 0x09       | 0x04     |
| LB (sinistra Bumper)                                               | Pulsante 5       | 0x09       | 0x05     |
| RB (Right Bumper)                                              | Pulsante 6       | 0x09       | 0x06     |
| LSB (pulsante a sinistra)                                        | Pulsante 7       | 0x09       | 0x07     |
| RSB (pulsante destro)                                       | Pulsante 8       | 0x09       | 0x08     |
| INDIETRO                                                           | Pulsante 9       | 0x09       | 0x09     |
| START                                                          | Pulsante 10      | 0x09       | 0x0A     |

> [!Note]  
> ( \* ): Questa combinazione viene eseguita in modo che Z mostri il comportamento di centramento previsto dalla maggior parte dei titoli per i controlli freno e acceleratore. Ciò significa che non è possibile visualizzare tutti i possibili valori di combinazione di pedali tramite [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)).

## <a name="flight-stick"></a>Volo

Questo mapping è progettato per l'uso di Xbox Flight Stick ed è esposto come tipo di utilizzo *joystick* nascosto.

| Control                     | Nome utilizzo | Pagina utilizzo | ID utilizzo   |
|-----------------------------|------------|------------|------------|
| Flight Stick (Left Stick)   | X, Y       | 0x01       | 0x30, 0x31 |
| POV hat (right stick)       | RX, Ry     | 0x01       | 0x33, 0x34 |
| Limitazione (trigger a destra)    | Z          | 0x01       | 0x32       |
| Timone (trigger a sinistra)       | Rz         | 0x01       | 0x35       |
| D-riempimento in alto, in basso, a sinistra, a destra | Switch Hat | 0x01       | 0x39       |
| Weapon principale (A)          | Pulsante 1   | 0x09       | 0x01       |
| Arma secondaria (B)        | Pulsante 2   | 0x09       | 0x02       |
| X                           | Pulsante 3   | 0x09       | 0x03       |
| S                           | Pulsante 4   | 0x09       | 0x04       |
| LB (sinistra Bumper)            | Pulsante 5   | 0x09       | 0x05       |
| RB (Right Bumper)           | Pulsante 6   | 0x09       | 0x06       |
| INDIETRO                        | Pulsante 7   | 0x09       | 0x07       |
| START                       | Pulsante 8   | 0x09       | 0x08       |
| LSB (pulsante a sinistra)     | Pulsante 9   | 0x09       | 0x09       |
| RSB (pulsante destro)    | Pulsante 10  | 0x09       | 0x0A       |

> [!Note]  
> Questa operazione si basa sulla progettazione di Flight Stick finale. Poiché questo comportamento è diverso dalle definizioni Early Flight Stick, molti dispositivi hanno un'opzione mode che supporta il vecchio modello rispetto a quello nuovo. Questo mapping presuppone il nuovo modello.