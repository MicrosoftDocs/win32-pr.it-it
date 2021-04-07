---
title: Messaggio TB_SETBUTTONINFO (COMmctrl. h)
description: Imposta le informazioni per un pulsante esistente in una barra degli strumenti.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- Controlli di Windows Message TB_SETBUTTONINFO
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
ms.openlocfilehash: 70612a90f245a25dde5a487917d7c3b669424ea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874490"
---
# <a name="tb_setbuttoninfo-message"></a>TB \_ SETBUTTONINFO messaggio

Imposta le informazioni per un pulsante esistente in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del pulsante.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) che contiene le informazioni sul pulsante nuovo. Prima di inviare questo messaggio, è necessario compilare i membri **cbSize** e **dwMask** di questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Il testo viene generalmente assegnato ai pulsanti quando vengono aggiunti a una barra degli strumenti specificando l'indice di una stringa nel pool di stringhe della barra degli strumenti. Se si usa un **\_ SETBUTTONINFO TB** per assegnare nuovo testo a un pulsante, il testo verrà sostituito in modo permanente dal pool di stringhe. È possibile modificare il testo richiamando **TB \_ SETBUTTONINFO** , ma non è possibile riassegnare la stringa dal pool di stringhe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ SETBUTTONINFOW** (Unicode) e **TB \_ SETBUTTONINFOA** (ANSI)<br/>         |



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

[**TB \_ GETstring**](tb-getstring.md)
</dt> <dt>

[**TB \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

 





