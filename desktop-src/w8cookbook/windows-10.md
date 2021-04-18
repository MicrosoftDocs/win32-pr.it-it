---
title: Windows 10
description: Questa guida di riferimento fornisce informazioni per gli sviluppatori sulle modifiche apportate alla piattaforma per i sistemi operativi Windows 10.
ms.assetid: bf8d7d10-bab6-4711-b65f-5393d906e47b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03fce627969573deb395fda356564a85a3573682
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399566"
---
# <a name="windows-10"></a>Windows 10

Questa guida di riferimento fornisce informazioni per gli sviluppatori sulle modifiche apportate alla piattaforma per i sistemi operativi Windows 10. Vengono inoltre fornite linee guida per verificare la compatibilità delle app esistenti e pianificate con la versione più recente del sistema operativo. Si presuppone che l'utente abbia familiarità con le versioni precedenti di Windows.

Il contenuto si applica a: Windows 10

Il Cookbook è destinato agli sviluppatori di terze parti di app e dispositivi progettati per l'uso nell'ambiente Microsoft Windows.

## <a name="introduction"></a>Introduzione

Windows 10 introduce le più recenti piattaforme di sviluppo software e tecnologia del sistema operativo per l'uso da parte di sviluppatori e aziende di app e driver a livello mondiale. Per migliorare ulteriormente la sicurezza, l'affidabilità, le prestazioni e l'esperienza utente di Windows, Microsoft ha introdotto numerose nuove funzionalità, ha migliorato le funzionalità esistenti e ne ha rimosse altre.

Anche se l'obiettivo di Windows 10 è mantenere la compatibilità con le app scritte per le versioni rilasciate in precedenza del sistema operativo Windows, alcune interruzioni di compatibilità sono inevitabili a causa di innovazioni, protezione rafforzata e maggiore affidabilità. In generale, la compatibilità della versione più recente del sistema operativo Windows con le app e i dispositivi esistenti è elevata.

Questo documento illustra come verificare che le app e i dispositivi siano compatibili con la versione più recente del sistema operativo e fornisce una panoramica dei problemi noti di incompatibilità delle app.

Si consiglia di consultare questi argomenti per informazioni su come ottimizzare le app e sfruttare i vantaggi offerti da questa versione più recente di Windows.

## <a name="contents"></a>Contenuto

-   [Modifiche principali apportate da Windows 7 per garantire la compatibilità](key-changes-since-windows-7-to-ensure-compatibility.md)
-   [Come è possibile garantire la compatibilità dell'ecosistema combinato](how-we-can-ensure-compatibility-of-the-combined-ecosystem.md)
    -   [Controllo della versione di Windows](windows-version-check.md)
    -   [API non documentate](undocumented-apis.md)
    -   [Sviluppare app UWP e desktop Bridge](/windows/desktop/w8cookbook/develop-universal-windows-platform-apps)
    -   [Le funzionalità moderne dell'app desktop sono interessate se non vengono eseguite in modalità finestra](modern-desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode.md)
    -   [Disponibilità dei driver grafici applicabili in Windows Update](availability-of-applicable-graphics-drivers-on-windows-update.md)
    -   [Migrazione di driver grafici a Windows 10](graphics-driver-migration-to-windows-10.md)
    -   [Driver Bluetooth](bluetooth-drivers.md)

## <a name="download-the-cookbook"></a>Scarica il Cookbook

Per un riferimento rapido a tutte queste informazioni e per informazioni su Windows As a Service, su come supportare le app in Windows e sulle strategie ottimizzate per il test dell'app, [scaricare il Cookbook per la compatibilità con Windows 10](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).

## <a name="see-also"></a>Vedere anche

-   [Windows As a Service](/windows/deployment/update/), per informazioni sui tipi di versione di Windows 10 e sul supporto delle app.
-   [Windows Insider](https://insider.windows.com/), per accedere alle build di anteprima, testare e fornire commenti e suggerimenti.
-   [Pronto per Windows 10](https://www.readyfor10.com/), per inviare le informazioni aziendali a una risorsa per i responsabili IT.

 

 