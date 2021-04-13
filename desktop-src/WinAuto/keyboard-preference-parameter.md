---
title: Parametro preferenza tastiera
description: Il parametro preferenza tastiera indica che l'utente si basa sulla tastiera anziché sul mouse, quindi le applicazioni devono visualizzare le interfacce della tastiera che altrimenti sarebbero nascoste.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399271"
---
# <a name="keyboard-preference-parameter"></a>Parametro preferenza tastiera

Il parametro preferenza tastiera indica che l'utente si basa sulla tastiera anziché sul mouse, quindi le applicazioni devono visualizzare le interfacce della tastiera che altrimenti sarebbero nascoste.

L'utente controlla l'impostazione del parametro preferenza tastiera usando il centro di accesso facilitato nel pannello di controllo o un'altra applicazione per la personalizzazione dell'ambiente. Le applicazioni usano i flag **SPI \_ GETKEYBOARDPREF** e **SPI \_ SETKEYBOARDPREF** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro di preferenza della tastiera.

Inoltre, in Windows 2000, gli utenti possono impostare un parametro che indica se i tasti di scelta dei menu sono sempre sottolineati. Le applicazioni usano i flag **SPI \_ GETMENUUNDERLINES** e **SPI \_ SETMENUUNDERLINES** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro di sottolineatura menu.

Quando un'applicazione riceve un messaggio [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) per il parametro preferenza tastiera o sottolineatura menu, è consigliabile che l'applicazione chiami [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per aggiornare le informazioni per entrambi i parametri.

Si noti **che \_ SPI GETMENUUNDERLINES** è uguale a **SPI \_ GETKEYBOARDCUES** e **SPI \_ SETMENUUNDERLINES** è uguale a **SPI \_ SETKEYBOARDCUES**.

 

 