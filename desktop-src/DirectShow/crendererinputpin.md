---
description: La classe CBaseRendererInputPin implementa un pin di input per la classe CBaseRenderer. Eccetto laddove indicato, i metodi di questa classe delegano ai metodi corrispondenti sulla classe CBaseRenderer.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: Classe CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ec48b31170b2233f211e7e72de81d8792ae9160
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333172"
---
# <a name="crendererinputpin-class"></a>Classe CRendererInputPin

![crendererinput gerarchia di classi pin](images/rbase01.png)

La classe **CBaseRendererInputPin** implementa un pin di input per la classe [**CBaseRenderer**](cbaserenderer.md) . Eccetto laddove indicato, i metodi di questa classe delegano ai metodi corrispondenti sulla classe **CBaseRenderer** .



| Variabili membro protette                                       | Descrizione                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_pRenderer m**](crendererinputpin-m-prenderer.md)            | Puntatore al filtro.                                                                 |
| Metodi pubblici                                                   | Descrizione                                                                            |
| [**CRendererInputPin**](crendererinputpin-crendererinputpin.md) | Metodo del costruttore.                                                                    |
| [**BreakConnect**](crendererinputpin-breakconnect.md)           | Aggiunge codice personalizzato quando si interrompe una connessione.                                       |
| [**CompleteConnect**](crendererinputpin-completeconnect.md)     | Completa la connessione.                                                              |
| [**CheckMediaType**](crendererinputpin-checkmediatype.md)       | Determina se il pin può supportare un tipo di supporto specifico.                               |
| [**Attivo**](crendererinputpin-active.md)                       | Passa il pin alla modalità attiva (in pausa o in esecuzione).                               |
| [**Inattivo**](crendererinputpin-inactive.md)                   | Passa il pin a uno stato inattivo e rilascia la memoria dell'allocatore.        |
| [**SetMediaType**](crendererinputpin-setmediatype.md)           | Imposta il tipo di supporto del PIN.                                                        |
| [**Allocatore**](crendererinputpin-allocator.md)                 | Recupera un puntatore all'allocatore di memoria predefinito.                                   |
| Metodi IPin                                                     | Descrizione                                                                            |
| [**QueryId**](crendererinputpin-queryid.md)                     | Recupera un identificatore per il PIN.                                                   |
| [**EndOfStream**](crendererinputpin-endofstream.md)             | Informa il pin che non sono previsti dati aggiuntivi fino a quando non viene emesso un nuovo comando di esecuzione. |
| [**BeginFlush**](crendererinputpin-beginflush.md)               | Informa il pin per iniziare un'operazione di svuotamento.                                            |
| [**EndFlush**](crendererinputpin-endflush.md)                   | Informa il pin per terminare un'operazione di svuotamento.                                              |
| Metodi IMemInputPin                                             | Descrizione                                                                            |
| [**Ricevere**](crendererinputpin-receive.md)                     | Recupera il blocco di dati successivo dal flusso.                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




