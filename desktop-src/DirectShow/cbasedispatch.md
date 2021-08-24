---
description: La classe CBaseDispatch è una classe di base per l'implementazione dell'interfaccia IDispatch in DirectShow filtro.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: Classe CBaseDispatch (Ctlutil.h)
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
ms.openlocfilehash: 1a094ad3b79dbeb8c4dfc2888de01a521738740fc19ad70b521172d3194fd9f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793317"
---
# <a name="cbasedispatch-class"></a>Classe CBaseDispatch

![Gerarchia di classi cbasedispatch](images/cutil01.png)

La **classe CBaseDispatch** è una classe di base per l'implementazione **dell'interfaccia IDispatch** in un DirectShow filtro.

Questa classe è limitata al supporto delle interfacce compatibili con Automazione esportate dalla libreria DirectShow tipi, QuartzTypeLib. Ad esempio, le [**classi CMediaControl**](cmediacontrol.md) e [**CMediaPosition**](cmediaposition.md) usano **CBaseDispatch per** implementare [**rispettivamente IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaPosition.**](/windows/desktop/api/Control/nn-control-imediaposition) A causa di questa limitazione, probabilmente non esiste alcun motivo per usare **CBaseDispatch** direttamente nei propri filtri.

Per usare questa classe, eseguire le operazioni seguenti:

-   Dichiarare una nuova classe che supporta **IDispatch.**
-   Assegnare alla nuova classe una variabile membro privata di **tipo CBaseDispatch**.
-   Implementare **i metodi IDispatch.**
-   Nei metodi **IDispatch** chiamare i **metodi CBaseDispatch.**

Per altri dettagli, vedere il codice sorgente per una delle classi di esempio dichiarate in Ctlutil.h.



| Metodi pubblici                                             | Descrizione                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CBaseDispatch**](cbasedispatch-cbasedispatch.md)       | Metodo del costruttore.                                                                                                 |
| [**~CBaseDispatch**](cbasedispatch--cbasedispatch.md)     | Metodo del distruttore.                                                                                                  |
| [**Getidsofnames**](cbasedispatch-getidsofnames.md)       | Mappe un set di nomi a un set corrispondente di DISPID.                                                              |
| [**GetTypeInfo**](cbasedispatch-gettypeinfo.md)           | Recupera le informazioni sul tipo per l'oggetto , che possono quindi essere utilizzate per ottenere le informazioni sul tipo per un'interfaccia. |
| [**GetTypeInfoCount**](cbasedispatch-gettypeinfocount.md) | Recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Classi di base](directshow-base-classes.md)
</dt> </dl>

 

 




