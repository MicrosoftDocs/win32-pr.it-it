---
title: Panoramica dell'interfaccia di programmazione di Microsoft Agent
description: Panoramica dell'interfaccia di programmazione di Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4dc087064afb0e3beaaf97d987e496239d3fd378461acaf5601927ac6d929
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887921"
---
# <a name="microsoft-agent-programming-interface-overview"></a>Panoramica dell'interfaccia di programmazione di Microsoft Agent

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

L'API di Microsoft Agent offre servizi che supportano la visualizzazione e l'animazione di caratteri animati. Implementato come server di automazione OLE (Component Object Model COM), Microsoft Agent consente a più applicazioni, denominate client o applicazioni client, di ospitare e accedere contemporaneamente ai relativi servizi di \[ \] animazione, input e output. Un client può essere qualsiasi applicazione che si connette alle interfacce COM di Microsoft Agent.

Come server COM, Microsoft Agent viene avviato automaticamente solo quando un'applicazione client usa le interfacce COM e le richieste per connettersi a esso. Rimane in esecuzione fino a quando tutti i client non chiudono le connessioni. Quando non rimane alcun client connesso, Microsoft Agent viene chiuso automaticamente.

Sebbene sia possibile chiamare direttamente le interfacce COM di Microsoft Agent, Microsoft Agent include anche un ActiveX Microsoft. Questo controllo semplifica l'accesso ai servizi di Microsoft Agent da linguaggi di programmazione che supportano l'ActiveX di controllo.

Oltre a supportare programmi autonomi scritti per Windows, è possibile creare script per Agent per supportare le pagine Web, a condizione che il browser supporti l'ActiveX predefinita. Microsoft Internet Explorer include il supporto per ActiveX nonché linguaggi di scripting che è possibile usare per programmare Agent. Se non si usa Internet Explorer, rivolgersi al fornitore o al fornitore per informazioni sul supporto del browser per ActiveX.

Le informazioni seguenti forniscono una breve panoramica delle interfacce di programmazione per il software Microsoft Agent.

-   [Servizi di animazione](animation-services.md)
-   [Servizi di input](input-services.md)
-   [Finestra Comandi vocali](the-voice-commands-window.md)
-   [Servizi di output](output-services.md)

 

 




