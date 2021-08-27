---
description: La classe CEnumMediaTypes implementa un enumeratore per i tipi di supporti preferiti.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: Classe CEnumMediaTypes (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1729407f1022c2781fc97f8638ea8748323c151e9bd67c5ad31b30ae05fdff0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131276"
---
# <a name="cenummediatypes-class"></a>Classe CEnumMediaTypes

![Gerarchia di classi cenummediatypes](images/filter04.png)

La `CEnumMediaTypes` classe implementa un enumeratore per i tipi di supporti preferiti.

Questa classe implementa [**l'interfaccia IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) Chiama i metodi [**CBasePin**](cbasepin.md) seguenti:

-   [**CBasePin::GetMediaType:**](cbasepin-getmediatype.md)recupera un tipo di supporto, a cui fa riferimento un indice in base zero.
-   [**CBasePin::GetMediaTypeVersion:**](cbasepin-getmediatypeversion.md)determina se il set di tipi preferiti è stato modificato.

Ogni volta che un pin modifica l'elenco dei tipi di supporti preferiti, il pin incrementa il numero di versione del tipo di supporto. In questo caso, l'oggetto enumeratore non è più sincronizzato con il pin e i metodi della classe restituiscono VFW \_ \_ ENUM \_ OUT OF \_ \_ SYNC. Chiamare il [**metodo CEnumMediaTypes::Reset**](cenummediatypes-reset.md) per risincronizzare l'enumeratore.



| Metodi pubblici                                               | Descrizione                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [**CEnumMediaTypes**](cenummediatypes-cenummediatypes.md)   | Metodo del costruttore.                                             |
| [**~CEnumMediaTypes**](cenummediatypes--cenummediatypes.md) | Metodo del distruttore. Virtuale.                                     |
| Metodi di IEnumMediaTypes                                      | Descrizione                                                     |
| [**Clone**](cenummediatypes-clone.md)                       | Crea una copia dell'enumeratore con lo stesso stato di enumerazione. |
| [**Avanti**](cenummediatypes-next.md)                         | Recupera un numero specificato di tipi di supporti.                    |
| [**Reset**](cenummediatypes-reset.md)                       | Riporta all'inizio la sequenza di enumerazione.               |
| [**Ignora**](cenummediatypes-skip.md)                         | Ignora un numero specificato di tipi di supporti.                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




