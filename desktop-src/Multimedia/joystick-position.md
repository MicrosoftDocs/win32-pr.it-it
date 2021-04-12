---
title: Posizione del joystick
description: Posizione del joystick
ms.assetid: db0d1125-e39f-445b-bd65-373633cad578
keywords:
- joystick, posizione
- joystick, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcdc187cfba244bb2b8c28c37e3677593f99870
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223791"
---
# <a name="joystick-position"></a>Posizione del joystick

È possibile eseguire una query su un joystick per ottenere informazioni sulla posizione e sul pulsante usando la funzione [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Ad esempio, un'applicazione può eseguire una query sul joystick per i valori di posizione della linea di base. La finestra delle proprietà del pannello di controllo del joystick usa questa tecnica quando si calibra il joystick.

È anche possibile eseguire query su un joystick o su un altro dispositivo con funzionalità estese usando la funzione [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

 

 