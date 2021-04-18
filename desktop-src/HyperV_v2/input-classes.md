---
description: I dispositivi di input utente sono rappresentati da queste classi. Una macchina virtuale ha sempre un'istanza di ogni classe associata.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Classi di input
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2955cadfb00dcc39fed490a9c706b12bb1a8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309508"
---
# <a name="input-classes"></a>Classi di input

I dispositivi di input utente sono rappresentati da queste classi. Una macchina virtuale ha sempre un'istanza di ogni classe associata. Questi dispositivi non possono essere aggiunti o rimossi dalla macchina virtuale. Pertanto, non sono presenti istanze del pool di risorse per i dispositivi della tastiera o del mouse.

I dispositivi della tastiera e del mouse sono collegati alla macchina virtuale tramite l'associazione [**\_ SystemDevice di MSVM**](msvm-systemdevice.md) . Una macchina virtuale contiene un dispositivo mouse PS2 e un mouse sintetico. Solo un dispositivo di puntamento è attivo alla volta.

Di seguito sono riportate le classi WMI di virtualizzazione correlate all'input.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                          | Descrizione                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [**\_Tastiera MSVM**](msvm-keyboard.md)<br/>             | Rappresenta un dispositivo da tastiera.<br/>        |
| [**\_Ps2Mouse MSVM**](msvm-ps2mouse.md)<br/>             | Rappresenta un dispositivo mouse PS2.<br/>       |
| [**\_SyntheticMouse MSVM**](msvm-syntheticmouse.md)<br/> | Rappresenta un dispositivo mouse sintetico.<br/> |



 

 

 




