---
description: Nome del pin.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: Membro CBasePin::m_pName (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: d118ed76650b9ea580c0143ff4334a480d110c4a9d9531a23dda60c05c614630
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052681"
---
# <a name="cbasepinm_pname-member"></a>Membro CBasePin::m \_ pName

Nome del pin.

## <a name="syntax"></a>Sintassi


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Osservazioni

Il [**metodo CBasePin::QueryPinInfo**](cbasepin-querypininfo.md) restituisce questa stringa come nome del pin e il metodo [**CBasePin::QueryId**](cbasepin-queryid.md) la restituisce come identificatore pin. In generale, tuttavia, il nome del pin e l'identificatore pin non devono essere uguali. L'identificatore pin viene usato per la persistenza del grafico. Per altre informazioni, vedere [**IBaseFilter::FindPin.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




