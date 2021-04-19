---
description: Il \_ metodo Put WindowStyleEx imposta gli stili della finestra estesa.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: Metodo CBaseControlWindow.put_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333365"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a>CBaseControlWindow. put \_ WindowStyleEx (metodo)

Il `put_WindowStyleEx` metodo imposta gli stili della finestra estesa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*WindowStyleEx* \[ in\]
</dt> <dd>

Valore che specifica lo stile della finestra del controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR.

## <a name="remarks"></a>Commenti

Questo metodo utilizza gli stili estesi della finestra. Per un elenco completo degli stili della finestra estesa, vedere la funzione **CreateWindowEx** di Microsoft Win32. Per modificare lo stile della finestra, recuperare lo stile della finestra corrente, quindi aggiungere o rimuovere i campi di bit necessari.

Non usare gli stili della finestra seguenti perché non vengono convalidati.

-   WS \_ disabilitato
-   WS \_ HSCROLL
-   \_icona WS
-   WS- \_ Ingrandisc
-   WS- \_ riduzione a icona
-   WS \_ VSCROLL

Con alcune eccezioni (indicate qui), i flag accettabili sono gli stessi di quelli consentiti dalla funzione Win32 **CreateWindow** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




