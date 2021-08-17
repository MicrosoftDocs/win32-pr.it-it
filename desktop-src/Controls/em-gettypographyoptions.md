---
title: EM_GETTYPOGRAPHYOPTIONS messaggio (Richedit.h)
description: Restituisce lo stato corrente delle opzioni tipografiche di un controllo Rich Edit.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- EM_GETTYPOGRAPHYOPTIONS dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d575550e2c239ee5b689deb5874a9803c581151b54100ab227a24d4f29941973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831171"
---
# <a name="em_gettypographyoptions-message"></a>Messaggio \_ EM GETTYPOGRAPHYOPTIONS

Restituisce lo stato corrente delle opzioni tipografiche di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce le opzioni tipografiche correnti. Per un elenco di opzioni, vedere [**EM \_ SETTYPOGRAPHYOPTIONS.**](em-settypographyoptions.md)

## <a name="remarks"></a>Commenti

È possibile attivare l'interruzione di riga avanzata inviando il [**messaggio EM \_ SETTYPOGRAPHYOPTIONS.**](em-settypographyoptions.md) L'interruzione di riga avanzata e normale può anche essere attivata automaticamente dal controllo Rich Edit, se necessario per determinate lingue.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Componente ridistribuibile<br/>          | Rich Edit 3.0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sui controlli Rich Edit](about-rich-edit-controls.md)
</dt> </dl>

 

 





