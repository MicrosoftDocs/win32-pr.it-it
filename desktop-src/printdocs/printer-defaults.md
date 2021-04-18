---
description: La \_ struttura delle impostazioni predefinite della stampante specifica il tipo di dati predefinito, l'ambiente, i dati di inizializzazione e i diritti di accesso per una stampante.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: Struttura PRINTER_DEFAULTS (winspool. h)
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
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314010"
---
# <a name="printer_defaults-structure"></a>\_Struttura delle impostazioni predefinite della stampante

La struttura delle **\_ impostazioni predefinite della stampante** specifica il tipo di dati predefinito, l'ambiente, i dati di inizializzazione e i diritti di accesso per una stampante.

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

Puntatore a una stringa con terminazione null che specifica il tipo di dati predefinito per una stampante.

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che identifica l'ambiente predefinito e i dati di inizializzazione per una stampante.

</dd> <dt>

**DesiredAccess**
</dt> <dd>

Specifica i diritti di accesso desiderati per una stampante. La funzione [**OpenPrinter**](openprinter.md) utilizza questo membro per impostare i diritti di accesso alla stampante. Questi diritti possono influire sul funzionamento delle funzioni [**Seprinter**](setprinter.md) e [**DeletePrinter**](deleteprinter.md) . I diritti di accesso possono essere uno dei seguenti.



| Valore                                       | Significato                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_amministrazione dell'accesso alla stampante \_                 | Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md).                                                                                                 |
| \_uso dell'accesso alla stampante \_                        | Per eseguire operazioni di stampa di base.                                                                                                                                                        |
| \_gestione dell'accesso alla stampante \_ \_ limitata            | Per eseguire attività amministrative, ad esempio quelle fornite da [**Seprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md). Questo valore è disponibile a partire da Windows 8.1. |
| \_tutti gli \_ accessi alla stampante                        | Per eseguire tutte le attività amministrative e le operazioni di stampa di base, ad eccezione della sincronizzazione (vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) ).                                   |
| valori di sicurezza generici, ad esempio WRITE \_ DAC | Per consentire diritti di accesso di controllo specifici. Vedere [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ Printer \_ DEFAULTSW** (Unicode) e **\_ Printer \_ DEFAULTSA** (ANSI)<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

