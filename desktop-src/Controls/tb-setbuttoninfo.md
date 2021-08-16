---
title: TB_SETBUTTONINFO messaggio (Commctrl.h)
description: Imposta le informazioni per un pulsante esistente in una barra degli strumenti.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- TB_SETBUTTONINFO dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e9fa1da0f9556c025b83ac2b3345680fe11dac0dd15e202ed7336cacfe511e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829625"
---
# <a name="tb_setbuttoninfo-message"></a>TB \_ SETBUTTONINFO message

Imposta le informazioni per un pulsante esistente in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del pulsante.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) che contiene le informazioni sul nuovo pulsante. I **membri cbSize** **e dwMask** di questa struttura devono essere compilati prima di inviare questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Il testo viene in genere assegnato ai pulsanti quando vengono aggiunti a una barra degli strumenti specificando l'indice di una stringa nel pool di stringhe della barra degli strumenti. Se si usa **\_ setBUTTONINFO da TB** per assegnare nuovo testo a un pulsante, verrà eseguito l'override permanente del testo dal pool di stringhe. È possibile modificare il testo chiamando **di nuovo \_ TB SETBUTTONINFO,** ma non è possibile riassegnare la stringa dal pool di stringhe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ SETBUTTONINFOW** (Unicode) e **\_ TB SETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TB \_ ADDBUTTONS**](tb-addbuttons.md)
</dt> <dt>

[**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> <dt>

[**TB \_ GETSTRING**](tb-getstring.md)
</dt> <dt>

[**TB \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

 





