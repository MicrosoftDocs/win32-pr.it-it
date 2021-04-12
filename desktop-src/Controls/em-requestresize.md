---
title: Messaggio di EM_REQUESTRESIZE (RichEdit. h)
description: Impone a un controllo Rich Edit di inviare un \_ codice di notifica en REQUESTRESIZE alla finestra padre.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- Controlli di Windows Message EM_REQUESTRESIZE
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225237"
---
# <a name="em_requestresize-message"></a>\_Messaggio REQUESTRESIZE em

Impone a un controllo Rich Edit di inviare un codice di notifica [**en \_ REQUESTRESIZE**](en-requestresize.md) alla finestra padre.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Questo messaggio è utile durante l'elaborazione di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) per l'elemento padre di un controllo Rich Edit senza fondo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EN \_ REQUESTRESIZE**](en-requestresize.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_dimensioni WM**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

