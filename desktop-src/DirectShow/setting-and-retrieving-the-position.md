---
description: Impostazione e recupero della posizione
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Impostazione e recupero della posizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7951ce12fe498a4f230ab3d1ac84796621e04ed025010678f1c43a39d88eb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683691"
---
# <a name="setting-and-retrieving-the-position"></a>Impostazione e recupero della posizione

Il grafico dei filtri mantiene due valori di posizione, la posizione corrente e la posizione di arresto. Questi sono definiti come segue:

-   Quando il grafico è in esecuzione, la posizione corrente è la posizione di riproduzione corrente, relativa all'inizio dell'origine. Quando il grafo viene arrestato o sospeso, la posizione corrente è il punto in cui lo streaming inizierà al comando di esecuzione successivo.
-   La posizione di arresto è il punto in cui termina il flusso. Quando il grafo raggiunge la posizione di arresto, non vengono trasmessi altri dati e il gestore del grafo del filtro invia un [**evento EC \_ COMPLETE.**](ec-complete.md) Tuttavia, il grafico non passa automaticamente a uno stato arrestato. Per altre informazioni, vedere [Risposta agli eventi.](responding-to-events.md)

Per recuperare questi valori, chiamare il [**metodo IMediaSeeking::GetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) I valori restituiti sono sempre relativi all'origine multimediale originale. Per impostazione predefinita, i valori sono in unità di tempo di riferimento. In alcuni casi, è possibile modificare le unità di tempo. Per altre informazioni, vedere [Formati di ora per i comandi Seek](time-formats-for-seek-commands.md).

Per cercare una nuova posizione o impostare una nuova posizione di arresto, chiamare il metodo [**IMediaSeeking::SetPositions,**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) come illustrato nell'esempio seguente:


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> Un secondo è 10.000.000 unità di tempo di riferimento. Per praticità, l'esempio definisce questo valore come UN \_ SECONDO. Se si usa la libreria DirectShow di classi base, la costante UNITS ha lo stesso valore.

 

Il *parametro rtNow* specifica la nuova posizione corrente. Il secondo parametro è un flag che definisce come interpretare *rtNow*. In questo esempio il flag AM SEEKING AbsolutePositioning indica che rtNow specifica una \_ \_ posizione assoluta nell'origine.  Pertanto, il grafico dei filtri cercherà una posizione a due secondi dall'inizio del flusso. Il *parametro rtStop* indica l'ora di arresto. L'ultimo parametro specifica che *anche rtStop* è una posizione assoluta.

Per specificare una posizione relativa al valore della posizione precedente, usare il flag AM \_ SEEKING \_ RelativePositioning. Per lasciare invariato uno dei valori di posizione, usare il flag AM \_ SEEKING \_ NoPositioning. In tal caso, il parametro time corrispondente **può essere NULL.** L'esempio seguente cerca in avanti di 10 secondi, ma lascia invariata la posizione di arresto:


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



Se il grafico dei filtri viene arrestato, il renderer video non aggiorna l'immagine dopo un'operazione di ricerca. All'utente verrà visualizzato come se la ricerca non fosse stata verificata. Per aggiornare l'immagine, sospendere il grafico dopo l'operazione di ricerca. La sospensione del grafo crea un nuovo fotogramma video per il renderer video. È possibile usare il [**metodo IMediaControl::StopWhenReady,**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) che sospende il grafo e lo arresta.

 

 



