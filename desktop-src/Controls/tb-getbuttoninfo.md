---
title: Messaggio TB_GETBUTTONINFO (COMmctrl. h)
description: Recupera le informazioni estese per un pulsante in una barra degli strumenti.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- Controlli di Windows Message TB_GETBUTTONINFO
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
ms.openlocfilehash: 74c7f6a8d1d36737d09cfb4d307129200a51180c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121718"
---
# <a name="tb_getbuttoninfo-message"></a>TB \_ GETBUTTONINFO messaggio

Recupera le informazioni estese per un pulsante in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del comando del pulsante.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) che riceve le informazioni sul pulsante. Prima di inviare questo messaggio, è necessario compilare i membri **cbSize** e **dwMask** di questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice in base zero del pulsante oppure-1 se si verifica un errore.

## <a name="remarks"></a>Commenti

Quando si usa [**TB \_ ADDBUTTONS**](tb-addbuttons.md) o [**TB \_ INSERTBUTTON**](tb-insertbutton.md) per posizionare i pulsanti sulla barra degli strumenti, il testo del pulsante viene comunemente specificato dall'indice del pool di stringhe. **TB \_ GETBUTTONINFO** non recupererà questa stringa. Per usare **TB \_ GETBUTTONINFO** per recuperare il testo del pulsante, è necessario innanzitutto impostare la stringa di testo con [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md). Dopo aver impostato il testo del pulsante con **TB \_ SETBUTTONINFO**, non è più possibile usare l'indice del pool di stringhe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ GETBUTTONINFOW** (Unicode) e **TB \_ GETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> </dl>

 

 





