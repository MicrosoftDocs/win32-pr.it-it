---
description: Il \_ metodo get Caption Recupera la didascalia della finestra corrente.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: Metodo CBaseControlWindow.get_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326670"
---
# <a name="cbasecontrolwindowget_caption-method"></a>CBaseControlWindow. Get ( \_ Metodo Caption)

Il `get_Caption` metodo recupera la didascalia della finestra corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pstrCaption* 
</dt> <dd>

Puntatore alla didascalia della finestra corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Per la maggior parte delle finestre di primo livello in un desktop basato su Windows è associato un titolo (didascalia). Questa proprietà può essere sottoposta a query e impostata tramite l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Qualsiasi set di didascalie sarà visibile solo se nella finestra è \_ applicato lo stile di didascalia WS. In caso contrario, è comunque possibile impostare (e recuperare) la didascalia, anche se non sarà visibile all'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




