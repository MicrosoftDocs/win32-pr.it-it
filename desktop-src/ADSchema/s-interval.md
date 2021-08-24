---
title: Sintassi dell'intervallo
description: Rappresenta un valore di intervallo di tempo.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Schema AD della sintassi dell'intervallo
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e088c8347ff12172cb87c521e049e2646a0711e1eaedf805887b6988af1e284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580291"
---
# <a name="interval-syntax"></a>Sintassi dell'intervallo

Rappresenta un valore di intervallo di tempo. Le unità di tempo effettive dipendono dall'attributo che usa questa sintassi. Questa sintassi è identica alla [**sintassi LargeInteger,**](s-largeinteger.md) ad eccezione del fatto che i valori alti e bassi sono interi senza segno.



| Voce | Valore |
|--------------|------------------------------------------------------------------------------------|
| Nome         | Intervallo                                                                           |
| ID sintassi    | 2.5.5.16                                                                           |
| OM ID        | 65                                                                                 |
| Tipo MAPI    | \-                                                                                 |
| Tipo di ADS     | ADSTYPE \_ LARGE \_ INTEGER                                                            |
| Tipo variant | VT \_ DISPATCH                                                                       |
| Tipo SDS     | Oggetto COM di cui è possibile eseguire il cast in [**un oggetto IADsLargeInteger.**](/windows/desktop/api/iads/nn-iads-iadslargeinteger) |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[**LargeInteger**](s-largeinteger.md)
</dt> </dl>

 

 
