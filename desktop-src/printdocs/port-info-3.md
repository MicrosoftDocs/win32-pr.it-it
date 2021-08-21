---
description: La struttura PORT \_ INFO \_ 3 specifica il valore di stato di una porta della stampante.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: PORT_INFO_3 (Winspool.h)
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
ms.openlocfilehash: cdd7f2fd931c7f503d566cdfc4ab38c5f595b51cea23d0cdf2fb326811cf7748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033969"
---
# <a name="port_info_3-structure"></a>Struttura PORT \_ INFO \_ 3

La **struttura PORT INFO \_ \_ 3** specifica il valore di stato di una porta della stampante.

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

Nuovo valore di stato della porta. Questo valore viene usato solo se il **membro pszStatus** è **NULL.**

Questo membro può essere uno dei valori seguenti.



| Valore                            | Significato                                             |
|----------------------------------|-----------------------------------------------------|
| 0                                | Cancella lo stato della porta della stampante.                     |
| STATO \_ PORTA \_ OFFLINE            | La stampante della porta è offline.                      |
| CARTA DI \_ STATO DELLA PORTA IN \_ \_ JAM         | La stampante della porta ha un inceppamento della carta.                 |
| PORT \_ STATUS \_ PAPER \_ OUT         | La stampante della porta è senza carta.                 |
| PORT \_ STATUS \_ OUTPUT \_ BIN \_ FULL  | Il bin di output della stampante della porta è pieno.            |
| PROBLEMA RELATIVO \_ AL DOCUMENTO SULLO STATO DELLA \_ \_ PORTA     | La stampante della porta presenta un problema di carta.             |
| STATO \_ PORTA \_ NO \_ TONER          | La stampante della porta è fuori toner.                 |
| PORTA \_ DI STATO PORTA \_ \_ APERTA         | La porta della stampante della porta è aperta.             |
| INTERVENTO \_ \_ DELL'UTENTE SULLO STATO DELLA \_ PORTA | La stampante della porta richiede l'intervento dell'utente.      |
| MEMORIA \_ INSUFFICIENTE PER LO STATO DELLA \_ \_ \_ PORTA    | Memoria insufficiente per la stampante della porta.                |
| PORT \_ STATUS \_ TONER \_ LOW         | Il toner della stampante della porta è basso.                 |
| RISCALDAMENTO \_ DELLO STATO DELLA \_ \_ PORTA        | La stampante della porta si sta riscaldamento.                   |
| STATO \_ PORTA \_ RISPARMIO ENERGIA \_        | La stampante della porta è in modalità di risparmio energia. |



 

</dd> <dt>

**pszStatus**
</dt> <dd>

Puntatore a una nuova stringa del valore di stato della porta della stampante da impostare. Usare questo membro se non esiste alcun valore di stato appropriato tra quelli elencati per **dwStatus**.

</dd> <dt>

**dwSeverity**
</dt> <dd>

Gravità del valore dello stato della porta.

Questo membro può essere uno dei valori seguenti.



| Valore                       | Significato                                   |
|-----------------------------|-------------------------------------------|
| ERRORE DEL \_ TIPO DI STATO DELLA \_ \_ PORTA   | Il valore di stato della porta indica un errore. |
| AVVISO \_ RELATIVO AL TIPO DI STATO DELLA \_ \_ PORTA | Il valore di stato della porta è un avviso.       |
| INFORMAZIONI SUL \_ TIPO DI STATO DELLA \_ \_ PORTA    | Il valore dello stato della porta è informativo.   |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si imposta un valore di stato della porta della stampante con il valore di gravità PORT STATUS TYPE ERROR, lo \_ spooler di stampa interrompe l'invio \_ \_ dei processi alla porta. Lo spooler di stampa non riprende l'invio dei processi alla porta fino a quando non viene effettuata un'altra [**chiamata SetPort**](setport.md) per cancellare lo stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PORT \_ INFO \_ 3W** (Unicode) e **\_ PORT INFO \_ \_ 3A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




