---
description: Molte delle funzionalità di debug descritte in questo argomento sono implementate nella libreria di classi base DirectShow. Per altre informazioni, vedere classi base di DirectShow.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Debug dei filtri DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522554"
---
# <a name="debugging-directshow-filters"></a>Debug dei filtri DirectShow

Molte delle funzionalità di debug descritte in questo argomento sono implementate nella libreria di classi base DirectShow. Per altre informazioni, vedere [classi base di DirectShow](directshow-base-classes.md).

## <a name="assertion-checking"></a>Verifica dell'asserzione

Usare il controllo dell'asserzione in tutta liberalità. Le asserzioni possono verificare i presupposti che si apportano nel codice sulle precondizioni e le postcondizioni. DirectShow fornisce diverse macro di asserzione. Per altre informazioni, vedere [macro ASSERT e breakpoint](assert-and-breakpoint-macros.md).

## <a name="object-names"></a>Nomi di oggetti

Nelle build di debug è presente un elenco globale di oggetti che derivano dalla classe [**CBaseObject**](cbaseobject.md) . Man mano che vengono creati, gli oggetti vengono aggiunti all'elenco. Quando vengono eliminati definitivamente, vengono rimossi dall'elenco. Per visualizzare un elenco di tali oggetti, chiamare la funzione [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) .

Il metodo del costruttore per la classe base [**CBaseObject**](cbaseobject.md) , e la maggior parte delle classi derivate da esso, include un parametro per il nome dell'oggetto. Assegnare agli oggetti nomi univoci per identificarli. Usare la macro [**Name**](name.md) quando si dichiara il nome, in modo che il nome venga allocato solo nelle compilazioni di debug. Nelle compilazioni finali il nome diventa **null**.

## <a name="debug-logging"></a>Registrazione debug

La funzione [**DbgLog**](dbglog.md) Visualizza i messaggi di debug durante l'esecuzione del programma. Usare questa funzione per tenere traccia dell'esecuzione dell'applicazione o del filtro. È possibile registrare i codici restituiti, i valori delle variabili e altre informazioni rilevanti.

Ogni messaggio di debug dispone di un tipo, ad esempio log \_ Trace o log \_ Error e un livello di debug, che indica l'importanza del messaggio. I messaggi con livelli di debug inferiori sono più importanti rispetto a quelli con livelli più elevati.

Nell'esempio seguente un filtro ipotetico disconnette un pin da una matrice di pin. Se il tentativo di disconnessione ha esito positivo, il filtro Visualizza un messaggio di traccia del LOG \_ . Se il tentativo non riesce, viene visualizzato un \_ messaggio di errore di log:


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



Quando si esegue il debug, è possibile impostare il livello di debug per ogni tipo di messaggio. Ogni modulo (DLL o eseguibile) mantiene inoltre i propri livelli di debug. Se si sta testando un filtro, aumentare i livelli di debug per la DLL che contiene il filtro.

Per altre informazioni, vedere [debug di funzioni di output](debug-output-functions.md).

## <a name="critical-sections"></a>Sezioni critiche

Per semplificare la traccia dei deadlock, includere asserzioni che determinano se il codice chiamante possiede una sezione critica specificata. Le funzioni [**CritCheckIn**](critcheckin.md) e [**CritCheckOut**](critcheckout.md) indicano se il thread chiamante è proprietario di una sezione critica. In genere, queste funzioni vengono chiamate dall'interno di una macro ASSERT.

È anche possibile usare la funzione [**DbgLockTrace**](dbglocktrace.md) per tracciare quando le sezioni critiche vengono mantenute o rilasciate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug in DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



