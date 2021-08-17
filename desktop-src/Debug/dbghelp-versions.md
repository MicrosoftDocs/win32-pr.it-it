---
description: La libreria DbgHelp viene implementata da DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Versioni di DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5adb00c6442f7ba36f5aeb86e0255e175131492124d08fbf865e57a9721a7893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343861"
---
# <a name="dbghelp-versions"></a>Versioni di DbgHelp

La libreria DbgHelp viene implementata da DbgHelp.dll. Anche se questa DLL è inclusa in tutte le versioni supportate di Windows, raramente è la versione più recente di DbgHelp disponibile. Inoltre, la versione di DbgHelp in Windows ha funzionalità ridotte rispetto alle altre versioni, in particolare non supporta il server di simboli e il server di origine.

Le versioni più recenti di DbgHelp.dll, SymSrv.dll e SrcSrv.dll sono disponibili come parte del pacchetto [Debugging Tools For Windows.](https://developer.microsoft.com/windows/downloads/windows-10-sdk) I criteri di ridistribuzione per queste DLL incluse sono stati appositamente progettati per semplificare il più possibile l'inclusione di questi file nei propri pacchetti e versioni.

> [!Caution]  
> Gli utenti non devono mai tentare di installare gli strumenti di debug per le versioni di [Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) di DbgHelp.dll nelle directory di sistema di Windows perché non sono testati in questo scenario e probabilmente destabilizzano il sistema. Sono disponibili versioni X64 e X86 separate del pacchetto di debug ed entrambe sono necessarie per gli utenti interessati a supportare entrambe le piattaforme.

Per ottenere la versione più recente di DbgHelp.dll, passare a [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) e scaricare Gli strumenti di debug per Windows. Per informazioni sull'installazione corretta, vedere Chiamata della [libreria DbgHelp.](calling-the-dbghelp-library.md)

> [!Note]  
> Il DbgHelp.dll file fornito in Windows non è ridistribuibile.

Molte versioni di DbgHelp includono funzionalità aggiuntive. Per assicurarsi che sia disponibile la versione corretta di DbgHelp per l'applicazione, vedere le informazioni sui requisiti nella documentazione di riferimento dell'API specifica.
