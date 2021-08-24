---
description: La struttura PRINTER \_ INFO \_ 4 specifica le informazioni generali sulla stampante. La struttura può essere utilizzata per recuperare informazioni minime sulla stampante in una chiamata a EnumPrinters.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: PRINTER_INFO_4 struttura (Winspool.h)
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
ms.openlocfilehash: 3ba6e372b495c47dd92e61e51ba6487e6d9c2c0aca924bf6ed3a092ba0816820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119446991"
---
# <a name="printer_info_4-structure"></a>Struttura PRINTER \_ INFO \_ 4

La **struttura PRINTER INFO \_ \_ 4** specifica le informazioni generali sulla stampante.

La struttura può essere utilizzata per recuperare informazioni minime sulla stampante in una chiamata a [**EnumPrinters**](enumprinters.md). Una chiamata di questo tipo è un modo semplice e rapido per recuperare i nomi e gli attributi di tutte le stampanti installate localmente in un sistema e di tutte le connessioni remote alle stampanti stabilite da un utente.

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

Puntatore a una stringa con terminazione Null che specifica il nome della stampante (locale o remota).

</dd> <dt>

**pServerName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che rappresenta il nome del server.

</dd> <dt>

**Attributes (Attributi)**
</dt> <dd>

Specifica le informazioni sui dati restituiti.



| Valore                       | Significato                          |
|-----------------------------|----------------------------------|
| ATTRIBUTO \_ PRINTER \_ LOCAL   | La stampante è una stampante locale.  |
| PRINTER \_ ATTRIBUTE \_ NETWORK | La stampante è una stampante remota. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura PRINTER INFO \_ \_ 4** offre un modo semplice ed estremamente rapido per recuperare i nomi delle stampanti installate in un computer locale, nonché le connessioni remote stabilite da un utente. Quando [**EnumPrinters viene**](enumprinters.md) chiamato con una struttura di dati **PRINTER INFO \_ \_ 4,** tale funzione esegue una query nel Registro di sistema per ottenere le informazioni specificate, quindi restituisce immediatamente un risultato. Questo comportamento differisce dal comportamento di **EnumPrinters** quando viene chiamato con altri livelli di strutture di dati **PRINTER INFO \_ \_ xxx.** In particolare, quando **EnumPrinters** viene chiamato con una struttura di dati di livello 2 (**PRINTER INFO \_ \_ 2** ), esegue una chiamata **OpenPrinter** su ogni connessione remota. Se una connessione remota non è attiva, se il server remoto non esiste più o se la stampante remota non esiste più, la funzione deve attendere il timeout di RPC e di conseguenza non eseguire la chiamata **a OpenPrinter.** L'operazione può richiedere un po' di tempo. Il passaggio di una struttura **PRINTER \_ INFO \_ 4** consente a un'applicazione di recuperare un minimo di informazioni necessarie. Se si desiderano informazioni più dettagliate, è possibile eseguire una chiamata di livello 2 **EnumPrinter** successiva.

**Gli** attributi possono inoltre contenere valori definiti nel **campo Attributi** di PRINTER **INFO \_ \_ 2.**

Alcune configurazioni della stampante, ad esempio le connessioni della stampante ad alcuni server di stampa non basati su Windows, potrebbero restituire sia **PRINTER \_ ATTRIBUTE \_ LOCAL** che **PRINTER ATTRIBUTE \_ \_ NETWORK**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PRINTER \_ INFO \_ 4W** (Unicode) e **\_ PRINTER INFO \_ \_ 4A** (ANSI)<br/>                           |



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

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 1**](printer-info-1.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 2**](printer-info-2.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 3**](printer-info-3.md)
</dt> </dl>

 

 




