---
description: Il metodo RefreshDisplayType aggiorna il formato video dell'oggetto in modo che corrisponda alla visualizzazione specificata.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Metodo CImageDisplay. RefreshDisplayType (Winutil. h)
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
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329382"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a>CImageDisplay. RefreshDisplayType, metodo

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

Puntatore a una stringa che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione **ENUMDISPLAYDEVICES** GDI. Per usare il dispositivo di visualizzazione principale, impostare questo parametro su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o se l'operazione ha \_ esito negativo.

## <a name="remarks"></a>Commenti

Questo metodo inizializza il membro di **\_ visualizzazione m** in un tipo video che corrisponde alla modalità di visualizzazione sul dispositivo specificato.

Chiamare questo metodo ogni volta che \_ viene ricevuto un messaggio WM DISPLAYCHANGED o per specificare un dispositivo di visualizzazione secondario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




