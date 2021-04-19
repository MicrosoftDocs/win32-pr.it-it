---
description: Metodo del costruttore.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Costruttore CBaseVideoRenderer. CBaseVideoRenderer (Renbase. h)
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
ms.openlocfilehash: 27ed49be63d9c2c05e12a2ac92ae33f64705460b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328509"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a>Costruttore CBaseVideoRenderer. CBaseVideoRenderer

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

*RenderClass* 
</dt> <dd>

Identificatore di classe per questo renderer.

</dd> <dt>

*pName* 
</dt> <dd>

Puntatore a una descrizione utilizzata a scopo di debug.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntatore all'oggetto proprietario aggregato.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a un valore **HRESULT** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




