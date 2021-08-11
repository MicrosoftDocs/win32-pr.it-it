---
description: La struttura PRINTER \_ INFO \_ 1 specifica le informazioni generali sulla stampante.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: PRINTER_INFO_1 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ab70662371ef4ebe80b1d10f7f61700c97e979959c337bb5e81b3bc688e8c36b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234208"
---
# <a name="printer_info_1-structure"></a>Struttura PRINTER \_ INFO \_ 1

La **struttura PRINTER INFO \_ \_ 1** specifica le informazioni generali sulla stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**Flag**
</dt> <dd>

Specifica le informazioni sui dati restituiti. Di seguito sono riportati i valori per questo membro.



| Valore                    | Significato                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PRINTER \_ ENUM \_ EXPAND    | Un provider di stampa può impostare questo flag come hint per un'applicazione chiamante per enumerare ulteriormente questo oggetto se è abilitata l'espansione predefinita. Ad esempio, quando i domini vengono enumerati, un provider di stampa potrebbe indicare il dominio dell'utente impostando questo flag. |
| CONTENITORE PRINTER \_ ENUM \_ | Se questo flag è impostato, l'oggetto stampante può contenere oggetti enumerabili. Ad esempio, l'oggetto può essere un server di stampa che contiene stampanti.                                                                                                             |
| ICONA \_ ENUMERAZIONE \_ STAMPANTE1     | Indica che, dove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come nome di rete di primo livello, ad esempio Microsoft Windows Network.                                                                                           |
| ICONA \_ ENUMERAZIONE \_ STAMPANTE2     | Indica che, dove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come dominio di rete.                                                                                                                                  |
| ICONA \_ ENUMERAZIONE \_ STAMPANTE3     | Indica che, dove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come server di stampa.                                                                                                                                    |
| ICONA \_ ENUMERAZIONE \_ STAMPANTE4     | Riservato.                                                                                                                                                                                                                                                 |
| ICONA \_ ENUMERAZIONE \_ STAMPANTE5     | Riservato.                                                                                                                                                                                                                                                 |
| ICONA \_ ENUMERAZIONE \_ STAMPANTE6     | Riservato.                                                                                                                                                                                                                                                 |
| ICONA \_ ENUMERAZIONE \_ STAMPANTE7     | Riservato.                                                                                                                                                                                                                                                 |
| ICONA \_ ENUMERAZIONE \_ STAMPANTE8     | Indica che, dove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come stampante.                                                                                                                                         |



 

</dd> <dt>

**pDescription**
</dt> <dd>

Puntatore a una stringa con terminazione Null che descrive il contenuto della struttura .

</dd> <dt>

**Pname**
</dt> <dd>

Puntatore a una stringa con terminazione Null che indica il contenuto della struttura .

</dd> <dt>

**pComment**
</dt> <dd>

Puntatore a una stringa con terminazione Null che contiene dati aggiuntivi che descrivono la struttura .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PRINTER \_ INFO \_ 1W** (Unicode) e **\_ PRINTER INFO \_ \_ 1A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Enumprinters**](enumprinters.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 2**](printer-info-2.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 3**](printer-info-3.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




