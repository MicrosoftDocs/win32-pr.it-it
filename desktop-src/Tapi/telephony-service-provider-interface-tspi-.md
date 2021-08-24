---
description: Un provider di servizi di telefonia (TSPI) gestisce i controlli specifici del dispositivo per la programmazione delle comunicazioni.
ms.assetid: da54e219-9adb-4a12-baab-52f2b2fb7c66
title: TSPI (Telephony Service Provider Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fac57f3b86acdf105c4c78f46f4f1d1d0e270c2a0b1be2d8bd1f55009926329
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681801"
---
# <a name="telephony-service-provider-interface-tspi"></a>TSPI (Telephony Service Provider Interface)

Un provider di servizi di telefonia (TSPI) gestisce i controlli specifici del dispositivo per la programmazione delle comunicazioni. Un provider di servizi di telefonia deve essere conforme al provider di servizi di telefonia (TSPI) per funzionare come provider di servizi all'interno dell'ambiente di telefonia Microsoft. TSPI definisce le funzioni esterne esposte da un provider di servizi di telefonia fornito con apparecchiature di comunicazione.

Un autore TSP deve avere familiarità con il materiale in Panoramica della telefonia [Microsoft,](./microsoft-telephony-overview.md)che illustra l'architettura di telefonia generale e offre una panoramica del materiale comune a diverse API di telefonia. Questa sezione contiene ad esempio un elenco di operazioni di controllo sessione, ad esempio Park, con descrizioni di ogni operazione e passa agli elementi di programmazione TAPI 2.2, TAPI 3 e TSPI correlati.

Le panoramiche seguenti riguardano materiale specifico per le esigenze di un autore TSP. Si noti che le parti più difficili della scrittura di un TSP sono i dettagli specifici del dispositivo e del sistema operativo, che non sono nell'ambito di questo documento.

La panoramica di TSPI è suddivisa nelle sezioni seguenti:

-   [](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) Considerazioni generali sulla programmazione riguardano i requisiti delle DLL, la corretta gestione delle versioni, i controlli degli errori eseguiti da TAPI, un riepilogo del modo in cui le funzioni TSPI corrispondono alle funzioni TAPI 2.2 (TAPI/C) e una descrizione dei livelli di servizio espressi in TSPI.
-   Il [ciclo di vita di un provider di servizi](life-cycle-of-a-telephony-service-provider.md) di telefonia contiene un riepilogo di alto livello delle fasi operative di un provider di servizi di telefonia.
-   [Accesso ai dispositivi](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) illustra le nozioni di base sul modo in cui un provider di servizi di configurazione del servizio TSP espone le informazioni e i controlli del dispositivo a TAPI.
-   [L'accesso](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) alla sessione illustra gli aspetti previsti da TAPI per un provider di servizi terminal durante una sessione di comunicazione.
-   [Accesso ai](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) supporti offre un set limitato di controlli sui flussi multimediali. Un controllo molto più fine è possibile tramite l'uso di un provider di servizi multimediali e gli autori di provider di servizi devono usare questa API ogni volta che è possibile. TSPI fornisce le comunicazioni tra una coppia TSP/MSP.
-   [Telefono dispositivi copre](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85)) le informazioni supplementari e le operazioni esposte se un provider di servizi tsp gestisce il controllo del set di telefoni. Queste operazioni sono facoltative.
-   [L'interfaccia DLL](the-telephony-service-provider-ui-dll-interface.md) dell'interfaccia utente del provider di servizi di telefonia copre funzioni speciali che possono essere implementate per consentire a un utente di impostare direttamente molti aspetti delle funzionalità di un provider di servizi di telefonia.

Per informazioni dettagliate [degli elementi di programmazione TSPI,](tspi-reference.md) vedere le informazioni di riferimento su TSPI.

 

 
