---
description: Il metodo put \_ WindowStyleEx imposta gli stili di finestra estesi.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: CBaseControlWindow.put_WindowStyleEx metodo (Ctlutil.h)
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
ms.openlocfilehash: 48bdfba6b388d4595af3ba886ed97567c12f080953e238c03d8a5fb36f7a6ce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635541"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a>Metodo CBaseControlWindow.put \_ WindowStyleEx

Il `put_WindowStyleEx` metodo imposta gli stili di finestra estesi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*WindowStyleEx* \[ Pollici\]
</dt> <dd>

Valore che specifica lo stile della finestra del controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR.

## <a name="remarks"></a>Commenti

Questo metodo usa stili di finestra estesi. Per un elenco completo degli stili di finestra estesi, vedere la funzione Microsoft Win32 **CreateWindowEx.** Per modificare lo stile della finestra, recuperare lo stile della finestra corrente e quindi aggiungere o rimuovere i campi di bit necessari.

Non usare gli stili di finestra seguenti perché non vengono convalidati.

-   WS \_ DISABILITATO
-   WS \_ HSCROLL
-   WS \_ SIMBOLICO
-   WS \_ MAXIMIZE
-   WS \_ MINIMIZE
-   WS \_ VSCROLL

Con alcune eccezioni (qui segnalate), i flag accettabili sono gli stessi consentiti dalla funzione **Win32 CreateWindow.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




