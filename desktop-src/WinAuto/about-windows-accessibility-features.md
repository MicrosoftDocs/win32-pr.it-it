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

Windows L'accessibilità supporta due categorie di funzionalità che consentono agli sviluppatori Windows di progettare applicazioni accessibili, gli sviluppatori assistive technology creano strumenti come utilità per la lettura dello schermo e le lente di ingrandimento e i tecnici di test software creano script automatizzati per il test Windows applicazioni.

## <a name="settings"></a>Impostazioni

Esistono due tipi di impostazioni disponibili per gli utenti (tramite l'Centro accessibilità in Pannello di controllo) che vengono esposte anche agli sviluppatori:

- [Parametri di accessibilità](accessibility-parameters.md). Se impostati, questi parametri indicano che le applicazioni devono modificare il comportamento predefinito. Le applicazioni possono controllare lo stato di un parametro di accessibilità per determinare se l'utente desidera un comportamento speciale che può essere fornito in modo specifico dell'applicazione. Ad esempio, il parametro ShowSounds indica che anche un'applicazione che in genere usa il suono per trasmettere informazioni importanti deve fornire le informazioni visivamente.
- [Funzionalità di accessibilità incorporate.](built-in-accessibility-features.md) Queste funzionalità sono integrate nel sistema o fornite come estensione al sistema. Influiscono sul modo in cui l'utente fornisce input da tastiera e mouse al computer. Se abilitata, la relativa funzionalità è disponibile indipendentemente dalle applicazioni in esecuzione. Un esempio è un filtro da tastiera che semplifica la digitazione di combinazioni di tasti per gli utenti con problemi di spostamento, ad esempio CTRL+ALT+CANC.

Ogni parametro di accessibilità e ogni funzionalità di accessibilità incorporata corrisponde a un parametro di sistema che può essere impostato o sottoposto a query con la [funzione SystemParametersInfo.](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)

## <a name="win32-apis"></a>API Win32

Le API Win32 offrono funzionalità di accessibilità e automazione che consentono agli sviluppatori di creare applicazioni e framework dell'interfaccia utente, i fornitori di assistive technology compilano strumenti, i tester garantiscono implementazioni di qualità e gli utenti con disabilità usano i propri computer e dispositivi.

## <a name="related-topics"></a>Argomenti correlati

[Considerazioni sulla sicurezza per assistive Technologies](uiauto-securityoverview.md)