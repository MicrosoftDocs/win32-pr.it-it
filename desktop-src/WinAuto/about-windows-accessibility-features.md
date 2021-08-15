---
title: Funzionalità di accessibilità di Windows
description: "Windows L'accessibilità supporta due categorie di funzionalità per Windows sviluppatori: API Win32 e Impostazioni."
ms.assetid: 823bbc5b-062b-43ef-9f3e-822dc6f55c5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac63f4bf021888ee96cb180e423f55b07190959ad8c8b7966f1a4a7ae395119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994421"
---
# <a name="windows-accessibility-features"></a>Funzionalità di accessibilità di Windows

Windows L'accessibilità supporta due categorie di funzionalità per aiutare gli sviluppatori Windows a progettare applicazioni accessibili, gli sviluppatori di assistive technology creano strumenti come utilità per la lettura dello schermo e le lente di ingrandimento e i tecnici dei test software creano script automatizzati per il test Windows applicazioni.

## <a name="settings"></a>Impostazioni

Esistono due tipi di impostazioni disponibili per gli utenti (tramite il Centro accessibilità in Pannello di controllo) che vengono esposti anche agli sviluppatori:

- [Parametri di accessibilità](accessibility-parameters.md). Se impostati, questi parametri indicano che le applicazioni devono modificare il comportamento predefinito. Le applicazioni possono controllare lo stato di un parametro di accessibilità per determinare se l'utente desidera un comportamento speciale che possa essere fornito in modo specifico dell'applicazione. Ad esempio, il parametro ShowSounds indica che anche un'applicazione che usa il suono per trasmettere informazioni importanti deve fornire visivamente le informazioni.
- [Funzionalità di accessibilità incorporate.](built-in-accessibility-features.md) Queste funzionalità sono integrate nel sistema o fornite come estensione del sistema. Influiscono sul modo in cui l'utente fornisce input da tastiera e mouse al computer. Se abilitata, la funzionalità è disponibile indipendentemente dalle applicazioni in esecuzione. Un esempio è un filtro da tastiera che rende più semplice per gli utenti con problemi di spostamento digitare combinazioni di tasti, ad esempio CTRL+ALT+CANC.

Ogni parametro di accessibilità e ogni funzionalità di accessibilità incorporata corrisponde a un parametro di sistema che può essere impostato o sottoposto a query con la [funzione SystemParametersInfo.](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)

## <a name="win32-apis"></a>API Win32

Le API Win32 offrono funzionalità di accessibilità e automazione che consentono agli sviluppatori di creare applicazioni e framework dell'interfaccia utente, fornitori di assistive technology di creare strumenti, tester che garantiscono implementazioni di qualità e utenti con disabilità usano i propri computer e dispositivi.

## <a name="related-topics"></a>Argomenti correlati

[Considerazioni sulla sicurezza per Assistive Technologies](uiauto-securityoverview.md)