---
title: Messaggio EM_LINEFROMCHAR (winuser. h)
description: Ottiene l'indice della riga che contiene l'indice del carattere specificato in un controllo di modifica su più righe.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Controlli di Windows Message EM_LINEFROMCHAR
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119479"
---
# <a name="em_linefromchar-message"></a>\_Messaggio LINEFROMCHAR em

Ottiene l'indice della riga che contiene l'indice del carattere specificato in un controllo di modifica su più righe. Un indice dei caratteri è l'indice in base zero del carattere a partire dall'inizio del controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dei caratteri del carattere contenuto nella riga di cui è necessario recuperare il numero. Se questo parametro è-1, **em \_ LINEFROMCHAR** Recupera il numero di riga della riga corrente (la riga contenente il punto di inserimento) o, se è presente una selezione, il numero di riga della riga contenente l'inizio della selezione.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero di riga in base zero della riga che contiene l'indice dei caratteri specificato da *wParam*.

## <a name="remarks"></a>Commenti

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Se l'indice dei caratteri è maggiore di 64.000, utilizzare il messaggio [**\_ EXLINEFROMCHAR em**](em-exlinefromchar.md) . Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_EXLINEFROMCHAR em**](em-exlinefromchar.md)
</dt> <dt>

[**\_LINEINDEX em**](em-lineindex.md)
</dt> </dl>

 

 





