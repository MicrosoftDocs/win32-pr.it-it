---
description: Informazioni sul metodo del costruttore CMediaPosition. CMediaPosition (Ctlutil. h). Questo metodo usa i parametri ' pName ',' pUnk ' è PHR '.
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Costruttore CMediaPosition. CMediaPosition (Ctlutil. h)
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
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323772"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a>Costruttore CMediaPosition. CMediaPosition (Ctlutil. h)-pName, pUnk, PHR parametri

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
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

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a un valore **HRESULT** .

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

 

 




