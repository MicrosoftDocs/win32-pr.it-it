---
description: Valore booleano che indica se il filtro sta attualmente eliminando i frame. Se questo valore è TRUE, il filtro continua a rilasciare i frame fino a raggiungere il fotogramma chiave successivo o fino a quando non riceve 30 frame Delta in una riga senza un fotogramma chiave.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'Membro CVideoTransformFilter:: m_bSkipping (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7beb4073052149e246a55ffbb1ff057e836704c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330194"
---
# <a name="cvideotransformfilterm_bskipping-member"></a>Membro bSkipping di CVideoTransformFilter:: m \_

Valore booleano che indica se il filtro sta attualmente eliminando i frame. Se questo valore è **true**, il filtro continua a rilasciare i frame fino a raggiungere il fotogramma chiave successivo o fino a quando non riceve 30 frame Delta in una riga senza un fotogramma chiave.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




