---
description: Linee guida per la registrazione dei filtri
ms.assetid: 05945937-9e01-4930-ae95-1931a711b55e
title: Linee guida per la registrazione dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed616d90c17d232995994d8ceccfdc72d022d56
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123399"
---
# <a name="guidelines-for-registering-filters"></a>Linee guida per la registrazione dei filtri

Le informazioni del registro di sistema di filtro determinano il modo [in cui](intelligent-connect.md)il gestore del grafo del filtro viene in funzione Quindi, influiscono su tutte le applicazioni scritte per DirectShow, non solo quelle che utilizzeranno il filtro. È necessario assicurarsi che il filtro si comporta correttamente, attenendosi alle linee guida.

1.  Sono necessari i dati del filtro nel registro di sistema? Per molti filtri personalizzati, non esiste alcun motivo per rendere visibile il filtro al mapper del filtro o all'enumeratore di dispositivo di sistema. Fino a quando si registra la DLL, l'applicazione può creare il filtro utilizzando **CoCreateInstance**. In tal caso, è sufficiente omettere la struttura del [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) dal modello Factory. Uno svantaggio è che il filtro non sarà visibile in GraphEdit. Per aggirare questo problema, è possibile creare una categoria privata di "testing" usando il metodo [**IFilterMapper2:: CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory) . Questa operazione deve essere eseguita solo per le compilazioni di debug.
2.  Scegliere la categoria di filtri corretta. La categoria predefinita "filtri DirectShow" è per i filtri per utilizzo generico. Quando appropriato, registrare il filtro in una categoria più specifica. Quando [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) Cerca un filtro, ignora qualsiasi categoria il cui merito è Merit \_ \_ non \_ usare o meno. Le categorie non destinate alla riproduzione normale hanno un merito basso.
3.  Evitare di specificare MEDIATYPE \_ None, MEDIASUBTYPE \_ None o GUID \_ null nelle informazioni [**AMOVIESETUP \_ MEDIATYPE**](amoviesetup-mediatype.md) per un PIN. **IFilterMapper2** li considera come caratteri jolly, che possono rallentare il processo di creazione di grafici.
4.  Scegliere il valore di Merit più basso possibile. Di seguito sono riportate alcune linee guida:

    | Type of filter                                                                                       | Meriti consigliati                                                                                   |
    |------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
    | Renderer predefinito                                                                                     | \_preferenza preferita. Per i tipi di supporto standard, tuttavia, un renderer personalizzato non deve mai essere il valore predefinito. |
    | Renderer non predefinito                                                                                 | MERIT \_ non \_ \_ use o Merit \_ improbabile                                                              |
    | Mux                                                                                                  | il merito non viene \_ \_ \_ utilizzato                                                                                 |
    | Decodificatore                                                                                              | VALORE \_ normale                                                                                       |
    | Spitter, parser                                                                                      | VALORE \_ normale o inferiore                                                                              |
    | Filtro per scopi specifici; qualsiasi filtro creato direttamente dall'applicazione                       | il merito non viene \_ \_ \_ utilizzato                                                                                 |
    | Acquisizione                                                                                              | il merito non viene \_ \_ \_ utilizzato                                                                                 |
    | Filtro di "fallback"; ad esempio, il [filtro del convertitore dello spazio colori](color-space-converter-filter.md) | VALORE \_ improbabile                                                                                     |

    

     

    Se si assegna un filtro a un valore di merito \_ \_ non \_ usato, valutare se è necessario registrare queste informazioni nella prima posizione. (Vedere l'elemento 1).

5.  Non registrare un filtro nella categoria "filtri DirectShow" che accetta RGB a 24 bit. Il filtro interferisce con il filtro del convertitore dello spazio colori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come registrare i filtri DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



