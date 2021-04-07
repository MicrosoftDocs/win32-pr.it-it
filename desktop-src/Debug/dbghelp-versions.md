---
description: La libreria DbgHelp viene implementata da DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Versioni di DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811e92ba88bf38cb46274e2d2c716a620ea83b16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747743"
---
# <a name="dbghelp-versions"></a>Versioni di DbgHelp

La libreria DbgHelp viene implementata da DbgHelp.dll. Anche se questa DLL è inclusa in tutte le versioni supportate di Windows, raramente è la versione più recente di DbgHelp disponibile. Inoltre, la versione di DbgHelp fornita in Windows ha ridotto le funzionalità delle altre versioni, in particolare, manca il supporto per il server di simboli e il server di origine.

Le versioni più aggiornate di DbgHelp.dll, SymSrv.dll e SrcSrv.dll sono disponibili come parte del pacchetto strumenti di [debug per Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) . I criteri di ridistribuzione per queste DLL incluse sono stati progettati in modo specifico per semplificare il più possibile l'inclusione di questi file nei pacchetti e nelle versioni.

> [!Caution]  
> Gli utenti non devono mai tentare di installare gli [strumenti di debug per](https://developer.microsoft.com/windows/downloads/windows-10-sdk) le versioni di windows di DbgHelp.dll nelle directory di sistema di Windows perché non sono testati in questo scenario ed è probabile che destabilizzano il sistema. Sono disponibili versioni x64 e x86 separate del pacchetto di debug ed entrambe sono necessarie per gli utenti interessati a supportare entrambe le piattaforme.

Per ottenere la versione più recente di DbgHelp.dll, vedere [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) e scaricare gli strumenti di debug per Windows. Per informazioni sull'installazione corretta, vedere la pagina relativa alla [chiamata alla libreria DbgHelp](calling-the-dbghelp-library.md) .

> [!Note]  
> Il file di DbgHelp.dll fornito in Windows non è ridistribuibile.

Molte versioni di DbgHelp includono funzionalità aggiuntive. Per assicurarsi che sia disponibile la versione corretta di DbgHelp per l'applicazione, esaminare le informazioni sui requisiti nella documentazione di riferimento per l'API specifica.
