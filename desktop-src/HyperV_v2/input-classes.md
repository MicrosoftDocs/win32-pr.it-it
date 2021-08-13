---
description: I dispositivi di input dell'utente sono rappresentati da queste classi. A una macchina virtuale è sempre associata un'istanza di ogni classe.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Classi di input
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5df9c5a2f1d2743e062cf685dc6fd849f33333808315459560dfd840e925135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644863"
---
# <a name="input-classes"></a>Classi di input

I dispositivi di input dell'utente sono rappresentati da queste classi. A una macchina virtuale è sempre associata un'istanza di ogni classe. Questi dispositivi non possono essere aggiunti o rimossi dalla macchina virtuale. Pertanto, non sono presenti istanze del pool di risorse per i dispositivi tastiera o mouse.

I dispositivi da tastiera e mouse sono collegati alla macchina virtuale tramite [**l'associazione \_ Msvm SystemDevice.**](msvm-systemdevice.md) Una macchina virtuale contiene sia un DISPOSITIVO PS2 che un dispositivo mouse sintetico. È attivo un solo dispositivo di puntamento alla volta.

Di seguito sono riportate le classi WMI di virtualizzazione correlate all'input.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                          | Descrizione                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [**Tastiera \_ Msvm**](msvm-keyboard.md)<br/>             | Rappresenta un dispositivo tastiera.<br/>        |
| [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)<br/>             | Rappresenta un dispositivo mouse PS2.<br/>       |
| [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md)<br/> | Rappresenta un dispositivo mouse sintetico.<br/> |



 

 

 




