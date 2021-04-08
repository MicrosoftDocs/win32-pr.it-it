---
description: Impostazione e recupero della posizione
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Impostazione e recupero della posizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745410"
---
# <a name="setting-and-retrieving-the-position"></a>Impostazione e recupero della posizione

Il grafico del filtro mantiene due valori di posizione, la posizione corrente e la posizione di arresto. Questi vengono definiti come segue:

-   Quando il grafico è in esecuzione, la posizione corrente è la posizione di riproduzione corrente, relativa all'inizio dell'origine. Quando il grafico viene arrestato o sospeso, la posizione corrente è il punto in cui verrà avviato il flusso al successivo comando di esecuzione.
-   La posizione di arresto è il punto in cui si concluderà il flusso. Quando il grafico raggiunge la posizione di arresto, non viene eseguito il flusso di più dati e il gestore del grafo del filtro pubblica un evento di [**\_ completamento EC**](ec-complete.md) . Tuttavia, il grafico non passa automaticamente allo stato interrotto. Per ulteriori informazioni, vedere [risposta agli eventi](responding-to-events.md).

Per recuperare questi valori, chiamare il metodo [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) . I valori restituiti sono sempre relativi all'origine del supporto originale. Per impostazione predefinita, i valori sono in unità di tempo di riferimento. In alcuni casi, è possibile modificare le unità di tempo; per altre informazioni, vedere [formati di ora per i comandi Seek](time-formats-for-seek-commands.md).

Per cercare una nuova posizione o impostare una nuova posizione di arresto, chiamare il metodo [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , come illustrato nell'esempio seguente:


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
> Un secondo è 10 milioni unità di tempo di riferimento. Per praticità, l'esempio definisce questo valore come un \_ secondo. Se si usa la libreria di classi base DirectShow, le unità di costante hanno lo stesso valore.

 

Il parametro *rtNow* specifica la nuova posizione corrente. Il secondo parametro è un flag che definisce come interpretare *rtNow*. In questo esempio il flag AM \_ seeking \_ AbsolutePositioning indica che *rtNow* specifica una posizione assoluta nell'origine. Il grafico del filtro cercherà quindi una posizione di due secondi dall'inizio del flusso. Il parametro *rtStop* restituisce l'ora di arresto. L'ultimo parametro specifica che *rtStop* è anche una posizione assoluta.

Per specificare una posizione rispetto al valore di posizione precedente, usare il \_ \_ flag RelativePositioning seeking. Per lasciare invariato uno dei valori di posizione, utilizzare il \_ \_ flag nopositioning am seeking. Il parametro time corrispondente può essere **null** in questo caso. L'esempio seguente cerca di 10 secondi, ma lascia invariata la posizione di arresto:


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



Se il grafico del filtro viene arrestato, il renderer video non aggiorna l'immagine dopo un'operazione di ricerca. L'utente verrà visualizzato come se la ricerca non venisse eseguita. Per aggiornare l'immagine, sospendere il grafico dopo l'operazione di ricerca. La sospensione del grafico è un nuovo fotogramma video per il renderer video. È possibile usare il metodo [**IMediaControl:: StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) , che sospende il grafico e lo arresta.

 

 



