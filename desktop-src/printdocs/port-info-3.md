---
description: La struttura della porta \_ info \_ 3 specifica il valore di stato di una porta stampante.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: Struttura PORT_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 49888ee6410f39745b848bbbf7fd95fa329c6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311813"
---
# <a name="port_info_3-structure"></a>Struttura delle informazioni sulla porta \_ \_ 3

La struttura della **porta \_ info \_ 3** specifica il valore di stato di una porta stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a>Members

<dl> <dt>

**dwStatus**
</dt> <dd>

Nuovo valore dello stato della porta. Questo valore viene utilizzato solo se il membro **pszStatus** è **null**.

Il membro può essere uno dei valori seguenti.



| Valore                            | Significato                                             |
|----------------------------------|-----------------------------------------------------|
| 0                                | Cancella lo stato della porta stampante.                     |
| \_stato porta \_ offline            | La stampante della porta è offline.                      |
| \_ \_ inceppamento carta stato porta \_         | Alla stampante della porta è associato un inceppamento della carta.                 |
| carta di stato porta in \_ \_ \_ uscita         | La stampante della porta è fuori carta.                 |
| \_ \_ bin output stato \_ porta \_ completo  | Il contenitore di output printer's della porta è pieno.            |
| problema relativo alla carta di stato della porta \_ \_ \_     | La stampante della porta presenta un problema relativo alla carta.             |
| \_stato porta \_ senza \_ toner          | La stampante della porta non è presente nel toner.                 |
| \_sportello stato \_ porta \_ aperto         | La porta della stampante della porta è aperta.             |
| \_ \_ intervento dell'utente stato porta \_ | La stampante della porta richiede l'intervento dell'utente.      |
| \_ \_ \_ memoria insufficiente per lo stato della porta \_    | La stampante della porta ha esaurito la memoria.                |
| \_ \_ toner stato porta \_ basso         | Il toner della porta è insufficiente.                 |
| \_stato di \_ riscaldamento della porta \_        | La stampante della porta si sta scaldando.                   |
| \_ \_ risparmio energia stato \_ porta        | La stampante della porta è in modalità di risparmio energia. |



 

</dd> <dt>

**pszStatus**
</dt> <dd>

Puntatore a una nuova stringa del valore dello stato della porta stampante da impostare. Utilizzare questo membro se non esiste alcun valore di stato appropriato tra quelli elencati per **dwStatus**.

</dd> <dt>

**dwSeverity**
</dt> <dd>

Gravità del valore dello stato della porta.

Il membro può essere uno dei valori seguenti.



| Valore                       | Significato                                   |
|-----------------------------|-------------------------------------------|
| \_ \_ errore tipo di stato porta \_   | Il valore dello stato della porta indica un errore. |
| \_ \_ avviso tipo di stato porta \_ | Il valore dello stato della porta è un avviso.       |
| \_informazioni sul \_ tipo di stato della porta \_    | Il valore dello stato della porta è informativo.   |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si imposta un valore di stato porta stampante con l' \_ errore tipo di stato porta valore gravità \_ \_ , lo spooler di stampa interrompe l'invio di processi alla porta. Lo spooler di stampa non riprende l'invio di processi alla porta fino a quando non viene eseguita un'altra chiamata di [**porta**](setport.md) per cancellare lo stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ Informazioni sulla porta \_ \_ 3W** (Unicode) e **\_ informazioni sulla porta \_ \_ 3A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Porta**](setport.md)
</dt> </dl>

 

 




