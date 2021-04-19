---
description: Un provider di servizi di telefonia (TSPI) gestisce i controlli specifici del dispositivo per la programmazione delle comunicazioni.
ms.assetid: da54e219-9adb-4a12-baab-52f2b2fb7c66
title: Interfaccia del provider di servizi di telefonia (TSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a9d8ac4fd15fbc2685073e5954e14951f33acd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317634"
---
# <a name="telephony-service-provider-interface-tspi"></a>Interfaccia del provider di servizi di telefonia (TSPI)

Un provider di servizi di telefonia (TSPI) gestisce i controlli specifici del dispositivo per la programmazione delle comunicazioni. Un TSP deve essere conforme al provider di servizi di telefonia (TSPI) per fungere da provider di servizi nell'ambiente di telefonia Microsoft. TSPI definisce le funzioni esterne esposte da un provider di servizi di telefonia fornito con apparecchiature per le comunicazioni.

Un autore di un TSP deve avere familiarità con il materiale nella [Panoramica della telefonia Microsoft](./microsoft-telephony-overview.md), che illustra l'architettura di telefonia generale e offre una panoramica del materiale comune a diverse API di telefonia. Ad esempio, in questa sezione è contenuto un elenco di operazioni di controllo della sessione, ad esempio Park, con le descrizioni di ogni operazione e vengono saltati gli elementi di programmazione TAPI 2,2, TAPI 3 e TSPI correlati.

Di seguito vengono descritti i materiali specifici delle esigenze di un autore di un TSP. Si noti che le parti più complesse della scrittura di un TSP sono i dettagli specifici del sistema operativo e del dispositivo che esulano dall'ambito di questo documento.

La Panoramica di TSPI è divisa nelle sezioni seguenti:

-   [Considerazioni generali sulla programmazione](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) riguarda i requisiti della dll, la gestione corretta delle versioni, i controlli degli errori eseguiti da TAPI, un riepilogo del modo in cui le funzioni TSPI corrispondono alle funzioni TAPI 2,2 (TAPI/C) e una discussione dei livelli di servizio come espresso in TSPI.
-   Il [ciclo di vita di un provider di servizi di telefonia](life-cycle-of-a-telephony-service-provider.md) contiene un riepilogo generale delle fasi operative di un tsp.
-   L' [accesso ai dispositivi](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) illustra le nozioni di base sul modo in cui un TSP espone informazioni sul dispositivo e controlli a TAPI.
-   [L'accesso alla sessione](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) riguarda ciò che TAPI prevede un TSP durante una sessione di comunicazione.
-   [L'accesso ai file multimediali](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) fornisce un set limitato di controlli sui flussi multimediali. Un controllo molto più preciso è possibile tramite l'uso di un provider di servizi multimediali e gli autori del provider di servizi devono usare questa API ogni volta che è possibile. TSPI fornisce le comunicazioni tra una coppia TSP/MSP.
-   [Dispositivi telefonici](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85)) copre le informazioni aggiuntive e le operazioni esposte se un TSP gestisce il controllo set telefonico. Queste operazioni sono facoltative.
-   [L'interfaccia dll dell'interfaccia utente del provider di servizi di telefonia](the-telephony-service-provider-ui-dll-interface.md) copre funzioni speciali che possono essere implementate per consentire a un utente di impostare direttamente molti aspetti della funzionalità di un tsp.

Per informazioni dettagliate sugli elementi di programmazione TSPI, vedere la Guida di [riferimento a TSPI](tspi-reference.md) .

 

 
