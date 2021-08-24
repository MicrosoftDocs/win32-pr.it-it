---
description: Il metodo SetWindowForeground sposta la finestra video in primo piano e, facoltativamente, gli assegna lo stato attivo.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Metodo CBaseControlWindow.SetWindowForeground (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 87a6768c8864de45d50dc630773b756dfad43759adbf4b09ed8070febd37f4d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635471"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a>Metodo CBaseControlWindow.SetWindowForeground

Il `SetWindowForeground` metodo sposta la finestra video in primo piano e, facoltativamente, le assegna lo stato attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Focus* 
</dt> <dd>

Valore che specifica se la finestra video otterrà lo stato attivo. Il valore 1 indica lo stato attivo della finestra e 0 no.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                                           | Descrizione                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NOERROR**</dt> </dl>                | Il metodo è riuscito.<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Lo stato attivo non è uguale a 1 o 0.<br/>                                   |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il filtro corrente non è connesso a un grafo di filtro completo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




