---
description: Specifica la memorizzazione nella cache di un handle per una stampante aperta con OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: Enumerazione PRINTER_OPTION_FLAGS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233042"
---
# <a name="printer_option_flags-enumeration"></a>\_ \_ Enumerazione flag opzioni stampante

Specifica la memorizzazione nella cache di un handle per una stampante aperta con [**OpenPrinter2**](openprinter2.md).

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**\_opzione stampante \_ senza \_ cache**
</dt> <dd>

L'handle non viene memorizzato nella cache. Tutte le funzioni applicate a un handle restituito da [**OpenPrinter2**](openprinter2.md) verranno inviate al computer remoto.

</dd> <dt>

<span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**\_cache delle opzioni della stampante \_**
</dt> <dd>

L'handle viene memorizzato nella cache. Tutte le funzioni applicate a un handle restituito da [**OpenPrinter2**](openprinter2.md) verranno inviate alla cache locale.

</dd> <dt>

<span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**\_opzione stampante \_ - \_ modifica client**
</dt> <dd>

L'handle restituito da [**OpenPrinter2**](openprinter2.md) può essere usato da [**seprinter**](setprinter.md) per rinominare la connessione alla stampante.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




