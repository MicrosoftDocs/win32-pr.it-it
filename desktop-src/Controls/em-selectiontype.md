---
title: Messaggio di EM_SELECTIONTYPE (RichEdit. h)
description: Determina il tipo di selezione per un controllo Rich Edit.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- Controlli di Windows Message EM_SELECTIONTYPE
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518682"
---
# <a name="em_selectiontype-message"></a>\_Messaggio SELECTIONTYPE em

Determina il tipo di selezione per un controllo Rich Edit.

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

Se la selezione è vuota, il valore restituito è SEL \_ Empty.

Se la selezione non è vuota, il valore restituito è un set di flag che contengono uno o più dei valori seguenti.



| Codice restituito                                                                                     | Descrizione                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_testo SEL**</dt> </dl>        | Text.<br/>                            |
| <dl> <dt>**\_oggetto SEL**</dt> </dl>      | Almeno un oggetto COM.<br/>         |
| <dl> <dt>**SEL \_ MULTIchar**</dt> </dl>   | Più di un carattere di testo.<br/> |
| <dl> <dt>**SEL \_ MULTIoggetto**</dt> </dl> | Più di un oggetto COM.<br/>        |



 

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

[**\_dimensioni WM**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

