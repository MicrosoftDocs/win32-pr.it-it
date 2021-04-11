---
description: La \_ struttura Printer Info \_ 4 specifica le informazioni generali sulla stampante. La struttura può essere utilizzata per recuperare informazioni minime sulla stampante in una chiamata a EnumPrinters.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: Struttura PRINTER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9a1501008f0235ea303dd1457fc8756c28abc21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232894"
---
# <a name="printer_info_4-structure"></a>\_Struttura Info stampante \_ 4

La struttura **Printer \_ info \_ 4** specifica le informazioni generali sulla stampante.

La struttura può essere utilizzata per recuperare informazioni minime sulla stampante in una chiamata a [**EnumPrinters**](enumprinters.md). Questa chiamata è un modo rapido e semplice per recuperare i nomi e gli attributi di tutte le stampanti installate localmente in un sistema e tutte le connessioni di stampanti remote stabilite da un utente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a>Members

<dl> <dt>

**pPrinterName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome della stampante (locale o remota).

</dd> <dt>

**pServerName**
</dt> <dd>

Puntatore a una stringa con terminazione null che rappresenta il nome del server.

</dd> <dt>

**Attributes (Attributi)**
</dt> <dd>

Specifica le informazioni sui dati restituiti.



| Valore                       | Significato                          |
|-----------------------------|----------------------------------|
| \_attributo stampante \_ locale   | La stampante è una stampante locale.  |
| \_rete attributi \_ stampante | La stampante è una stampante remota. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura delle **informazioni di stampa \_ \_ 4** fornisce un metodo semplice ed estremamente rapido per recuperare i nomi delle stampanti installate in un computer locale, nonché le connessioni remote stabilite da un utente. Quando [**EnumPrinters**](enumprinters.md) viene chiamato con una struttura di dati **Printer \_ info \_ 4** , tale funzione esegue una query sul Registro di sistema per ottenere le informazioni specificate, quindi restituisce immediatamente un risultato. Questo comportamento è diverso da quello di **EnumPrinters** quando viene chiamato con altri livelli di strutture di dati **\_ \_ xxx per informazioni sulla stampante** . In particolare, quando **EnumPrinters** viene chiamato con una struttura di dati di livello 2 (**Printer \_ info \_ 2** ), esegue una chiamata **OpenPrinter** su ogni connessione remota. Se una connessione remota è inattiva, se il server remoto non esiste più o se la stampante remota non esiste più, la funzione deve attendere il timeout di RPC e, di conseguenza, interrompere la chiamata **OpenPrinter** . L'operazione può richiedere un po' di tempo. Il passaggio di una struttura **Printer \_ info \_ 4** consente a un'applicazione di recuperare un minimo di informazioni obbligatorie; se si desidera ottenere informazioni più dettagliate, è possibile effettuare una chiamata di **EnumPrinter** Level 2 successiva.

**Gli attributi** possono inoltre contenere valori definiti nel campo **attributi** di **Printer \_ info \_ 2**.

Alcune configurazioni della stampante, ad esempio le connessioni alle stampanti ad alcuni server di stampa non basati su Windows, potrebbero restituire sia la **\_ \_ rete** locale degli attributi della stampante che l' **\_ \_ attributo Printer** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ Informazioni sulla stampante \_ \_ 4W** (Unicode) e **\_ informazioni sulla stampante \_ \_ 4a** (ANSI)<br/>                           |



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

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_Informazioni stampante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Informazioni stampante \_ 3**](printer-info-3.md)
</dt> </dl>

 

 




