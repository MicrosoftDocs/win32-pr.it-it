---
description: La struttura PRINTPROCESSOR CAPS 1 è il formato per le informazioni sulle funzionalità della stampante restituite dalla \_ funzione GetPrinterData nel buffer specificato dalla \_ variabile pData.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: PRINTPROCESSOR_CAPS_1 struttura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d057914ef9a77c7a545817b205f919afa66fdd3bc154363f7e33a9a5ba43c446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824791"
---
# <a name="printprocessor_caps_1-structure"></a>Struttura PRINTPROCESSOR \_ CAPS \_ 1

La **struttura PRINTPROCESSOR \_ CAPS \_ 1** è il formato per le informazioni sulle funzionalità della stampante restituite dalla [**funzione GetPrinterData**](getprinterdata.md) nel buffer specificato dalla *variabile pData.*

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a>Members

<dl> <dt>

**dwLevel**
</dt> <dd>

Numero di versione della struttura. Questo valore deve essere 1.

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Maschera di bit che rappresenta il numero di pagine di documenti stampate dalla stampante su una pagina fisica. Il bit meno significativo rappresenta 1 pagina di documento per pagina, il bit successivo rappresenta 2 pagine di documento per pagina e così via. Ad esempio, 0x0000810B indica che la stampante supporta 1, 2, 4, 9 e 16 pagine di documenti per pagina fisica.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Ordine in cui verranno stampate le pagine. Questo valore può essere NORMAL \_ PRINT, REVERSE \_ PRINT o BOOKLET \_ PRINT.

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Numero massimo di copie che la stampante è in grado di gestire.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori per tutti i membri della struttura vengono forniti dalla funzione [**GetPrintProcessorCapabilities,**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) documentata in Windows Driver Kit (WDK).

Lo spooler chiama la funzione [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) di un processore di stampa quando un'applicazione chiama [**GetPrinterData**](getprinterdata.md), specificando un nome di valore con un formato di tipo di dati PrintProcCaps , dove datatype è il nome di un tipo di \_ dati di input. 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

