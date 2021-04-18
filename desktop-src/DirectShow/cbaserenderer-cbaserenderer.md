---
description: Metodo del costruttore.
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Costruttore CBaseRenderer. CBaseRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41f8d7f9681a64f58413aea2fd8717320278f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329402"
---
# <a name="cbaserenderercbaserenderer-constructor"></a>Costruttore CBaseRenderer. CBaseRenderer

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RenderClass* 
</dt> <dd>

Identificatore di classe del renderer.

</dd> <dt>

*pName* 
</dt> <dd>

Puntatore a una stringa che contiene il nome del filtro, a scopo di debug.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione. In caso contrario, impostare questo parametro su **null**.

</dd> <dt>

*PHR* 
</dt> <dd>

Riceve un valore **HRESULT** .

</dd> <dt>

*TimerResolution* 
</dt> <dd>

Risoluzione del timer.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




