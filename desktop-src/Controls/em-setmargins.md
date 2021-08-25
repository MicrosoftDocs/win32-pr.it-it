---
title: EM_SETMARGINS messaggio (Winuser.h)
description: Imposta le larghezze dei margini sinistro e destro per un controllo di modifica. Il messaggio ridisegna il controllo in modo da riflettere i nuovi margini. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- EM_SETMARGINS controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396bba6dda0f6dbd132b9f67fa5a1ef012758bbf7cf8fa9517b656dcf164c94c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048361"
---
# <a name="em_setmargins-message"></a>Messaggio \_ EM SETMARGINS

Imposta le larghezze dei margini sinistro e destro per un controllo di modifica. Il messaggio ridisegna il controllo in modo da riflettere i nuovi margini. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Margini da impostare. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <dt>**EC \_ LEFTMARGIN**</dt> </dl>    | Imposta il margine sinistro.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <dt>**EC \_ RIGHTMARGIN**</dt> </dl> | Imposta il margine destro.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <dt>**EC \_ USEFONTINFO**</dt> </dl> | **Controlli Rich Edit:** Imposta i margini sinistro e destro su una larghezza ridotta calcolata usando le metriche del testo del tipo di carattere corrente del controllo. Se per il controllo non è stato impostato alcun tipo di carattere, i margini vengono impostati su zero. Il *parametro lParam* viene ignorato. <br/> **Controlli di modifica:** Il **valore \_ EC USEFONTINFO** non può essere usato nel *parametro wParam.* Può essere usato solo nel *parametro lParam.*<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LoWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la nuova larghezza del margine sinistro, in pixel. Questo valore viene ignorato *se wParam* non include **EC \_ LEFTMARGIN.**

**Controlli di modifica e Rich Edit 3.0 e versioni successive:** LoWORD [**può**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specificare il valore **EC \_ USEFONTINFO** per impostare il margine sinistro su una larghezza ridotta calcolata usando le metriche del testo del tipo di carattere corrente del controllo. Se per il controllo non è stato impostato alcun tipo di carattere, il margine viene impostato su zero.

La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la nuova larghezza del margine destro, in pixel. Questo valore viene ignorato *se wParam* non include **EC \_ RIGHTMARGIN**.

**Controlli di modifica e Rich Edit 3.0 e versioni successive:** HiWORD [**può**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specificare il valore **EC \_ USEFONTINFO** per impostare il margine destro su una larghezza ridotta calcolata usando le metriche del testo del tipo di carattere corrente del controllo. Se per il controllo non è stato impostato alcun tipo di carattere, il margine viene impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

**Controlli di modifica:** Non è possibile **usare EC \_ USEFONTINFO** nel *parametro wParam,* ma è possibile usarlo nel *parametro lParam.*

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Tutte le versioni rich edit supportano **l'uso di EC \_ USEFONTINFO** nel *parametro wParam.* Tuttavia, solo Microsoft Rich Edit 3.0 e versioni successive supportano l'uso di **EC \_ USEFONTINFO** nel *parametro lParam.* Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETMARGINS**](em-getmargins.md)
</dt> </dl>

 

