---
description: Il metodo RefreshDisplayType aggiorna il formato video dell'oggetto in modo che corrisponda alla visualizzazione specificata.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Metodo CImageDisplay.RefreshDisplayType (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9184d5e8a0e0ad6c0242ec1dc4b7590f1bc0d39a0a9cd6a09b2676563a2796e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055471"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a>Metodo CImageDisplay.RefreshDisplayType

Il `RefreshDisplayType` metodo aggiorna il formato video dell'oggetto in modo che corrisponda alla visualizzazione specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szDeviceName* 
</dt> <dd>

Puntatore a una stringa che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione **GDI EnumDisplayDevices.** Per usare il dispositivo di visualizzazione principale, impostare questo parametro su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo oppure E FAIL in caso di esito \_ negativo.

## <a name="remarks"></a>Commenti

Questo metodo inizializza il **membro \_ m Display** su un tipo di video che corrisponde alla modalità di visualizzazione nel dispositivo specificato.

Chiamare questo metodo ogni volta che viene ricevuto un messaggio WM \_ DISPLAYCHANGED o per specificare un dispositivo di visualizzazione secondario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




