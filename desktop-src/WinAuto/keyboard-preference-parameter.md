---
title: Parametro preferenza tastiera
description: Il parametro delle preferenze della tastiera indica che l'utente si basa sulla tastiera anziché sul mouse, pertanto le applicazioni devono visualizzare le interfacce della tastiera che altrimenti verrebbero nascoste.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c074078cdd548b6b3614213d6086edb3f5a6a412d84e418417dc0b4fcd2800e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998481"
---
# <a name="keyboard-preference-parameter"></a>Parametro preferenza tastiera

Il parametro delle preferenze della tastiera indica che l'utente si basa sulla tastiera anziché sul mouse, pertanto le applicazioni devono visualizzare le interfacce della tastiera che altrimenti verrebbero nascoste.

L'utente controlla l'impostazione del parametro delle preferenze della tastiera usando il Centro accessibilità in Pannello di controllo o un'altra applicazione per la personalizzazione dell'ambiente. Le applicazioni usano i flag **SPI \_ GETKEYBOARDPREF** e **SPI \_ SETKEYBOARDPREF** con la [**funzione SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro delle preferenze della tastiera.

Inoltre, in Windows 2000, gli utenti possono impostare un parametro che indica se i tasti di scelta dei menu sono sempre sottolineati. Le applicazioni usano i flag **SPI \_ GETMENUUNDERLINES** e **SPI \_ SETMENUUNDERLINES** con la [**funzione SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro di sottolineatura del menu.

Quando un'applicazione riceve un messaggio [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) per la preferenza della tastiera o il parametro di sottolineatura del menu, è consigliabile che l'applicazione chiami [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per aggiornare le informazioni per entrambi i parametri.

Si noti **che SPI \_ GETMENUUNDERLINES** è uguale a **SPI \_ GETKEYBOARDCUES** e **SPI \_ SETMENUUNDERLINES** è uguale a **SPI \_ SETKEYBOARDCUES**.

 

 