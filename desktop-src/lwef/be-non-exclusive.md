---
title: Non essere esclusivo
description: Non essere esclusivo
ms.assetid: 7a44840d-6bf9-4c12-ba14-66d7067a984d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b637bcf0860ccc4917b1af344664f9828b0da8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395643"
---
# <a name="be-non-exclusive"></a>Non essere esclusivo

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

I caratteri interattivi possono essere utilizzati nell'interfaccia utente come assistenti, guide, intrattenitori, cantastorie, agenti di vendita o in diversi altri ruoli. Un carattere che esegue o assiste automaticamente non deve essere progettato in modo contrario al principio di progettazione per mantenere il controllo dell'utente. Quando si aggiunge un carattere all'interfaccia di un sito Web o di un'applicazione convenzionale, utilizzare il carattere come miglioramento, anziché come sostituzione di, l'interfaccia principale. Evitare di implementare funzionalità o operazioni che richiedono esclusivamente un carattere.

Allo stesso modo, consentire all'utente di scegliere quando si desidera interagire con il carattere. Un utente dovrebbe essere in grado di chiudere il carattere e restituire solo con l'autorizzazione dell'utente. La forzatura dell'interazione tra caratteri sugli utenti può avere un effetto negativo grave. Per supportare il controllo utente dell'interazione dei caratteri, Microsoft Agent include automaticamente i comandi Nascondi e Mostra. L'API di Microsoft Agent supporta inoltre questi metodi, pertanto è possibile includere il supporto per queste funzioni nella propria interfaccia. Inoltre, l'interfaccia utente dell'agente Microsoft include proprietà globali che consentono all'utente di eseguire l'override di determinate opzioni di output dei caratteri. Per assicurarsi che le preferenze dell'utente siano gestite, non è possibile eseguire l'override di queste proprietà tramite l'API.

 

 




