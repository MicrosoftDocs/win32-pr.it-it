---
description: Handle per l'istanza del modulo.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: Membro CBaseWindow::m_hInstance (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddf1da2d7f947bbaed9972a40a20497a81f84ebda68dba31cd5518b64f6e8434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016529"
---
# <a name="cbasewindowm_hinstance-member"></a>Membro CBaseWindow::m \_ hInstance

Handle per l'istanza del modulo.

## <a name="syntax"></a>Sintassi


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a>Osservazioni

La funzione del punto di ingresso DLL imposta una variabile globale con un handle per l'istanza del modulo. La **classe CBaseWindow** archivia questo handle nel metodo del costruttore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




