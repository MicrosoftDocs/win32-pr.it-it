---
title: Metodo ID2D1CommandSink1 SetPrimitiveBlend1
description: Imposta una nuova modalità di Blend primitiva.
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- Direct2D metodo SetPrimitiveBlend1
- Metodo SetPrimitiveBlend1 Direct2D, interfaccia ID2D1CommandSink1
- Interfaccia Direct2D di ID2D1CommandSink1, metodo SetPrimitiveBlend1
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119651"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a>Metodo ID2D1CommandSink1:: SetPrimitiveBlend1

Imposta una nuova modalità di Blend primitiva.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*primitiveBlend* 
</dt> <dd>

Tipo: **[ **d2d1 \_ primitive \_ Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**

Blend primitiva che si applicherà alle primitive successive.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se il metodo ha esito positivo, restituisce **S \_ OK**. Se ha esito negativo, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

### <a name="blend-modes"></a>Modalità di Blend

Per il rendering con alias (ad eccezione della modalità MIN), il valore di output O viene calcolato tramite l'interpolazione lineare del valore *Blend (S, D)* con il valore del pixel di destinazione, in base alla quantità che la primitiva copre il pixel di destinazione.

La tabella seguente mostra le modalità di Blend primitive per la fusione con alias e con aliasing. Le equazioni elencate nella tabella utilizzano questi elementi:

-   O = output
-   S = origine
-   SA = Alpha di origine
-   D = destinazione
-   DA = Alpha di destinazione
-   C = copertura pixel



| Modalità di Blend primitiva                 | Fusione con alias                            | Blending con anti-aliasing            | Descrizione                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ \_ origine Blend primitiva \_ \_ | O = (S + (1 SA) \* D) \* C + D \* (1 C) | O = S \* C + D \* (1 SA \* c)   | Modalità di Blend di origine/destinazione standard.                                                                         |
| \_Copia di \_ Blend PRIMItiva d2d1 \_         | O = S \* C + D \* (1 C)                   | O = S \* C + D \* (1 C)       | L'origine viene copiata nella destinazione. i pixel di destinazione vengono ignorati.                                             |
| \_Min Blend primitiva d2d1 \_ \_          | O = min (S + 1-SA, D)                        | O = min (S \* c + 1 SA \* c, D) | I valori pixel risultanti usano il minimo dei valori di pixel di origine e di destinazione. Disponibile in Windows 8 e versioni successive. |
| \_Aggiunta d2d1 primitive \_ Blend \_          | O = (S + D) \* C + d \* (1 C)             | O = S \* C + D                  | I valori pixel risultanti sono la somma dei valori dei pixel di origine e di destinazione. Disponibile in Windows 8 e versioni successive.     |



 

![illustrazione delle modalità di Blend primitive Direct2D con opacità e sfondi diversi.](images/primblenddemo.png)

Illustrazione delle modalità di Blend primitive con opacità e sfondi diversi.

La Blend primitiva verrà applicata a tutte le primitive disegnate nel contesto, a meno che non venga sottoposto a override con il parametro *compositeMode* nell'API [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) .

La Blend primitiva si applica all'interno di qualsiasi primitiva disegnata nel contesto. Nel caso di [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), questo sarà implicito nel rettangolo dell'immagine, nell'offset e nella trasformazione globale.

Se la Blend primitiva è un valore diverso da **d2d1 \_ primitive \_ Blend \_** , il rendering ClearType verrà disattivato. Se l'applicazione forza in modo esplicito il rendering ClearType in queste modalità, il contesto di disegno verrà inserito in uno stato di errore. \_ \_ Lo stato D2DERR errato verrà restituito da [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1CommandSink1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

