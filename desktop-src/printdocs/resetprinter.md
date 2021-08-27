---
description: La funzione ResetPrinter specifica il tipo di dati e i valori della modalità dispositivo da utilizzare per la stampa di documenti inviati dalla funzione StartDocPrinter. È possibile eseguire l'override di questi valori usando la funzione SetJob dopo l'avvio della stampa dei documenti.
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: Funzione ResetPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResetPrinter
- ResetPrinterA
- ResetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: f68601acde884d15572871848eed2d2388c927cf04758ad1183343486d4cc0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470280"
---
# <a name="resetprinter-function"></a>Funzione ResetPrinter

La **funzione ResetPrinter** specifica il tipo di dati e i valori della modalità dispositivo da utilizzare per la stampa di documenti inviati dalla [**funzione StartDocPrinter.**](startdocprinter.md) È possibile eseguire l'override di questi valori usando la [**funzione SetJob**](setjob.md) dopo l'avvio della stampa dei documenti.

## <a name="syntax"></a>Sintassi


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante. Usare la [**funzione OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*pDefault* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura PRINTER \_ DEFAULTS.**](printer-defaults.md)

La **funzione ResetPrinter** ignora il **membro DesiredAccess** della [**struttura PRINTER \_ DEFAULTS.**](printer-defaults.md) Impostare il membro su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **ResetPrinterW** (Unicode) e **ResetPrinterA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**IMPOSTAZIONI \_ PREDEFINITE DELLA STAMPANTE**](printer-defaults.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

 




