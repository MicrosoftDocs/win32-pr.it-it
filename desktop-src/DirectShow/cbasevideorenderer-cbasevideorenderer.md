---
description: Costruttore CBaseVideoRenderer.CBaseVideoRenderer - Metodo costruttore.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Costruttore CBaseVideoRenderer.CBaseVideoRenderer (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec6a5e12d12b12f22cf1089d85ed4c07656da86cda071d8645355890996e2cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954760"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a>Costruttore CBaseVideoRenderer.CBaseVideoRenderer

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Classe RenderClass* 
</dt> <dd>

Identificatore di classe per questo renderer.

</dd> <dt>

*Pname* 
</dt> <dd>

Puntatore a una descrizione utilizzata a scopo di debug.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore all'oggetto proprietario aggregato.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




