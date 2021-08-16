---
title: Piattaforma dei sensori
description: Windows 7 ha modificato il modo in cui gli sviluppatori usano i sensori.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7072a19ee0a746b0764850230a06de1ca72be8ca4633f1350165297f1ef4036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203891"
---
# <a name="sensor-platform"></a>Piattaforma dei sensori

Windows 7 ha modificato il modo in cui gli sviluppatori usano i sensori. Include il supporto nativo per i sensori, ampliato da una nuova piattaforma di sviluppo per l'uso dei sensori, inclusi i sensori di posizione, ad esempio i dispositivi GPS (Global Positioning Systems).

Le API di posizione di *Windows* sono una nuova funzionalità di Windows 7 che consente agli sviluppatori di applicazioni di accedere alle informazioni sulla posizione fisica dell'utente. Le *API Windows Location* possono astrarre l'hardware, supportare contemporaneamente più applicazioni e passare facilmente da una tecnologia all'altra, affidando allo sviluppatore dell'applicazione il carico di lavoro di gestione di questi vincoli. Le *API* location possono essere usate dai programmatori tramite il linguaggio di programmazione C++ (da programmatori che hanno familiarità con Component Object Model (COM)) o usando oggetti COM in linguaggi di scripting, ad esempio Microsoft JScript. Il supporto per gli script consente di accedere facilmente ai dati di posizione per progetti come i team.

Windows 7 offre una piattaforma solida e facile da usare per l'uso di dispositivi sensori, ad esempio un sensore di luce ambientale o un misuratore della temperatura, per creare consapevolezza ambientale nelle applicazioni Windows ambiente. I PC possono usare sensori incorporati nel computer, connessi tramite connessioni cablate o wireless o connessi tramite una rete o *Internet.*

Le *API Sensor* e *Location* offrono un modo standard per individuare i sensori e accedere a livello di codice ai dati forniti dai sensori.

Il *pannello di* controllo Sensore consente agli utenti di abilitare o disabilitare i sensori, controllare l'accesso ai sensori che potrebbero esporre dati sensibili, visualizzare le proprietà dei sensori e modificare le descrizioni dei sensori.

[L'estensione Sensor Class è](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) una parte fondamentale del modello di sviluppo del driver per la piattaforma Sensor. Fornisce i meccanismi seguenti, usati durante la scrittura di un driver del sensore [UMDF (User-Mode Driver Framework):](https://developer.microsoft.com/windows/hardware)

-   Integrazione con Sensor Platform
-   Applicazione della sicurezza

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API per sensori](../sensorsapi/portal.md)
</dt> <dt>