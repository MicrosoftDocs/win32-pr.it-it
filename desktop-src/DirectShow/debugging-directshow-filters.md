---
description: Molte delle funzionalità di debug descritte in questo argomento vengono implementate nella DirectShow di classi di base. Per altre informazioni, vedere Classi DirectShow base.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Debug DirectShow filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54532b68df09b78b3b03aa95d7dda5c84cdf7d770cffd131e47228e6d88cba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953290"
---
# <a name="debugging-directshow-filters"></a>Debug DirectShow filtri

Molte delle funzionalità di debug descritte in questo argomento vengono implementate nella DirectShow di classi di base. Per altre informazioni, vedere Classi [DirectShow base](directshow-base-classes.md).

## <a name="assertion-checking"></a>Controllo delle asserzioni

Usare il controllo delle asserzioni in modo libero. Le asserzioni possono verificare i presupposti che si fanno nel codice sulle precondizioni e sulle postcondizioni. DirectShow fornisce diverse macro di asserzione. Per altre informazioni, vedere [Macro di asserzione e punti di interruzione](assert-and-breakpoint-macros.md).

## <a name="object-names"></a>Nomi di oggetti

Nelle build di debug è disponibile un elenco globale di oggetti che derivano dalla [**classe CBaseObject.**](cbaseobject.md) Quando vengono creati, gli oggetti vengono aggiunti all'elenco. Quando vengono eliminati definitivamente, vengono rimossi dall'elenco. Per visualizzare un elenco di tali oggetti, chiamare la [**funzione DbgDumpObjectRegister.**](dbgdumpobjectregister.md)

Il metodo del costruttore per la classe di base [**CBaseObject**](cbaseobject.md) e la maggior parte delle classi derivate da essa include un parametro per il nome dell'oggetto. Assegnare agli oggetti nomi univoci per identificarli. Usare la macro [**NAME**](name.md) quando si dichiara il nome, in modo che il nome sia allocato solo nelle build di debug. Nelle build di vendita al dettaglio il nome diventa **NULL.**

## <a name="debug-logging"></a>Registrazione debug

La [**funzione DbgLog**](dbglog.md) visualizza i messaggi di debug durante l'esecuzione del programma. Usare questa funzione per tracciare l'esecuzione dell'applicazione o del filtro. È possibile registrare i codici restituiti, i valori delle variabili e qualsiasi altra informazione pertinente.

Ogni messaggio di debug ha un tipo, ad esempio LOG TRACE o LOG ERROR, e un livello di debug, che indica \_ \_ l'importanza del messaggio. I messaggi con livelli di debug inferiori sono più importanti di quelli con livelli superiori.

Nell'esempio seguente un filtro ipotetico disconnette un segnaposto da una matrice di pin. Se il tentativo di disconnessione ha esito positivo, il filtro visualizza un messaggio LOG \_ TRACE. Se il tentativo non riesce, viene visualizzato un messaggio \_ LOG ERROR:


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



Quando si esegue il debug, è possibile impostare il livello di debug per ogni tipo di messaggio. Inoltre, ogni modulo (DLL o eseguibile) mantiene i propri livelli di debug. Se si sta testando un filtro, aumentare i livelli di debug per la DLL che contiene il filtro.

Per altre informazioni, vedere [Funzioni di output di debug](debug-output-functions.md).

## <a name="critical-sections"></a>Sezioni critiche

Per semplificare il rilevamento dei deadlock, includere asserzioni che determinano se il codice chiamante è proprietario di una determinata sezione critica. Le [**funzioni CritCheckIn**](critcheckin.md) e [**CritCheckOut**](critcheckout.md) indicano se il thread chiamante è proprietario di una sezione critica. In genere, queste funzioni vengono chiamate dall'interno di una macro di asserzione.

È anche possibile usare la [**funzione DbgLockTrace**](dbglocktrace.md) per tracciare quando vengono mantenute o rilasciate sezioni critiche.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug in DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



