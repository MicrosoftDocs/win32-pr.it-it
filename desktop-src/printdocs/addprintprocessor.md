---
description: La funzione AddPrintProcessor installa un processore di stampa nel server specificato e aggiunge il nome del processore di stampa all'elenco dei processori di stampa supportati.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: Funzione AddPrintProcessor (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 83de05dd6aa0ef6541322a45894dcf24cffa3cc6bebcbbd3b42e6c48941360b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868746"
---
# <a name="addprintprocessor-function"></a>Funzione AddPrintProcessor

La **funzione AddPrintProcessor** installa un processore di stampa nel server specificato e aggiunge il nome del processore di stampa all'elenco dei processori di stampa supportati.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del server in cui deve essere installato il processore di stampa. Se questo parametro è **NULL,** il processore di stampa viene installato in locale.

</dd> <dt>

*pEnvironment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ambiente,ad esempio Windows x86, Windows IA64 o Windows x64). Se questo parametro è **NULL,** viene usato l'ambiente corrente del chiamante/client (non del server/destinazione).

</dd> <dt>

*pPathName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del file che contiene il processore di stampa. Questo file deve essere nella directory del processore di stampa di sistema.

</dd> <dt>

*pPrintProcessorName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del processore di stampa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Il chiamante deve avere [seLoadDriverPrivilege.](/windows/desktop/SecAuthZ/authorization-constants)

Prima di chiamare la **funzione AddPrintProcessor,** un'applicazione deve verificare che il file contenente il processore di stampa sia archiviato nella directory del processore di stampa di sistema. Un'applicazione può recuperare il nome della directory del processore di stampa di sistema chiamando la [**funzione GetPrintProcessorDirectory.**](getprintprocessordirectory.md)

Un'applicazione può determinare il nome dei processori di stampa esistenti chiamando la [**funzione EnumPrintProcessors.**](enumprintprocessors.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddPrintProcessorW** (Unicode) e **AddPrintProcessorA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**GetPrintProcessorDirectory**](getprintprocessordirectory.md)
</dt> </dl>

 

