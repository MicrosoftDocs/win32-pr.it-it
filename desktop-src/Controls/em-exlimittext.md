---
title: EM_EXLIMITTEXT messaggio (Richedit.h)
description: Imposta un limite massimo per la quantità di testo che l'utente può digitare o incollare in un controllo Rich Edit.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- EM_EXLIMITTEXT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f9879323f3feade3ece536cd130b274b423c98aebedd6b6f5ef1497d995d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915681"
---
# <a name="em_exlimittext-message"></a>MESSAGGIO \_ EM EXLIMITTEXT

Imposta un limite massimo per la quantità di testo che l'utente può digitare o incollare in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica la quantità massima di testo che è possibile immettere. Se questo parametro è zero, viene usato il valore massimo predefinito, ovvero 64.000 caratteri. Un oggetto COM viene conteggiato come carattere singolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il limite di testo impostato dal messaggio **EM \_ EXLIMITTEXT** non limita la quantità di testo che è possibile trasmettere in un controllo Rich Edit usando il messaggio [**\_ STREAMIN EM**](em-streamin.md) con *lParam* impostato su SF \_ TEXT. Tuttavia, limita la quantità di testo che è possibile trasmettere in un controllo Rich Edit usando il messaggio **\_ STREAMIN EM** con *lParam* impostato su \_ SF RTF.

Prima **della chiamata a EM \_ EXLIMITTEXT,** il limite predefinito per la quantità di testo che un utente può immettere è di 32.767 caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ STREAMIN**](em-streamin.md)
</dt> </dl>

 

 





