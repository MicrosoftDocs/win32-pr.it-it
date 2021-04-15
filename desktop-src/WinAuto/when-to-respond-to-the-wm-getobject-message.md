---
title: Quando rispondere al messaggio di WM_GETOBJECT
description: Se un'applicazione supporta Microsoft Active Accessibility o l'automazione dell'interfaccia utente per un elemento dell'interfaccia utente, l'applicazione non deve rispondere al \_ messaggio WM GetObject prima che l'oggetto che rappresenta l'elemento dell'interfaccia utente sia completamente inizializzato o dopo che l'applicazione è iniziata a chiudersi.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cfa8d6604a13e84ffa89bf1fcf93d5d13e66e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473950"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a>Quando rispondere al \_ messaggio WM GETobject

Se un'applicazione supporta Microsoft Active Accessibility o l'automazione dell'interfaccia utente per un elemento dell'interfaccia utente, l'applicazione non deve rispondere al messaggio [**WM \_ GetObject**](wm-getobject.md) prima che l'oggetto che rappresenta l'elemento dell'interfaccia utente sia completamente inizializzato o dopo che l'applicazione è iniziata a chiudersi. Quando un'applicazione crea una nuova finestra, il sistema genera l' [**\_ oggetto evento \_ create**](event-constants.md) WinEvent per notificare ai client prima di inviare il messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) alla routine della finestra dell'applicazione. Poiché molte applicazioni usano **WM \_ create** per avviare il processo di inizializzazione, qualsiasi implementazione di accessibilità di un elemento dell'interfaccia utente non risponde al messaggio [**WM \_ GetObject**](wm-getobject.md) fino al termine dell'elaborazione del messaggio **WM \_ create** .

 

 