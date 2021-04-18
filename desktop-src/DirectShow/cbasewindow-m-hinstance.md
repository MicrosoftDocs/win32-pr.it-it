---
description: Handle per l'istanza del modulo.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Membro CBaseWindow:: m_hInstance (Winutil. h)'
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
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325784"
---
# <a name="cbasewindowm_hinstance-member"></a>Membro HINSTANCE di CBaseWindow:: m \_

Handle per l'istanza del modulo.

## <a name="syntax"></a>Sintassi


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a>Osservazioni

La funzione del punto di ingresso della DLL imposta una variabile globale con un handle per l'istanza del modulo. La classe **CBaseWindow** archivia questo handle nel metodo del costruttore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




