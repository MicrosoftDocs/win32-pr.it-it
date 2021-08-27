---
description: Specifica la memorizzazione nella cache di un handle per una stampante aperta con OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: PRINTER_OPTION_FLAGS enumerazione (Winspool.h)
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
ms.openlocfilehash: b8541ec00f0d53bf58a826ceb7d8b8a821008fb6a66c0fe3917ebc12822e0e5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091801"
---
# <a name="printer_option_flags-enumeration"></a>Enumerazione PRINTER \_ OPTION \_ FLAGS

Specifica la memorizzazione nella cache di un handle per una stampante aperta [**con OpenPrinter2.**](openprinter2.md)

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

<span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**OPZIONE \_ STAMPANTE \_ NESSUNA \_ CACHE**
</dt> <dd>

L'handle non viene memorizzato nella cache. Tutte le funzioni applicate a un handle restituito da [**OpenPrinter2**](openprinter2.md) verranno applicate al computer remoto.

</dd> <dt>

<span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**PRINTER \_ OPTION \_ CACHE**
</dt> <dd>

L'handle viene memorizzato nella cache. Tutte le funzioni applicate a un handle restituito [**da OpenPrinter2**](openprinter2.md) verranno memorizzate nella cache locale.

</dd> <dt>

<span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**MODIFICA \_ DEL \_ CLIENT DELL'OPZIONE \_ STAMPANTE**
</dt> <dd>

L'handle restituito [**da OpenPrinter2**](openprinter2.md) può essere usato da [**SetPrinter**](setprinter.md) per rinominare la connessione della stampante.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> </dl>

 

 




