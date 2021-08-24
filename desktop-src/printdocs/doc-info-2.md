---
description: La struttura DOC \_ INFO \_ 2 descrive un documento che verrà stampato.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: DOC_INFO_2 struttura (Winspool.h)
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
ms.openlocfilehash: 27d7753fa16abcfbc30b28bcc4343b2e1ef7996cad408b54fefb850feac9b17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846261"
---
# <a name="doc_info_2-structure"></a>Struttura DOC \_ INFO \_ 2

La **struttura DOC INFO \_ \_ 2** descrive un documento che verrà stampato.

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

Puntatore a una stringa con terminazione Null che specifica il nome del documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome di un file di output.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica il tipo di dati utilizzato per registrare il documento.

</dd> <dt>

**dwMode**
</dt> <dd>

Informa lo spooler di stampa della natura dei dati da seguire. Se questo valore è zero, lo spooler di stampa considera i dati inviati dalle chiamate successive a [**WritePrinter**](writeprinter.md) come un normale processo di stampa (lo spooling dipende dalla proprietà della stampante). Se questo valore è DI CHANNEL, viene aperto solo \_ un canale di comunicazione. In questo caso, i dati passati alle chiamate successive a **WritePrinter** vengono inviati alla stampante o le chiamate successive a [**ReadPrinter**](readprinter.md) recuperano i dati dalla stampante. Questa modalità rimane attiva fino a quando [**non viene chiamato EndDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)

</dd> <dt>

**Jobid**
</dt> <dd>

Riservato per uso interno; deve essere zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ DOC \_ INFO \_ 2W** (Unicode) e **\_ DOC INFO \_ \_ 2A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[**ReadPrinter**](readprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




