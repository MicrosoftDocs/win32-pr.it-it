---
title: Chiamata di API Active Accessibility
description: Microsoft Active Accessibility fornisce API (Application Programming Interface) per client e server.
ms.assetid: c40441d2-7294-4c76-8b42-08ed66eccb7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a239495fddbcaf2275f095abc889295568b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046887"
---
# <a name="calling-active-accessibility-apis"></a>Chiamata di API Active Accessibility

Microsoft Active Accessibility fornisce API (Application Programming Interface) per client e server. La maggior parte è implementata nella libreria a collegamento dinamico Microsoft Active Accessibility, Oleacc.dll, mentre [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)e [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) sono implementate in user32.dll, che è un componente principale del sistema operativo Microsoft Windows.

I computer che eseguono Windows 95 o Microsoft Windows NT 4,0 non hanno Oleacc.dll e la versione corretta di user32.dll installata perché Microsoft Active Accessibility è stata incorporata in fasi nelle versioni successive di Windows. Di conseguenza, le applicazioni eseguite su queste piattaforme si collegano in modo esplicito a Oleacc.dll in fase di esecuzione utilizzando la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) anziché basarsi sulle librerie di importazione. Active Accessibility 1,3 supporta Windows 95 e Microsoft Windows NT 4,0. Le versioni precedenti di Windows non sono supportate da Microsoft Active Accessibility.

Le applicazioni server utilizzano la funzione [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per recuperare l'indirizzo di una funzione di Microsoft Active Accessibility e quindi effettuare la chiamata tramite un puntatore a funzione. Se si chiama una funzione implementata in Oleacc.dll, le applicazioni server utilizzano l'handle restituito da [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) nella chiamata a **GetProcAddress**. Se si chiama una funzione definita in user32.dll, le applicazioni server chiamano [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) specificando "user32" e utilizzano l'handle del modulo restituito nella chiamata a **GetProcAddress**.

Se, ad esempio, un'applicazione usa [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), chiama [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) usando l'handle del modulo di user32.dll per ottenere l'indirizzo della funzione. Se la chiamata ha esito positivo (vale a dire che questa versione di Windows supporta Microsoft Active Accessibility), l'applicazione imposta un flag che indica che è sicuro chiamare **NotifyWinEvent**. L'indirizzo ricevuto da **GetProcAddress** viene archiviato in una variabile puntatore a funzione e usato in tutto il codice.

 

 