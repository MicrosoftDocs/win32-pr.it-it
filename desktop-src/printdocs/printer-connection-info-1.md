---
description: Rappresenta le informazioni su una connessione a una stampante.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: Struttura PRINTER_CONNECTION_INFO_1 (winspool. h)
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
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757382"
---
# <a name="printer_connection_info_1-structure"></a>Struttura delle informazioni di connessione della stampante \_ \_ \_ 1

Rappresenta le informazioni su una connessione a una stampante.

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
| \_ \_ Mancata corrispondenza della connessione stampante (0x00000020) | Se questo flag di bit è impostato, la connessione alla stampante non corrisponde. L'utente può fornire un driver di stampa locale come *pszDriverName* e utilizzarlo per eseguire il rendering anziché utilizzare il driver installato nella stampante server a cui è connesso l'utente.<br/>                                                                                                                                                                                                                                    |
| \_Connessione stampante \_ senza \_ interfaccia utente (0x00000040)   | Se viene impostato questo flag di bit, questa chiamata non potrà visualizzare una finestra di dialogo. Se è necessario visualizzare una finestra di dialogo per installare un driver della stampante dal server e questo flag di bit è impostato, il driver della stampante non verrà installato, la connessione alla stampante non verrà aggiunta e la chiamata avrà esito negativo.<br/> **Windows 7:** In Windows 7 e nelle versioni successive di Windows, se questo flag è impostato e l'utente è in esecuzione in modalità con privilegi elevati, la finestra di dialogo **attendibile per la stampante?** non verrà visualizzata.<br/> |



 

</dd> <dt>

**pszDriverName**
</dt> <dd>

Puntatore al nome del driver.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




