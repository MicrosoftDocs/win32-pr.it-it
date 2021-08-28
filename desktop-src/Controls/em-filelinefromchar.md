---
title: EM_FILELINEFROMCHAR messaggio (CommCtrl.h)
description: Ottiene l'indice della riga che contiene l'indice dei caratteri specificato in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_FILELINEFROMCHAR dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d238117a9f2ba18ae838eec32d7dc2fa12ba0833f9cdee54ce2d1a2c998944
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915631"
---
# <a name="em_filelinefromchar-message"></a>Messaggio EM \_ FILELINEFROMCHAR

Ottiene l'indice della riga che contiene l'indice dei caratteri specificato in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo. Un indice di caratteri è l'indice in base zero del carattere dall'inizio del controllo di modifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dei caratteri del carattere contenuto nella riga di cui recuperare il numero. Se questo parametro è -1, **EM \_ FILELINEFROMCHAR** recupera il numero di riga della riga corrente (la riga contenente il punto di selezione) o, se è presente una selezione, il numero di riga della riga contenente l'inizio della selezione.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero di riga in base zero della riga contenente l'indice dei caratteri specificato da *wParam*, indipendentemente dalla modalità di visualizzazione delle righe sullo schermo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2019 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ FILELINEINDEX**](em-filelineindex.md)
</dt> </dl>

 

 





