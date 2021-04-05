---
title: Funzionalità di accessibilità di Windows
description: 'Windows Accessibility supporta due categorie di funzionalità per gli sviluppatori Windows: le API Win32 e le impostazioni utente.'
ms.assetid: 823bbc5b-062b-43ef-9f3e-822dc6f55c5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabd92ed8594d711ae9b744dc7f4a2622e8cb3d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046971"
---
# <a name="windows-accessibility-features"></a>Funzionalità di accessibilità di Windows

L'accessibilità di Windows supporta due categorie di funzionalità che consentono agli sviluppatori di Windows di progettare applicazioni accessibili, gli sviluppatori di tecnologie per l'accesso facilitato compilano strumenti quali utilità per la lettura dello schermo e lente di ingrandimento e i tecnici di test software creano script automatici

## <a name="settings"></a>Impostazioni

Esistono due tipi di impostazioni disponibili per gli utenti (tramite il centro di accesso facilitato nel pannello di controllo) esposte anche agli sviluppatori:

- [Parametri di accessibilità](accessibility-parameters.md). Se impostati, questi parametri indicano che le applicazioni devono modificare il comportamento predefinito. Le applicazioni possono controllare lo stato di un parametro di accessibilità per determinare se l'utente vuole un comportamento speciale che può essere fornito in modo specifico dell'applicazione. Il parametro ShowSounds, ad esempio, indica che un'applicazione che in genere usa il suono per trasmettere informazioni importanti deve fornire anche le informazioni in modo visivo.
- [Funzionalità di accessibilità predefinite](built-in-accessibility-features.md). Queste funzionalità sono incorporate nel sistema o fornite come estensione del sistema. Che influiscono sul modo in cui l'utente fornisce l'input della tastiera e del mouse al computer. Se abilitata, la relativa funzionalità è disponibile indipendentemente dalle applicazioni in esecuzione. Un esempio è un filtro da tastiera che rende più semplice per gli utenti con problemi di spostamento rispetto alle combinazioni di tasti di tipo, ad esempio CTRL + ALT + CANC.

Ogni parametro di accessibilità e ogni funzionalità di accessibilità predefinita corrisponde a un parametro di sistema che può essere impostato o sottoposto a query con la funzione [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .

## <a name="win32-apis"></a>API Win32

Le API Win32 forniscono funzionalità di accessibilità e automazione per aiutare gli sviluppatori a creare applicazioni e Framework dell'interfaccia utente, i fornitori di tecnologie per l'accesso facilitato compilano strumenti, tester assicurano implementazioni qualitative e persone con disabilità usano computer e dispositivi.

## <a name="related-topics"></a>Argomenti correlati

[Considerazioni sulla sicurezza per le tecnologie per l'accesso facilitato](uiauto-securityoverview.md)