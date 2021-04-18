---
description: Il metodo CBaseList implementa un elenco di Abtract. Il modello di classe CGenericList, che deriva da CBaseList, fornisce il controllo del tipo e un'interfaccia più semplice rispetto alla classe CBaseList.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: Classe CBaseList (Wxlist. h)
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
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325673"
---
# <a name="cbaselist-class"></a>Classe CBaseList

![gerarchia di classi cbaselist](images/list01.png)

Il metodo **CBaseList** implementa un elenco di Abtract. Il modello di classe [**CGenericList**](cgenericlist.md) , che deriva da **CBaseList**, fornisce il controllo del tipo e un'interfaccia più semplice rispetto alla classe **CBaseList** .

La classe **CBaseList** viene modellata dopo la classe **CObList** nella libreria Microsoft Foundation Classes (MFC). Le posizioni all'interno dell'elenco sono rappresentate da una struttura di posizione. Il chiamante non deve accedere ai membri interni della struttura di posizione; considerarlo come un puntatore a un nodo elenco. La posizione di un oggetto nell'elenco rimane valida fino a quando l'oggetto non viene eliminato.

L'elenco non richiede alcun supporto per gli oggetti in esso contenuti. Non esegue alcuna gestione dell'archiviazione o copia sugli oggetti. Gli oggetti possono trovarsi in più elenchi.

Approssimativamente la metà dei metodi in questa classe agisce su singoli oggetti. Questi metodi hanno il suffisso-I nel nome del metodo. Gli altri metodi agiscono su interi elenchi. Ad esempio, il metodo [**CBaseList:: AddAfter**](cbaselist-addafter.md) Accoda un elenco a un altro elenco. Le operazioni a oggetto singolo restituiscono valori di posizione o **null** in caso di errore. Le operazioni di elenco restituiscono **true** in caso di esito positivo o **falso** .



| Variabili membro protette                             | Descrizione                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [**\_conteggio m**](cbaselist-m-count.md)                  | Numero di elementi nell'elenco.                                              |
| [**\_pFirst m**](cbaselist-m-pfirst.md)                | Puntatore al primo nodo nell'elenco.                                    |
| [**m \_ pLast**](cbaselist-m-plast.md)                  | Puntatore all'ultimo nodo nell'elenco.                                     |
| Metodi protetti                                      | Descrizione                                                               |
| [**Getnexti**](cbaselist-getnexti.md)                 | Recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione.  |
| [**GetI**](cbaselist-geti.md)                         | Recupera l'elemento in corrispondenza della posizione specificata.                             |
| [**FindI**](cbaselist-findi.md)                       | Recupera la prima posizione che include l'elemento specificato.               |
| [**RemoveHeadI**](cbaselist-removeheadi.md)           | Rimuove il primo elemento nell'elenco.                                       |
| [**RemoveTailI**](cbaselist-removetaili.md)           | Rimuove l'ultimo elemento dell'elenco.                                        |
| [**Rimuovi**](cbaselist-removei.md)                   | Rimuove l'elemento nella posizione specificata.                               |
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
| [**Getcounti**](cbaselist-getcounti.md)               | Recupera il numero di elementi nell'elenco.                                |
| [**Avanti**](cbaselist-next.md)                         | Recupera la posizione successiva nell'elenco.                                  |
| [**Prev**](cbaselist-prev.md)                         | Recupera la posizione precedente nell'elenco.                              |
| [**AddHead**](cbaselist-addhead.md)                   | Inserisce un altro elenco all'inizio dell'elenco.                           |
| [**AddTail**](cbaselist-addtail.md)                   | Accoda un altro elenco alla fine dell'elenco.                             |
| [**AddAfter**](cbaselist-addafter.md)                 | Inserisce un elenco dopo la posizione specificata.                              |
| [**AddBefore**](cbaselist-addbefore.md)               | Inserisce un elenco prima della posizione specificata.                             |
| [**MoveToTail**](cbaselist-movetotail.md)             | Suddivide l'elenco e aggiunge la parte Head alla parte finale di un altro elenco. |
| [**MoveToHead**](cbaselist-movetohead.md)             | Suddivide l'elenco e inserisce la parte finale all'inizio di un altro elenco. |
| [**Inverso**](cbaselist-reverse.md)                   | Inverte l'ordine dell'elenco.                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi base di DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




