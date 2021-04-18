---
description: La classe CBaseDispatch è una classe di base per l'implementazione dell'interfaccia IDispatch in un filtro DirectShow.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: Classe CBaseDispatch (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327965"
---
# <a name="cbasedispatch-class"></a>Classe CBaseDispatch

![gerarchia di classi cbasedispatch](images/cutil01.png)

La classe **CBaseDispatch** è una classe di base per l'implementazione dell'interfaccia **IDispatch** in un filtro DirectShow.

Questa classe è limitata al supporto delle interfacce compatibili con l'automazione esportate dalla libreria dei tipi DirectShow, file QuartzTypeLib. Ad esempio, le classi [**CMediaControl**](cmediacontrol.md) e [**CMediaPosition**](cmediaposition.md) usano **CBaseDispatch** per implementare rispettivamente [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition). A causa di questa limitazione, probabilmente non esiste alcun motivo per usare **CBaseDispatch** direttamente nei filtri personalizzati.

Per usare questa classe, eseguire le operazioni seguenti:

-   Dichiarare una nuova classe che supporta **IDispatch**.
-   Assegnare alla nuova classe una variabile membro privata di tipo **CBaseDispatch**.
-   Implementare i metodi **IDispatch** .
-   Nei metodi **IDispatch** chiamare i metodi **CBaseDispatch** .

Per ulteriori informazioni, fare riferimento al codice sorgente per le classi di esempio dichiarate in Ctlutil. h.



| Metodi pubblici                                             | Descrizione                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CBaseDispatch**](cbasedispatch-cbasedispatch.md)       | Metodo del costruttore.                                                                                                 |
| [**~ CBaseDispatch**](cbasedispatch--cbasedispatch.md)     | Metodo del distruttore.                                                                                                  |
| [**GetIDsOfNames**](cbasedispatch-getidsofnames.md)       | Esegue il mapping di un set di nomi a un set di DISPID corrispondente.                                                              |
| [**GetTypeInfo**](cbasedispatch-gettypeinfo.md)           | Recupera le informazioni sul tipo per l'oggetto, che può quindi essere utilizzato per ottenere le informazioni sul tipo per un'interfaccia. |
| [**GetTypeInfoCount**](cbasedispatch-gettypeinfocount.md) | Recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi base di DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




