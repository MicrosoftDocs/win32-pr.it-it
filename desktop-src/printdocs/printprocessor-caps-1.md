---
description: La \_ struttura PRINTPROCESSOR Caps \_ 1 è il formato per le informazioni sulle funzionalità della stampante restituite dalla funzione GetPrinterData nel buffer specificato dalla variabile pData.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: Struttura PRINTPROCESSOR_CAPS_1 (winspool. h)
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
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316423"
---
# <a name="printprocessor_caps_1-structure"></a>\_Struttura PRINTPROCESSOR Caps \_ 1

La struttura **PRINTPROCESSOR \_ Caps \_ 1** è il formato per le informazioni sulle funzionalità della stampante restituite dalla funzione [**GetPrinterData**](getprinterdata.md) nel buffer specificato dalla variabile *pData* .

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

Maschera di bit che rappresenta i vari numeri di pagine del documento che la stampante è in grado di stampare in una pagina fisica. Il bit meno significativo rappresenta 1 pagina documento per pagina, il bit successivo rappresenta 2 pagine documento per pagina e così via. Ad esempio, 0x0000810B indica che la stampante supporta 1, 2, 4, 9 e 16 pagine documento per ogni pagina fisica.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Ordine in cui verranno stampate le pagine. Questo valore può essere una stampa normale \_ , una stampa inversa \_ o un opuscolo \_ .

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Numero massimo di copie che la stampante è in grado di gestire.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori per tutti i membri della struttura sono forniti dalla funzione [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) , che è documentata in Windows Driver Kit (WDK).

Lo spooler chiama la funzione [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) di un processore di stampa quando un'applicazione chiama [**GetPrinterData**](getprinterdata.md), specificando il nome di un valore con formato PrintProcCaps \_ *DataType*, dove *DataType* è il nome di un tipo di dati di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

