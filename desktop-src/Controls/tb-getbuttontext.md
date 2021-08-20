---
title: TB_GETBUTTONTEXT messaggio (Commctrl.h)
description: Recupera il testo visualizzato di un pulsante su una barra degli strumenti.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- TB_GETBUTTONTEXT dei messaggi Windows controlli
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
ms.openlocfilehash: 2ec63815886ecc32f8f0b0759b9f6a8cf847bfe56e6c898fd6e3a3ae8e0f40ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829767"
---
# <a name="tb_getbuttontext-message"></a>TB \_ GETBUTTONTEXT message

Recupera il testo visualizzato di un pulsante su una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del comando del pulsante di cui recuperare il testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer che riceve il testo del pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la lunghezza, in caratteri, della stringa a cui punta *lParam*. La lunghezza non include il carattere Null di terminazione. In caso di esito negativo, il valore restituito è -1.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso non corretto di questo messaggio potrebbe compromettere la sicurezza del programma. Questo messaggio non consente di conoscere le dimensioni del buffer. Se si usa questo messaggio, chiamare prima il messaggio passando **NULL** in *lParam*, in questo modo viene restituito il numero di caratteri, esclusi **i valori NULL** necessari. Chiamare quindi il messaggio una seconda volta per recuperare la stringa. Prima di continuare, vedere Considerazioni sulla [sicurezza: Microsoft Windows Controlli.](sec-comctls.md)

La stringa restituita corrisponde al testo attualmente visualizzato dal pulsante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ GETBUTTONTEXTW** (Unicode) e **TB \_ GETBUTTONTEXTA** (ANSI)<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ GETSTRING**](tb-getstring.md)
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> </dl>

 

 





