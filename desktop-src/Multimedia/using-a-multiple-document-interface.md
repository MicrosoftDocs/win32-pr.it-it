---
title: Uso di un'interfaccia a documenti multipli
description: Uso di un'interfaccia a documenti multipli
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- Funzione MCIWndRegisterClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b75d337c5375b66974161c1c983c1aeec5bed7805457186139771d879132b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941056"
---
# <a name="using-a-multiple-document-interface"></a>Uso di un'interfaccia a documenti multipli

Le applicazioni che usano un'interfaccia a documenti multipli (MDI) potrebbero dover specificare stili di finestra non disponibili tramite la [**funzione MCIWndCreate.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) Per queste applicazioni, è possibile registrare e creare una finestra MCIWnd usando la [**funzione MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) con la [funzione CreateWindowEx.](/windows/win32/api/winuser/nf-winuser-createwindowexa) La **funzione MCIWndRegisterClass** registra la classe finestra MCIWND WINDOW CLASS e quindi CreateWindowEx crea un'istanza di \_ una finestra \_ MCIWnd. 

 

 