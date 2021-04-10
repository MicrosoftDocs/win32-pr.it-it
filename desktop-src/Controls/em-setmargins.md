---
title: Messaggio EM_SETMARGINS (winuser. h)
description: Imposta le larghezze dei margini sinistro e destro per un controllo di modifica. Il messaggio ridisegnato il controllo in modo da riflettere i nuovi margini. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- Controlli di Windows Message EM_SETMARGINS
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
ms.openlocfilehash: 5c68f3394234a6f86b3c5ff69622b86e61afc556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964393"
---
# <a name="em_setmargins-message"></a>\_Messaggio SEmargini em

Imposta le larghezze dei margini sinistro e destro per un controllo di modifica. Il messaggio ridisegnato il controllo in modo da riflettere i nuovi margini. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Margini da impostare. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <dt>**\_LeftMargin EC**</dt> </dl>    | Imposta il margine sinistro.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <dt>**\_RightMargin EC**</dt> </dl> | Imposta il margine destro.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <dt>**\_USEFONTINFO EC**</dt> </dl> | **Controlli Rich Edit:** Imposta i margini sinistro e destro su una larghezza ridotta calcolata usando le metriche di testo del tipo di carattere corrente del controllo. Se per il controllo non è stato impostato alcun tipo di carattere, i margini vengono impostati su zero. Il parametro *lParam* viene ignorato. <br/> **Controlli di modifica:** Impossibile utilizzare il valore **EC \_ USEFONTINFO** nel parametro *wParam* . Può essere usato solo nel parametro *lParam* .<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la nuova larghezza del margine sinistro, in pixel. Questo valore viene ignorato se *wParam* non include la **\_ LeftMargin EC**.

**Modificare i controlli e rich edit 3,0 e versioni successive:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) può specificare il valore **EC \_ USEFONTINFO** per impostare il margine sinistro su una larghezza ridotta calcolata usando le metriche di testo del tipo di carattere corrente del controllo. Se per il controllo non è stato impostato alcun carattere, il margine è impostato su zero.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la nuova larghezza del margine destro, in pixel. Questo valore viene ignorato se *wParam* non include la **\_ RightMargin EC**.

**Modificare i controlli e rich edit 3,0 e versioni successive:** [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) può specificare il valore **EC \_ USEFONTINFO** per impostare il margine destro su una larghezza ridotta calcolata usando le metriche di testo del tipo di carattere corrente del controllo. Se per il controllo non è stato impostato alcun carattere, il margine è impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

**Controlli di modifica:** Non è possibile usare **EC \_ USEFONTINFO** nel parametro *wParam* , ma è possibile usarlo nel parametro *lParam* .

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Tutte le versioni Rich Edit supportano l'uso di **EC \_ USEFONTINFO** nel parametro *wParam* . Tuttavia, solo Microsoft Rich Edit 3,0 e versioni successive supportano l'uso di **EC \_ USEFONTINFO** nel parametro *lParam* . Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETmargini em**](em-getmargins.md)
</dt> </dl>

 

