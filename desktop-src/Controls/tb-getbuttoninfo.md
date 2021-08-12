---
title: TB_GETBUTTONINFO messaggio (Commctrl.h)
description: Recupera informazioni estese per un pulsante in una barra degli strumenti.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- TB_GETBUTTONINFO di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 457b8ca82d570b9d6c55cf97392803fce9a81cbe1d5db8122fcdaa975dd99d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669934"
---
# <a name="tb_getbuttoninfo-message"></a>MESSAGGIO \_ GETBUTTONINFO DA TB

Recupera informazioni estese per un pulsante in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del comando del pulsante.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) che riceve le informazioni sul pulsante. I **membri cbSize** **e dwMask** di questa struttura devono essere compilati prima di inviare questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice in base zero del pulsante oppure -1 se si verifica un errore.

## <a name="remarks"></a>Commenti

Quando si usa [**TB \_ ADDBUTTONS**](tb-addbuttons.md) o [**TB \_ INSERTBUTTON**](tb-insertbutton.md) per posizionare i pulsanti sulla barra degli strumenti, il testo del pulsante viene in genere specificato dall'indice del pool di stringhe. **TB \_ GETBUTTONINFO non** recupererà questa stringa. Per usare **TB \_ GETBUTTONINFO per** recuperare il testo del pulsante, è innanzitutto necessario impostare la stringa di testo con TB [**\_ SETBUTTONINFO**](tb-setbuttoninfo.md). Dopo aver impostato il testo del pulsante con **TB \_ SETBUTTONINFO,** non è più possibile usare l'indice del pool di stringhe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ GETBUTTONINFOW** (Unicode) e **\_ TB GETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> </dl>

 

 





