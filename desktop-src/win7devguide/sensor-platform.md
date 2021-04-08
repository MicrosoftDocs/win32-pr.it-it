---
title: Piattaforma sensore
description: Windows 7 ha modificato il modo in cui gli sviluppatori usano i sensori.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046981"
---
# <a name="sensor-platform"></a>Piattaforma sensore

Windows 7 ha modificato il modo in cui gli sviluppatori usano i sensori. Include il supporto nativo per i sensori, espanso da una nuova piattaforma di sviluppo per l'uso dei sensori, inclusi i sensori di posizione, ad esempio i dispositivi GPS (Global Positioning System).

Basati sulla piattaforma dei sensori, le API di *Windows location* sono una nuova funzionalità di Windows 7 che consente agli sviluppatori di applicazioni di accedere alle informazioni sulla posizione fisica dell'utente. Le API di *Windows location* possono astrarre hardware, supportare contemporaneamente più applicazioni e passare facilmente da una tecnologia all'altra, evitando allo sviluppatore di applicazioni di gestire tali vincoli. Le API *location* possono essere utilizzate dai programmatori tramite il linguaggio di programmazione C++ (da parte dei programmatori che hanno familiarità con Component Object Model (com)) o utilizzando oggetti com in linguaggi di scripting, ad esempio Microsoft JScript. Il supporto per gli script consente di accedere facilmente ai dati di posizione per progetti quali i gadget.

Windows 7 offre una piattaforma solida e facile da usare per l'uso di dispositivi di sensori, ad esempio un sensore di luce di ambiente o un misuratore di temperatura, per creare la consapevolezza ambientale nelle applicazioni Windows. I PC possono usare i sensori incorporati nel computer, connessi tramite connessioni cablate o wireless o connessi tramite una rete o *Internet*.

Le API sensori e *località* forniscono un modo standard per *individuare i sensori* e accedere a livello di codice ai dati forniti dai sensori.

Il pannello di controllo del *sensore* consente agli utenti di abilitare o disabilitare i sensori, controllare l'accesso ai sensori che potrebbero esporre dati sensibili, visualizzare le proprietà dei sensori e modificare le descrizioni dei sensori.

L' [estensione della classe Sensor](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) è una parte essenziale del modello di sviluppo di driver per la piattaforma di sensori. Fornisce i meccanismi seguenti, che vengono utilizzati durante la scrittura di un driver del sensore [UMDF (User-Mode Driver Framework)](https://developer.microsoft.com/windows/hardware) :

-   Integrazione con la piattaforma dei sensori
-   Imposizione della sicurezza

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API per sensori](../sensorsapi/portal.md)
</dt> <dt>