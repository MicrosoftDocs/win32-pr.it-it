---
description: Informazioni sul metodo del costruttore CMediaPosition.CMediaPosition (Ctlutil.h). Questo metodo usa i parametri 'pName', 'pUnk' e 'phr'.
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Costruttore CMediaPosition.CMediaPosition (Ctlutil.h)
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
ms.openlocfilehash: 101678ebcb851ef0fcdc8eeaa202435ca80eb796555c81e5e5d95eb4998131c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655262"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a>Costruttore CMediaPosition.CMediaPosition (Ctlutil.h): parametri pName, pUnk e phr

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

*Pname* 
</dt> <dd>

Puntatore al nome dell'oggetto, a scopo di debug. Allocare questo parametro nella memoria statica.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto oppure **NULL** se l'oggetto non è aggregato.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.**

</dd> </dl>

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Ctlutil.h (includere Flussi.h) |
| Libreria| Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




