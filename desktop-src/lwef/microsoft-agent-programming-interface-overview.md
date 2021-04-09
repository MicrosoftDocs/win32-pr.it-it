---
title: Panoramica dell'interfaccia di programmazione Microsoft Agent
description: Panoramica dell'interfaccia di programmazione Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856214"
---
# <a name="microsoft-agent-programming-interface-overview"></a>Panoramica dell'interfaccia di programmazione Microsoft Agent

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

L'API dell'agente Microsoft fornisce servizi che supportano la visualizzazione e l'animazione dei caratteri animati. Implementato come server di automazione OLE (Component Object Model \[ com \] ), Microsoft Agent consente a più applicazioni, denominate client o applicazioni client, di ospitare e accedere ai servizi di animazione, input e output allo stesso tempo. Un client può essere qualsiasi applicazione che si connette alle interfacce COM di Microsoft Agent.

In quanto server COM, Microsoft Agent viene avviato automaticamente solo quando un'applicazione client usa le interfacce COM e le richieste per la connessione. Rimane in esecuzione fino a quando tutti i client non chiudono le connessioni. Quando non viene mantenuto alcun client connesso, l'agente Microsoft viene chiuso automaticamente.

Sebbene sia possibile chiamare direttamente le interfacce COM di Microsoft Agent, Microsoft Agent include anche un controllo Microsoft ActiveX. Questo controllo consente di accedere facilmente ai servizi di Microsoft Agent dai linguaggi di programmazione che supportano l'interfaccia di controllo ActiveX.

Oltre a supportare i programmi autonomi scritti per Windows, è possibile creare script per Agent per supportare pagine Web, purché il browser supporti l'interfaccia ActiveX. Microsoft Internet Explorer include il supporto per ActiveX e per i linguaggi di scripting che è possibile utilizzare per programmare Agent. Se non si usa Internet Explorer, consultare il fornitore o il fornitore per informazioni sul supporto del browser per ActiveX.

Le informazioni seguenti forniscono una breve panoramica delle interfacce di programmazione per il software dell'agente Microsoft.

-   [Servizi di animazione](animation-services.md)
-   [Servizi di input](input-services.md)
-   [Finestra comandi vocali](the-voice-commands-window.md)
-   [Servizi di output](output-services.md)

 

 




