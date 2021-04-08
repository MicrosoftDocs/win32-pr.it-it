---
title: Codice di notifica EN_OBJECTPOSITIONS (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit quando il controllo legge negli oggetti. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- Controlli di Windows per il codice di notifica EN_OBJECTPOSITIONS
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873906"
---
# <a name="en_objectpositions-notification-code"></a>\_Codice di notifica en OBJECTPOSITIONS

Notifica alla finestra padre di un controllo Rich Edit quando il controllo legge negli oggetti. Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Struttura [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero per continuare l'operazione di **lettura** .

Restituisce un valore diverso da zero per arrestare l'operazione di **lettura** .

## <a name="remarks"></a>Commenti

Per ricevere un \_ codice di notifica en OBJECTPOSITIONS, specificare il flag [**ENM \_ OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio \_ SETEVENTMASK em**](em-seteventmask.md) .

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

[**\_SETEVENTMASK em**](em-seteventmask.md)
</dt> <dt>

[**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[**\_notifica WM**](wm-notify.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

