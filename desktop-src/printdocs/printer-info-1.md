---
description: La \_ struttura Printer Info \_ 1 specifica le informazioni generali sulla stampante.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: Struttura PRINTER_INFO_1 (winspool. h)
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
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314001"
---
# <a name="printer_info_1-structure"></a>\_Struttura Info stampante \_ 1

La struttura **Printer \_ info \_ 1** specifica le informazioni generali sulla stampante.

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

Specifica le informazioni sui dati restituiti. Di seguito sono riportati i valori di questo membro.



| Valore                    | Significato                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_espansione enumerazione \_ stampanti    | Un provider di stampa può impostare questo flag come hint per un'applicazione chiamante per enumerare ulteriormente questo oggetto se è abilitata l'espansione predefinita. Ad esempio, quando vengono enumerati i domini, un provider di stampa potrebbe indicare il dominio dell'utente impostando questo flag. |
| \_contenitore enum \_ Printer | Se questo flag è impostato, l'oggetto stampante può contenere oggetti enumerabili. Ad esempio, l'oggetto può essere un server di stampa che contiene stampanti.                                                                                                             |
| \_ICON1 enum \_ Printer     | Indica che, laddove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come nome di rete di primo livello, ad esempio rete Microsoft Windows.                                                                                           |
| \_Icon2 enum \_ Printer     | Indica che, laddove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come dominio di rete.                                                                                                                                  |
| \_ICON3 enum \_ Printer     | Indica che, laddove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come server di stampa.                                                                                                                                    |
| \_ICON4 enum \_ Printer     | Riservato.                                                                                                                                                                                                                                                 |
| \_ICON5 enum \_ Printer     | Riservato.                                                                                                                                                                                                                                                 |
| \_ICON6 enum \_ Printer     | Riservato.                                                                                                                                                                                                                                                 |
| \_Icon7 enum \_ Printer     | Riservato.                                                                                                                                                                                                                                                 |
| \_ICON8 enum \_ Printer     | Indica che, laddove appropriato, un'applicazione deve visualizzare un'icona che identifica l'oggetto come stampante.                                                                                                                                         |



 

</dd> <dt>

**pDescription**
</dt> <dd>

Puntatore a una stringa con terminazione null che descrive il contenuto della struttura.

</dd> <dt>

**pName**
</dt> <dd>

Puntatore a una stringa con terminazione null che assegna un nome al contenuto della struttura.

</dd> <dt>

**pComment**
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene dati aggiuntivi che descrivono la struttura.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Info stampante \_ 1W** (Unicode) e **\_ \_ Info stampante \_ 1a** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Informazioni stampante \_ 3**](printer-info-3.md)
</dt> <dt>

[**\_Informazioni stampante \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




