---
title: Sintassi intervallo
description: Rappresenta un valore di intervallo di tempo.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Schema di AD di sintassi intervallo
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b92961deecde7faa879dbbda6bfd24560ad705
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104400954"
---
# <a name="interval-syntax"></a>Sintassi intervallo

Rappresenta un valore di intervallo di tempo. Le unità di tempo effettive dipendono dall'attributo che usa questa sintassi. Questa sintassi è identica alla sintassi [**LargeInteger**](s-largeinteger.md) , ad eccezione del fatto che i valori High e low sono interi senza segno.



| Voce | Valore |
|--------------|------------------------------------------------------------------------------------|
| Nome         | Interval                                                                           |
| ID sintassi    | 2.5.5.16                                                                           |
| ID OM        | 65                                                                                 |
| Tipo MAPI    | \-                                                                                 |
| Tipo di annunci     | ADSTYPE \_ \_ Integer grande                                                            |
| Tipo Variant | \_invio VT                                                                       |
| Tipo SDS     | Oggetto COM di cui è possibile eseguire il cast a un [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger). |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[**LargeInteger**](s-largeinteger.md)
</dt> </dl>

 

 
