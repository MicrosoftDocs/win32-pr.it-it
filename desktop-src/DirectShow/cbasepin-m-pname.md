---
description: Nome del PIN.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Membro CBasePin:: m_pName (Amfilter. h)'
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
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331523"
---
# <a name="cbasepinm_pname-member"></a>Membro pName di CBasePin:: m \_

Nome del PIN.

## <a name="syntax"></a>Sintassi


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Osservazioni

Il metodo [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md) restituisce questa stringa come nome del PIN e il metodo [**CBasePin:: QueryId**](cbasepin-queryid.md) lo restituisce come identificatore del PIN. In generale, tuttavia, il nome del PIN e l'identificatore del PIN non devono essere uguali. L'identificatore del PIN viene usato per la persistenza del grafo. Per ulteriori informazioni, vedere [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




