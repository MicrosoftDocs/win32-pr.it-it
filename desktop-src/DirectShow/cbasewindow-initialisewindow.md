---
description: Il metodo InitialiseWindow Inizializza la finestra.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: Metodo CBaseWindow.InitialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327935"
---
# <a name="cbasewindowinitialisewindow-method"></a>Metodo tialiseWindow CBaseWindow.Ini

Il `InitialiseWindow` metodo inizializza la finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, questo metodo recupera un handle per il contesto di dispositivo (DC) della finestra e crea un controller di dominio di memoria compatibile. Se il valore del flag [**\_ BDoGetDC di CBaseWindow:: m**](cbasewindow-m-bdogetdc.md) è **false**, tuttavia, questo metodo non recupera i contesti di dispositivo. Il controller di dominio della memoria è utile per la selezione di bitmap prima di blitting nella finestra.

Il metodo [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) chiama questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




