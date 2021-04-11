---
title: Messaggio EM_SETREADONLY (winuser. h)
description: Imposta o rimuove lo stile di sola lettura \_ di un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Controlli di Windows Message EM_SETREADONLY
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119659"
---
# <a name="em_setreadonly-message"></a>Messaggio di sola \_ lettura em

Imposta o rimuove lo stile di sola lettura di [**un \_**](edit-control-styles.md)controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se impostare o rimuovere lo stile di sola [**\_ lettura di es**](edit-control-styles.md) . Il valore **true** imposta lo stile di sola **\_ lettura di es** . il valore **false** rimuove lo stile di sola **\_ lettura** .

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è diverso da zero.

Se l'operazione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Quando un controllo di modifica ha lo stile di sola [**\_ lettura**](edit-control-styles.md) , l'utente non può modificare il testo nel controllo di modifica.

Per determinare se un controllo di modifica ha lo stile di sola [**\_ lettura di es**](edit-control-styles.md) , usare la funzione [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con il \_ flag di stile GWL.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

