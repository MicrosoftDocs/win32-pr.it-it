---
description: Modello di classe CGenericList che implementa un elenco specifico del tipo. Per ulteriori informazioni, vedere CBaseList.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: Classe CGenericList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329792"
---
# <a name="cgenericlist-class"></a>Classe CGenericList

![gerarchia di classi cgenericlist](images/list01.png)

`CGenericList`Modello di classe che implementa un elenco specifico del tipo. Per ulteriori informazioni, vedere [**CBaseList**](cbaselist.md).

Per usare questo modello, dichiarare una variabile di tipo `CGenericList` con un argomento di modello che definisce il tipo di oggetto nell'elenco. L'istruzione seguente, ad esempio, dichiara un elenco di oggetti [**CBaseFilter**](cbasefilter.md) :


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



Per praticità, Wxlist. h definisce i tipi di elenco seguenti:

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| Metodi pubblici                                          | Descrizione                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**CGenericList**](cgenericlist-cgenericlist.md)       | Metodo del costruttore.                                                      |
| [**~ CGenericList**](cgenericlist--cgenericlist.md)     | Metodo del distruttore.                                                       |
| [**GetHeadPosition**](cgenericlist-getheadposition.md) | Recupera la posizione del primo elemento nell'elenco.                    |
| [**GetTailPosition**](cgenericlist-gettailposition.md) | Recupera la posizione dell'ultimo elemento dell'elenco.                     |
| [**GetCount**](cgenericlist-getcount.md)               | Recupera il numero di elementi nell'elenco.                               |
| [**GetNext**](cgenericlist-getnext.md)                 | Recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione. |
| [**Recupero**](cgenericlist-get.md)                         | Recupera l'elemento in corrispondenza della posizione specificata.                            |
| [**GetHead**](cgenericlist-gethead.md)                 | Recupera l'elemento all'inizio dell'elenco.                              |
| [**RemoveHead**](cgenericlist-removehead.md)           | Rimuove il primo elemento nell'elenco.                                      |
| [**RemoveTail**](cgenericlist-removetail.md)           | Rimuove l'ultimo elemento dell'elenco.                                       |
| [**Rimuovi**](cgenericlist-remove.md)                   | Rimuove l'elemento nella posizione specificata.                              |
| [**AddBefore**](cgenericlist-addbefore.md)             | Inserisce un elemento o un elenco prima della posizione specificata.                   |
| [**AddAfter**](cgenericlist-addafter.md)               | Inserisce un elemento o un elenco dopo la posizione specificata.                    |
| [**AddHead**](cgenericlist-addhead.md)                 | Aggiunge un elemento o un elenco all'inizio dell'elenco.                           |
| [**AddTail**](cgenericlist-addtail.md)                 | Accoda un elemento o un elenco alla fine dell'elenco.                          |
| [**Find**](cgenericlist-find.md)                       | Recupera la prima posizione che include l'elemento specificato.              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




