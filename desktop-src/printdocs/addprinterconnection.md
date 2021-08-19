---
description: La funzione AddPrinterConnection aggiunge una connessione alla stampante specificata per l'utente corrente.
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: Funzione AddPrinterConnection (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection
- AddPrinterConnectionA
- AddPrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 83c4d348266e0d596deccb03b39e98ec41f8f23837727520d55b9baff82fec4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869033"
---
# <a name="addprinterconnection-function"></a>Funzione AddPrinterConnection

La **funzione AddPrinterConnection** aggiunge una connessione alla stampante specificata per l'utente corrente.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome di una stampante a cui l'utente corrente desidera stabilire una connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Quando Windows una connessione a una stampante, potrebbe essere necessario copiare i file del driver della stampante nel server a cui è collegata la stampante. Se l'utente non dispone dell'autorizzazione per copiare i file nel percorso appropriato, la funzione **AddPrinterConnection** ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ ACCESS \_ DENIED.

Una connessione della stampante stabilita chiamando **AddPrinterConnection** verrà enumerata quando [**EnumPrinters**](enumprinters.md) viene chiamato con *dwType* impostato su PRINTER \_ ENUM \_ CONNECTION.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddPrinterConnectionW** (Unicode) e **AddPrinterConnectionA** (ANSI)<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> <dt>

[**Enumprinters**](enumprinters.md)
</dt> </dl>

 

