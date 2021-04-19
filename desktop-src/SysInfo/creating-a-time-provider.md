---
description: Un provider di ora viene implementato come una DLL. Ogni DLL può supportare più provider di tempo. Ogni provider è responsabile della propria configurazione e della propria sincronizzazione.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Creazione di un provider Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319899"
---
# <a name="creating-a-time-provider"></a>Creazione di un provider Time

Un provider di ora viene implementato come una DLL. Ogni DLL può supportare più provider di tempo. Ogni provider è responsabile della propria configurazione e della propria sincronizzazione.

I provider di servizi temporali devono implementare le funzioni di callback seguenti:

-   [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

Dopo aver caricato la DLL del provider, il gestore del provider di servizi temporali chiama [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), passando il nome del provider e i puntatori alle funzioni seguenti:

-   [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

Queste funzioni sono destinate all'uso da parte del provider di servizi temporali. Il provider Time USA [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) per restituire un handle del provider usato da gestione provider di servizi temporali per l'invio di comandi al provider di servizi temporali. Il valore dell'handle viene definito dal provider di tempo e viene utilizzato principalmente per distinguere tra provider diversi implementati nella stessa DLL. Il provider di servizi temporali può registrare eventi significativi usando [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).

Gestione provider di servizi temporali USA [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) per inviare comandi al provider di servizi temporali. Quando il provider del tempo deve notificare al gestore del provider di servizi temporali la disponibilità di esempi temporali, viene chiamato [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc). Il gestore del provider di servizi ora chiama **TimeProvCommand** con il \_ comando TPC getSamples per recuperare gli esempi temporali. Potrebbero essere richiesti fino a 16 secondi affinché il gestore del provider di servizi temporali richieda l'esempio. Pertanto, l'applicazione non deve attendere la richiesta.

Per garantire l'accuratezza, il provider di tempo deve recuperare tutte le informazioni relative al tempo usando [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).

Quando è il momento di arrestare il provider di tempo, il gestore del provider di servizi ora chiama [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).

 

 



