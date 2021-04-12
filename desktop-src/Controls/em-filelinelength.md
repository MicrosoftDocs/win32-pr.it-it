---
title: Messaggio EM_FILELINELENGTH (CommCtrl. h)
description: Recupera la lunghezza, in caratteri, di una riga in un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Controlli di Windows Message EM_FILELINELENGTH
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
ms.openlocfilehash: 4aa50f4d9b49253a558095be78e0e781d7d4c7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517985"
---
# <a name="em_filelinelength-message"></a>\_Messaggio FILELINELENGTH em

Recupera la lunghezza, in caratteri, di una riga in un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.

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

Per i controlli di modifica su più righe, il valore restituito è la lunghezza, in **TCHAR** s, della riga specificata dal parametro *wParam* , indipendentemente dalla modalità di visualizzazione delle linee sullo schermo. Non include il carattere di ritorno a capo o di avanzamento riga alla fine della riga.

Per i controlli di modifica a riga singola, il valore restituito è la lunghezza, in **TCHAR** s, del testo nel controllo di modifica.

Se *wParam* è maggiore del numero di caratteri nel controllo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Usare il [**messaggio \_ FILELINEINDEX em**](em-lineindex.md) per recuperare un indice dei caratteri per un numero di riga specificato all'interno di un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10, 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2019\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_FILELINEINDEX em**](em-filelineindex.md)
</dt> </dl>

 

 





