---
description: Il metodo CBaseList implementa un elenco a discesa. Il modello di classe CGenericList, che deriva da CBaseList, fornisce il controllo dei tipi e un'interfaccia più semplice rispetto alla classe CBaseList.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: Classe CBaseList (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5616edd16921bb2ae4d1a0b7ad67f5bbec3fba560594d4710512bd2cec6f275f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823707"
---
# <a name="cbaselist-class"></a>Classe CBaseList

![Gerarchia di classi cbaselist](images/list01.png)

Il **metodo CBaseList** implementa un elenco a discesa. Il [**modello di classe CGenericList,**](cgenericlist.md) che deriva da **CBaseList,** fornisce il controllo dei tipi e un'interfaccia più semplice rispetto alla **classe CBaseList.**

La **classe CBaseList** è modellata in base alla **classe CObList** nella libreria Microsoft Foundation Classes (MFC). Le posizioni all'interno dell'elenco sono rappresentate da una struttura POSITION. Il chiamante non deve accedere ai membri interni della struttura POSITION. considerarlo come un puntatore a un nodo elenco. La posizione di un oggetto nell'elenco rimane valida fino a quando l'oggetto non viene eliminato.

L'elenco non richiede alcun supporto da parte degli oggetti in esso contenuti. Non esegue operazioni di gestione o copia dell'archiviazione sugli oggetti. Gli oggetti possono essere in più elenchi.

Circa la metà dei metodi in questa classe agisce su singoli oggetti. Questi metodi hanno il suffisso I nel nome del metodo. Gli altri metodi agiscono su interi elenchi. Ad esempio, il [**metodo CBaseList::AddAfter**](cbaselist-addafter.md) aggiunge un elenco a un altro elenco. Le operazioni a oggetto singolo restituiscono valori POSITION o **NULL in** caso di errore. Le operazioni di elenco **restituiscono TRUE** in caso di esito positivo o **FALSE in caso** contrario.



| Variabili membro protette                             | Descrizione                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [**m \_ Count**](cbaselist-m-count.md)                  | Numero di elementi nell'elenco.                                              |
| [**m \_ pFirst**](cbaselist-m-pfirst.md)                | Puntatore al primo nodo dell'elenco.                                    |
| [**m \_ pLast**](cbaselist-m-plast.md)                  | Puntatore all'ultimo nodo nell'elenco.                                     |
| Metodi protetti                                      | Descrizione                                                               |
| [**GetNextI**](cbaselist-getnexti.md)                 | Recupera l'elemento nella posizione specificata e sposta in avanti la posizione.  |
| [**GetI**](cbaselist-geti.md)                         | Recupera l'elemento nella posizione specificata.                             |
| [**FindI**](cbaselist-findi.md)                       | Recupera la prima posizione che contiene l'elemento specificato.               |
| [**RemoveHeadI**](cbaselist-removeheadi.md)           | Rimuove il primo elemento dell'elenco.                                       |
| [**RemoveTailI**](cbaselist-removetaili.md)           | Rimuove l'ultimo elemento dell'elenco.                                        |
| [**RemoveI**](cbaselist-removei.md)                   | Rimuove l'elemento nella posizione specificata.                               |
| [**AddTailI**](cbaselist-addtaili.md)                 | Aggiunge un elemento alla fine dell'elenco.                                      |
| [**AddHeadI**](cbaselist-addheadi.md)                 | Aggiunge un elemento all'inizio dell'elenco.                                    |
| [**AddAfterI**](cbaselist-addafteri.md)               | Inserisce un elemento dopo la posizione specificata.                             |
| [**AddBeforeI**](cbaselist-addbeforei.md)             | Inserisce un elemento prima della posizione specificata.                            |
| Metodi pubblici                                         | Descrizione                                                               |
| [**CBaseList**](cbaselist-cbaselist.md)               | Metodo del costruttore.                                                       |
| [**~ CBaseList**](cbaselist--cbaselist.md)            | Metodo del distruttore.                                                        |
| [**RemoveAll**](cbaselist-removeall.md)               | Rimuove tutti i nodi dall'elenco.                                          |
| [**GetHeadPositionI**](cbaselist-getheadpositioni.md) | Recupera la posizione del primo elemento nell'elenco.                     |
| [**GetTailPositionI**](cbaselist-gettailpositioni.md) | Recupera la posizione dell'ultimo elemento dell'elenco.                      |
| [**GetCountI**](cbaselist-getcounti.md)               | Recupera il numero di elementi nell'elenco.                                |
| [**Avanti**](cbaselist-next.md)                         | Recupera la posizione successiva nell'elenco.                                  |
| [**Prev**](cbaselist-prev.md)                         | Recupera la posizione precedente nell'elenco.                              |
| [**AddHead**](cbaselist-addhead.md)                   | Inserisce un altro elenco all'inizio dell'elenco.                           |
| [**AddTail**](cbaselist-addtail.md)                   | Aggiunge un altro elenco alla fine dell'elenco.                             |
| [**AddAfter**](cbaselist-addafter.md)                 | Inserisce un elenco dopo la posizione specificata.                              |
| [**AddBefore**](cbaselist-addbefore.md)               | Inserisce un elenco prima della posizione specificata.                             |
| [**MoveToTail**](cbaselist-movetotail.md)             | Suddivide l'elenco e aggiunge la parte head alla fine di un altro elenco. |
| [**MoveToHead**](cbaselist-movetohead.md)             | Suddivide l'elenco e inserisce la parte finale all'inizio di un altro elenco. |
| [**Reverse**](cbaselist-reverse.md)                   | Inverte l'ordine dell'elenco.                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Classi di base](directshow-base-classes.md)
</dt> </dl>

 

 




