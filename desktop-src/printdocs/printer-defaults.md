---
description: La struttura PRINTER DEFAULTS specifica il tipo di dati predefinito, l'ambiente, i dati di inizializzazione e i diritti di accesso \_ per una stampante.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: PRINTER_DEFAULTS struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: f1419948dddcd579e559ed084ce0af092cec373a7cd7f6d4b05d41f104f6666b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731689"
---
# <a name="printer_defaults-structure"></a>Struttura PRINTER \_ DEFAULTS

La **struttura PRINTER \_ DEFAULTS** specifica il tipo di dati predefinito, l'ambiente, i dati di inizializzazione e i diritti di accesso per una stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a>Members

<dl> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il tipo di dati predefinito per una stampante.

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntatore a una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che identifica l'ambiente predefinito e i dati di inizializzazione per una stampante.

</dd> <dt>

**DesiredAccess**
</dt> <dd>

Specifica i diritti di accesso desiderati per una stampante. La [**funzione OpenPrinter**](openprinter.md) usa questo membro per impostare i diritti di accesso alla stampante. Questi diritti possono influire sul funzionamento delle [**funzioni SetPrinter**](setprinter.md) [**e DeletePrinter.**](deleteprinter.md) I diritti di accesso possono essere uno dei seguenti.



| Valore                                       | Significato                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AMMINISTRAZIONE \_ DELL'ACCESSO ALLA \_ STAMPANTE                 | Per eseguire attività amministrative, ad esempio quelle fornite da [**SetPrinter**](setprinter.md).                                                                                                 |
| USO \_ DELL'ACCESSO ALLA \_ STAMPANTE                        | Per eseguire operazioni di stampa di base.                                                                                                                                                        |
| GESTIONE LIMITATA \_ \_ DELL'ACCESSO ALLA \_ STAMPANTE            | Per eseguire attività amministrative, ad esempio quelle fornite da [**SetPrinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md). Questo valore è disponibile a partire da Windows 8.1. |
| ACCESSO A PRINTER \_ ALL \_                        | Per eseguire tutte le attività amministrative e le operazioni di stampa di base ad eccezione di SYNCHRONIZE (vedere [Diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) ).                                   |
| valori di sicurezza generici, ad esempio l'applicazione livello dati WRITE \_ | Per consentire diritti di accesso di controllo specifici. Vedere [Diritti di accesso standard.](/windows/desktop/SecAuthZ/standard-access-rights)                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PRINTER \_ DEFAULTSW** (Unicode) e **\_ PRINTER \_ DEFAULTSA** (ANSI)<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> </dl>

 

