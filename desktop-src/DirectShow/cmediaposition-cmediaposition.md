---
description: Informazioni sul metodo del costruttore CMediaPosition. CMediaPosition (Ctlutil. h). Questo metodo usa i parametri "pName" e "pUnk".
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Costruttore CMediaPosition. CMediaPosition (Ctlutil. h)-pName, parametri pUnk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323785"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a>Costruttore CMediaPosition. CMediaPosition (Ctlutil. h)-pName, parametri pUnk

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* 
</dt> <dd>

Puntatore al nome dell'oggetto, a scopo di debug. Allocare questo parametro nella memoria statica.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto o **null** se l'oggetto non è aggregato.

</dd> </dl>

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Ctlutil. h (include Streams. h) |
| Libreria| Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




