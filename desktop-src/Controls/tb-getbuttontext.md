---
title: Messaggio TB_GETBUTTONTEXT (COMmctrl. h)
description: Recupera il testo visualizzato di un pulsante su una barra degli strumenti.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- Controlli di Windows Message TB_GETBUTTONTEXT
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac0b238574cc136f41959b57f3f0e1ec13e3ea1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120106"
---
# <a name="tb_getbuttontext-message"></a>TB \_ GETBUTTONTEXT messaggio

Recupera il testo visualizzato di un pulsante su una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del comando del pulsante di cui è necessario recuperare il testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer che riceve il testo del pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la lunghezza, in caratteri, della stringa a cui punta *lParam*. La lunghezza non include il carattere null di terminazione. Se ha esito negativo, il valore restituito è-1.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'utilizzo errato di questo messaggio potrebbe compromettere la sicurezza del programma. Questo messaggio non fornisce un modo per stabilire le dimensioni del buffer. Se si utilizza questo messaggio, chiamare prima il messaggio passando **null** in *lParam*, viene restituito il numero di caratteri, esclusi i **valori null** richiesti. Chiamare quindi il messaggio una seconda volta per recuperare la stringa. Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .

La stringa restituita corrisponde al testo attualmente visualizzato dal pulsante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ GETBUTTONTEXTW** (Unicode) e **TB \_ GETBUTTONTEXTA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ GETstring**](tb-getstring.md)
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> </dl>

 

 





