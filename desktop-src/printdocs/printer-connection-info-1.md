---
description: Rappresenta informazioni su una connessione a una stampante.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: PRINTER_CONNECTION_INFO_1 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b9adbe18d3f75062a67440fd7f7586c4336323ff3035416f3ad9799f5e34a17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033899"
---
# <a name="printer_connection_info_1-structure"></a>Struttura PRINTER \_ CONNECTION \_ INFO \_ 1

Rappresenta informazioni su una connessione a una stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**dwFlags**
</dt> <dd>

Vengono definiti i valori seguenti:



| Valore                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MANCATA \_ \_ CORRISPONDENZA CONNESSIONE STAMPANTE (0x00000020) | Se questo flag di bit è impostato, la connessione della stampante non corrisponde. L'utente può fornire un driver di stampa locale come *pszDriverName* e usarlo per eseguire il rendering anziché usare il driver installato nella stampante server a cui l'utente è connesso.<br/>                                                                                                                                                                                                                                    |
| CONNESSIONE \_ STAMPANTE NESSUNA INTERFACCIA UTENTE \_ \_ (0x00000040)   | Se questo flag di bit è impostato, questa chiamata non può visualizzare una finestra di dialogo. Se è necessario visualizzare una finestra di dialogo per installare un driver della stampante dal server e questo flag di bit è impostato, il driver della stampante non verrà installato, la connessione della stampante non verrà aggiunta e la chiamata avrà esito negativo.<br/> **Windows 7:** In Windows 7 e versioni successive di Windows, se questo flag è impostato e l'utente è in esecuzione in modalità con privilegi elevati, la finestra di dialogo Considera attendibile questa **stampante?** non verrà visualizzata.<br/> |



 

</dd> <dt>

**pszDriverName**
</dt> <dd>

Puntatore al nome del driver.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




