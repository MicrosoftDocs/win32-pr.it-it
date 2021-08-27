---
description: Il metodo InitialiseWindow inizializza la finestra.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Inimetodo tialiseWindow (Winutil.h)
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
ms.openlocfilehash: f260f60111f715bfce357e264b65bb4b821c5ca890d39d4d54e7269a191df303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954660"
---
# <a name="cbasewindowinitialisewindow-method"></a>CBaseWindow.Inimetodo tialiseWindow

Il `InitialiseWindow` metodo inizializza la finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle per la finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, questo metodo recupera un handle per il contesto di dispositivo della finestra e crea un controller di dominio di memoria compatibile. Se il valore del flag [**\_ BDoGetDC di CBaseWindow::m**](cbasewindow-m-bdogetdc.md) è **FALSE,** tuttavia, questo metodo non recupera i contesti di dispositivo. Il controller di dominio di memoria è utile per selezionare bitmap prima di eseguire il blitting nella finestra.

Il [**metodo CBaseWindow::D oCreateWindow**](cbasewindow-docreatewindow.md) chiama questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




