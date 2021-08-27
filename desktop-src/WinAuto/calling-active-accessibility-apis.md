---
title: Chiamata Active Accessibility API
description: Microsoft Active Accessibility fornisce API (Application Programming Interface) per client e server.
ms.assetid: c40441d2-7294-4c76-8b42-08ed66eccb7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a54bc297af42546a081c3478ef109be137d8af19a37ea39415e8b0d2c06ccc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122241"
---
# <a name="calling-active-accessibility-apis"></a>Chiamata Active Accessibility API

Microsoft Active Accessibility fornisce API (Application Programming Interface) per client e server. La maggior parte sono implementate nella libreria Microsoft Active Accessibility a collegamento dinamico, Oleacc.dll, ma [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)e [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) vengono implementate in user32.dll, che è un componente principale del sistema operativo Microsoft Windows.

Nei computer che eseguono Windows 95 o Microsoft Windows NT 4.0 non sono installati Oleacc.dll e la versione corretta di user32.dll perché Microsoft Active Accessibility è stato incorporato in fasi nelle versioni successive di Windows. Di conseguenza, le applicazioni eseguite su queste piattaforme si collegano in modo esplicito Oleacc.dll in fase di esecuzione usando la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) invece di basarsi sulle librerie di importazione. Active Accessibility 1.3 supporta Windows 95 e Microsoft Windows NT 4.0. Le versioni precedenti Windows non sono supportate da Microsoft Active Accessibility.

Le applicazioni server usano [**la funzione GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per recuperare l'indirizzo di una funzione Microsoft Active Accessibility e quindi eseguire la chiamata tramite un puntatore a funzione. Se si chiama una funzione implementata in Oleacc.dll, le applicazioni server usano l'handle restituito da [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) nella chiamata a **GetProcAddress**. Se si chiama una funzione definita in user32.dll, le applicazioni server chiamano [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) specificando "USER32" e usano l'handle del modulo restituito nella chiamata a **GetProcAddress**.

Ad esempio, se un'applicazione usa [**NotifyWinEvent,**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)chiama [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) usando l'handle del modulo user32.dll per ottenere l'indirizzo della funzione. Se la chiamata ha esito positivo (ovvero questa versione di Windows supporta Microsoft Active Accessibility), l'applicazione imposta un flag che indica che è sicuro chiamare **NotifyWinEvent**. L'indirizzo ricevuto da **GetProcAddress** viene archiviato in una variabile puntatore a funzione e usato in tutto il codice.

 

 