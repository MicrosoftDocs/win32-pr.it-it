---
description: Un provider di servizi ora viene implementato come DLL. Ogni DLL può supportare più provider di servizi ora. Ogni provider è responsabile della propria configurazione e della propria sincronizzazione.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Creazione di un provider di servizi ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58766bf0ed7339bf8c9bfd7abc7434ddc43165b7cbdd77bcfd5420947e743d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885764"
---
# <a name="creating-a-time-provider"></a>Creazione di un provider di servizi ora

Un provider di servizi ora viene implementato come DLL. Ogni DLL può supportare più provider di servizi ora. Ogni provider è responsabile della propria configurazione e della propria sincronizzazione.

I provider di servizi ora devono implementare le funzioni di callback seguenti:

-   [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

Dopo aver caricato la DLL del provider, il gestore del provider di servizi di riferimento ora chiama [**TimeProvOpen,**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)passando il nome del provider e i puntatori alle funzioni seguenti:

-   [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

Queste funzioni possono essere usate dal provider di servizi ora. Il provider di servizi ora usa [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) per restituire un handle del provider utilizzato dal gestore del provider di servizi ora durante l'invio di comandi al provider di servizi ora. Il valore dell'handle viene definito dal provider di servizi ora e viene utilizzato principalmente per distinguere tra provider diversi implementati nella stessa DLL. Il provider di servizi ora può registrare eventi significativi [**usando LogTimeProvEventFunc.**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

Il gestore del provider di servizi ora [**usa TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) per inviare comandi al provider di servizi ora. Quando il provider di servizi ora deve notificare al gestore del provider di servizi ora che sono disponibili esempi di tempo, chiama [**AlertSamplesAvailFunc.**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc) Il gestore del provider di servizi di riferimento ora chiama **quindi TimeProvCommand** con il comando \_ TPC GetSamples per recuperare i campioni di ora. La richiesta dell'esempio da parte del gestore del provider di servizi di tempo può richiedere fino a 16 secondi. Pertanto, l'applicazione non deve attendere la richiesta.

Per garantire l'accuratezza, il provider di servizi ora deve recuperare tutte le informazioni relative all'ora [**usando GetTimeSysInfoFunc.**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)

Quando è il momento di arrestare il provider di servizi ora, il gestore del provider di servizi ora chiama [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).

 

 



