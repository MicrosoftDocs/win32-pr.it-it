---
title: EM_FILELINELENGTH messaggio (CommCtrl.h)
description: Recupera la lunghezza, in caratteri, di una riga in un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_FILELINELENGTH di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cb05b0e2acbfb5049eddefab1dad42ecd7b6db234fa4a3c34d4877ed52b007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915541"
---
# <a name="em_filelinelength-message"></a>Messaggio \_ EM FILELINELENGTH

Recupera la lunghezza, in caratteri, di una riga in un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dei caratteri di un carattere nella riga di cui recuperare la lunghezza. Se questo parametro è maggiore del numero di caratteri nel controllo, il valore restituito è zero.

Questo parametro può essere -1. In questo caso, il messaggio restituisce il numero di caratteri non selezionati nelle righe contenenti caratteri selezionati. Ad esempio, se la selezione si estende dal quarto carattere di una riga all'ottavo carattere dalla fine della riga successiva, il valore restituito sarà 10 (tre caratteri nella prima riga e sette nella riga successiva).

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per i controlli di modifica su più righe, il valore restituito è la lunghezza, in **TCHAR** s, della riga specificata dal *parametro wParam,* indipendentemente dalla modalità di visualizzazione delle righe sullo schermo. Non include il carattere di ritorno a capo o avanzamento riga alla fine della riga.

Per i controlli di modifica a riga singola, il valore restituito è la lunghezza, in **TCHAR** s, del testo nel controllo di modifica.

Se *wParam* è maggiore del numero di caratteri nel controllo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Usare il [**messaggio EM \_ FILELINEINDEX**](em-lineindex.md) per recuperare un indice di caratteri per un determinato numero di riga all'interno di un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2019 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ FILELINEINDEX**](em-filelineindex.md)
</dt> </dl>

 

 





