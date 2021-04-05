---
title: Messaggio EM_LINELENGTH (winuser. h)
description: Recupera la lunghezza, in caratteri, di una riga in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Controlli di Windows Message EM_LINELENGTH
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874273"
---
# <a name="em_linelength-message"></a>\_Messaggio LINELENGTH em

Recupera la lunghezza, in caratteri, di una riga in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dei caratteri di un carattere nella riga di cui è necessario recuperare la lunghezza. Se questo parametro è maggiore del numero di caratteri nel controllo, il valore restituito è zero.

Questo parametro può essere-1. In questo caso, il messaggio restituisce il numero di caratteri non selezionati nelle righe contenenti caratteri selezionati. Se, ad esempio, la selezione è stata estesa dal quarto carattere di una riga attraverso l'ottavo carattere alla fine della riga successiva, il valore restituito sarà 10 (tre caratteri nella prima riga e sette nella successiva).

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per i controlli di modifica su più righe, il valore restituito è la lunghezza, in **TCHAR** s, della riga specificata dal parametro *wParam* . Per testo ANSI, indica il numero di byte; per il testo Unicode, indica il numero di caratteri. Non include il carattere di ritorno a capo alla fine della riga.

Per i controlli di modifica a riga singola, il valore restituito è la lunghezza, in **TCHAR** s, del testo nel controllo di modifica.

Se *wParam* è maggiore del numero di caratteri nel controllo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Usare il [**messaggio \_ LINEINDEX em**](em-lineindex.md) per recuperare un indice dei caratteri per un numero di riga specificato all'interno di un controllo di modifica su più righe.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_LINEINDEX em**](em-lineindex.md)
</dt> </dl>

 

 





