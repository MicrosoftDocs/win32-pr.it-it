---
description: La classe CBaseReferenceClock implementa un clock di riferimento.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: Classe CBaseReferenceClock (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329410"
---
# <a name="cbasereferenceclock-class"></a>Classe CBaseReferenceClock

![gerarchia di classi cbasereferenceclock](images/rclock01.png)

La `CBaseReferenceClock` classe implementa un clock di riferimento.



| Variabili membro protette                                                         | Descrizione                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_pSchedule m**](cbasereferenceclock-m-pschedule.md)                            | Oggetto [**CAMSchedule**](camschedule.md) che gestisce le attività di pianificazione del clock. |
| Metodi protetti                                                                  | Descrizione                                                                            |
| [**~ CBaseReferenceClock**](cbasereferenceclock--cbasereferenceclock.md)           | Metodo del distruttore.                                                                     |
| Metodi pubblici                                                                     | Descrizione                                                                            |
| [**CBaseReferenceClock**](cbasereferenceclock-cbasereferenceclock.md)             | Metodo del costruttore.                                                                    |
| [**GetPrivateTime**](cbasereferenceclock-getprivatetime.md)                       | Recupera il tempo reale dal clock.                                                |
| [**SetTimeDelta**](cbasereferenceclock-settimedelta.md)                           | Regola l'ora di clock interna.                                                       |
| [**Getschedule**](cbasereferenceclock-getschedule.md)                             | Recupera un puntatore all'oggetto di pianificazione del clock.                                  |
| [**TriggerThread**](cbasereferenceclock-triggerthread.md)                         | Attiva il thread di lavoro che gestisce la pianificazione.                                    |
| Metodi IReferenceClock                                                            | Descrizione                                                                            |
| [**GetTime**](cbasereferenceclock-gettime.md)                                     | Recupera l'ora di riferimento corrente.                                                  |
| [**AdviseTime**](cbasereferenceclock-advisetime.md)                               | Crea una richiesta di notifica di un unico tentativo.                                                     |
| [**AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md)                       | Crea una richiesta di notifica periodica.                                                     |
| [**Unadvise**](cbasereferenceclock-unadvise.md)                                   | Rimuove una richiesta di notifica in sospeso.                                                      |
| Metodi IReferenceClockTimerControl                                                | Descrizione                                                                            |
| [**GetDefaultTimerResolution**](cbasereferenceclock-getdefaulttimerresolution.md) | Restituisce la risoluzione corrente del timer del clock di riferimento.                         |
| [**SetDefaultTimerResolution**](cbasereferenceclock-setdefaulttimerresolution.md) | Imposta la risoluzione del timer del clock di riferimento.                                    |
| Funzioni di supporto                                                                   | Descrizione                                                                            |
| [**ConvertToMilliseconds**](converttomilliseconds.md)                             | Converte un'ora di riferimento in millisecondi.                                             |



 

## <a name="remarks"></a>Commenti

Questa classe implementa un clock di riferimento che supporta le interfacce [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) e [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) . Se un filtro può fornire un orologio di riferimento per il grafico di filtro, ad esempio accedendo a un dispositivo hardware, può usare questa classe per implementare l'orologio.

L' `CBaseReferenceClock` oggetto gestisce due valori temporali distinti:

-   Internamente, il metodo [**CBaseReferenceClock:: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) restituisce il tempo effettivo mantenuto dal clock.
-   Esternamente, il metodo [**CBaseReferenceClock:: GetTime**](cbasereferenceclock-gettime.md) restituisce l'ora di riferimento per il grafico del filtro.

È valido per l'esecuzione del clock interno indietro per brevi periodi. Se, ad esempio, il clock si sposta in avanti, il filtro può adattarlo all'indietro. Vedere [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md). Il metodo **getTime** usa i valori temporali restituiti da **GetPrivateTime**. Tuttavia, l'ora di riferimento è a incremento progressivo costante. in altre parole, non viene mai eseguito all'indietro. Di conseguenza, se il clock interno viene eseguito indietro, **getTime** continua a segnalare l'ora precedente fino a quando l'orologio interno non viene ripreso.

Ad esempio, i due metodi potrebbero restituire le sequenze seguenti:

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

Al terzo Tick del clock, il clock interno passa indietro a 103. Il metodo **getTime** continua a segnalare 106 fino a quando l'orologio interno non viene ripreso.

Per impostazione predefinita, **GetPrivateTime** restituisce l'ora di sistema tramite una chiamata alla funzione **timeGetTime** . Un filtro che fornisce un orologio di riferimento da un dispositivo esterno può eseguire una delle operazioni seguenti:

-   Eseguire l'override di **GetPrivateTime** per restituire l'ora dal dispositivo.
-   Monitorare la discrepanza tra l'ora del dispositivo e l'ora di sistema e chiamare **SetTimeDelta** per apportare le correzioni.

Questa classe usa un oggetto [**CAMSchedule**](camschedule.md) per gestire la pianificazione delle richieste di notifica. Per informazioni dettagliate, vedere la documentazione per la classe **CAMSchedule** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




