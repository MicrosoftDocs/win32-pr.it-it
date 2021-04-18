---
description: Il \_ metodo Put Caption Imposta il titolo o la didascalia della finestra.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: Metodo CBaseControlWindow.put_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328352"
---
# <a name="cbasecontrolwindowput_caption-method"></a>CBaseControlWindow. Put, \_ Metodo didascalia

Il `put_Caption` metodo imposta il titolo o la didascalia della finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strCaption* 
</dt> <dd>

Nuova didascalia della finestra.

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

 

 




