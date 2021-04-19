---
description: Il \_ metodo Put WindowStyle imposta gli stili della finestra standard.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: Metodo CBaseControlWindow.put_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333366"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a>CBaseControlWindow. put \_ WindowStyle (metodo)

Il `put_WindowStyle` metodo imposta gli stili della finestra standard.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*WindowStyle* 
</dt> <dd>

Nuovi stili della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Prestare attenzione quando si modificano gli stili della finestra. Nella maggior parte dei casi, un'applicazione deve recuperare lo stile corrente e quindi aggiungere o rimuovere i bit non appropriati. Questa procedura consente di mantenere intatti diversi stili interni della finestra utilizzati da Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




