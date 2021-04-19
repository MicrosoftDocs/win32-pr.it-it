---
description: Il metodo SetWindowForeground sposta la finestra video in primo piano e, facoltativamente, lo rende attivo.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Metodo CBaseControlWindow. SetWindowForeground (Ctlutil. h)
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
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333362"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a>CBaseControlWindow. SetWindowForeground, metodo

Il `SetWindowForeground` metodo sposta la finestra del video in primo piano e, facoltativamente, lo rende attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Lo stato attivo* 
</dt> <dd>

Valore che specifica se la finestra video otterrà lo stato attivo. Il valore 1 indica lo stato attivo della finestra e 0 non lo è.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                                           | Descrizione                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NOERROR**</dt> </dl>                | Il metodo è riuscito.<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Lo stato attivo non è uguale a 1 o 0.<br/>                                   |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il filtro corrente non è connesso a un grafico di filtro completo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




