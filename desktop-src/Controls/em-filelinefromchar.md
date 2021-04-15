---
title: Messaggio EM_FILELINEFROMCHAR (CommCtrl. h)
description: Ottiene l'indice della riga che contiene l'indice del carattere specificato in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Controlli di Windows Message EM_FILELINEFROMCHAR
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
ms.openlocfilehash: 7a083d7e12822eacfb1e29a7d4bfd2ea705f2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477332"
---
# <a name="em_filelinefromchar-message"></a>\_Messaggio FILELINEFROMCHAR em

Ottiene l'indice della riga che contiene l'indice del carattere specificato in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo. Un indice dei caratteri è l'indice in base zero del carattere a partire dall'inizio del controllo di modifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dei caratteri del carattere contenuto nella riga di cui è necessario recuperare il numero. Se questo parametro è-1, **em \_ FILELINEFROMCHAR** Recupera il numero di riga della riga corrente (la riga contenente il punto di inserimento) o, se è presente una selezione, il numero di riga della riga contenente l'inizio della selezione.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il numero di riga in base zero della riga che contiene l'indice dei caratteri specificato da *wParam*, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10, 1809 \[\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2019\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_FILELINEINDEX em**](em-filelineindex.md)
</dt> </dl>

 

 





