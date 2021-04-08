---
title: Messaggio di EM_GETZOOM (RichEdit. h)
description: Ottiene la percentuale di zoom corrente. Il razionamento dello zoom è sempre compreso tra 1/64 e 64. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- Controlli di Windows Message EM_GETZOOM
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740295"
---
# <a name="em_getzoom-message"></a>\_Messaggio GETZOOM em

Ottiene la percentuale di zoom corrente per un controllo di modifica su più righe o un controllo Rich Edit. Il razionamento dello zoom è sempre compreso tra 1/64 e 64.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Riceve il numeratore del rapporto di zoom.

</dd> <dt>

*lParam* 
</dt> <dd>

Riceve il denominatore del rapporto di zoom.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il messaggio restituisce **true** se il messaggio viene elaborato, che sarà se *wParam* e *lParam* non sono **null**.

## <a name="remarks"></a>Commenti

**Modifica:** Supportato in Windows 10 1809 e versioni successive. Il controllo di modifica deve avere il set di stili estesi **es \_ ex \_ Zoom** , perché questo messaggio abbia effetto, vedere [modificare gli stili estesi del controllo](edit-control-window-extended-styles.md). Per informazioni sul controllo di modifica, vedere [modificare i controlli](edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h/COMmctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Zoom em**](em-setzoom.md)
</dt> </dl>

 

 





