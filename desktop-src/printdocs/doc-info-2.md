---
description: La \_ struttura doc info \_ 2 descrive un documento che verrà stampato.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: Struttura DOC_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76b66711883e2238e971cb26d071716bd52ca54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316426"
---
# <a name="doc_info_2-structure"></a>\_Struttura doc info \_ 2

La struttura **doc \_ info \_ 2** descrive un documento che verrà stampato.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a>Members

<dl> <dt>

**pDocName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome di un file di output.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica il tipo di dati utilizzati per registrare il documento.

</dd> <dt>

**dwMode**
</dt> <dd>

Informa lo spooler di stampa della natura dei dati da seguire. Se questo valore è zero, lo spooler di stampa considera i dati inviati dalle chiamate successive a [**WritePrinter**](writeprinter.md) come processo di stampa normale (indipendentemente dal fatto che venga eseguito lo spooling a seconda della proprietà della stampante). Se questo valore è DI \_ canale di, viene aperto solo un canale di comunicazione. In questo caso, i dati passati alle chiamate successive a **WritePrinter** vengono inviati alla stampante o alle chiamate successive a [**ReadPrinter**](readprinter.md) per recuperare i dati dalla stampante. Questa modalità rimane valida fino a quando non viene chiamato [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .

</dd> <dt>

**JobId**
</dt> <dd>

Riservato per uso interno; deve essere zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Info doc \_ 2W** (Unicode) e **\_ doc \_ info \_ 2a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[**ReadPrinter**](readprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




