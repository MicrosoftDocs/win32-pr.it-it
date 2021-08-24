---
description: Linee guida per la registrazione dei filtri
ms.assetid: 05945937-9e01-4930-ae95-1931a711b55e
title: Linee guida per la registrazione dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221cadf6fb4806a2fa5c5b2cc4fd9abf423cec426ec23cd76b0bc642080852af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905361"
---
# <a name="guidelines-for-registering-filters"></a>Linee guida per la registrazione dei filtri

Le informazioni del registro filtri determinano il funzionamento di Filter Graph Manager durante [l'Connessione](intelligent-connect.md). Influisce quindi su ogni applicazione scritta per DirectShow, non solo su quelle che useranno il filtro. È necessario assicurarsi che il filtro funzioni correttamente, seguendo queste linee guida.

1.  Sono necessari i dati di filtro nel Registro di sistema? Per molti filtri personalizzati, non esiste alcun motivo per rendere il filtro visibile a Filter Mapper o all'enumeratore del dispositivo di sistema. Se si registra la DLL, l'applicazione può creare il filtro usando **CoCreateInstance**. In tal caso, è sufficiente omettere la [**struttura AMOVIESETUP \_ FILTER**](amoviesetup-filter.md) dal modello di factory. Uno svantaggio è che il filtro non sarà visibile in GraphEdit. Per risolvere questo problema, è possibile creare una categoria "Testing" privata usando il [**metodo IFilterMapper2::CreateCategory.**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory) È consigliabile eseguire questa operazione solo per le build di debug.
2.  Scegliere la categoria di filtro corretta. La categoria predefinita "DirectShow filtri" è per i filtri per utilizzo generico. Se necessario, registrare il filtro in una categoria più specifica. Quando [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) cerca un filtro, ignora qualsiasi categoria il cui merito è MERIT \_ DO NOT USE o \_ \_ minore. Le categorie non destinate alla riproduzione normale hanno un merito basso.
3.  Evitare di specificare MEDIATYPE None, MEDIASUBTYPE None o GUID NULL nelle informazioni \_ \_ \_ [**AMOVIESETUP \_ MEDIATYPE**](amoviesetup-mediatype.md) per un pin. **IFilterMapper2** li considera come caratteri jolly, che possono rallentare il processo di creazione del grafo.
4.  Scegliere il valore di merito più basso possibile. Ecco alcune linee guida:

    | Type of filter                                                                                       | Merito consigliato                                                                                   |
    |------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
    | Renderer predefinito                                                                                     | MERITO \_ PREFERITO. Per i tipi di supporti standard, tuttavia, un renderer personalizzato non deve mai essere l'impostazione predefinita. |
    | Renderer non predefinito                                                                                 | MERITO \_ NON USARE O MERITO \_ \_ \_ IMPROBABILE                                                              |
    | Mux                                                                                                  | MERITO \_ NON \_ \_ USARE                                                                                 |
    | Decodificatore                                                                                              | MERITO \_ NORMALE                                                                                       |
    | Spitter, parser                                                                                      | MERIT \_ NORMAL o inferiore                                                                              |
    | Filtro per scopi speciali; qualsiasi filtro creato direttamente dall'applicazione                       | MERITO \_ NON \_ \_ USARE                                                                                 |
    | Acquisizione                                                                                              | MERITO \_ NON \_ \_ USARE                                                                                 |
    | Filtro "Fallback"; ad esempio il filtro [del convertitore dello spazio colori](color-space-converter-filter.md) | MERITO \_ IMPROBABILE                                                                                     |

    

     

    Se si sta fornendo a un filtro un merito di MERIT DO NOT USE, valutare se è necessario registrare queste \_ \_ informazioni in primo \_ luogo. Vedere l'elemento 1.

5.  Non registrare un filtro nella categoria "DirectShow filtri" che accetta RGB a 24 bit. Il filtro interferirà con il filtro del convertitore dello spazio colori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come registrare DirectShow filtri](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



