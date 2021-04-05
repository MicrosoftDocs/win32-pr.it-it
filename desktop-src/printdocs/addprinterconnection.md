---
description: La funzione AddPrinterConnection aggiunge una connessione alla stampante specificata per l'utente corrente.
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: Funzione AddPrinterConnection (winspool. h)
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
ms.openlocfilehash: dae1f823f89b69526218ab4c027642fb54e3cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883209"
---
# <a name="addprinterconnection-function"></a>AddPrinterConnection (funzione)

La funzione **AddPrinterConnection** aggiunge una connessione alla stampante specificata per l'utente corrente.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome di una stampante a cui l'utente corrente desidera stabilire una connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Quando Windows crea una connessione a una stampante, potrebbe essere necessario copiare i file del driver della stampante nel server a cui è collegata la stampante. Se l'utente non dispone delle autorizzazioni per copiare i file nel percorso appropriato, la funzione **AddPrinterConnection** ha esito negativo e [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ accesso \_ negato.

Una connessione stampante stabilita chiamando **AddPrinterConnection** verrà enumerata quando viene chiamato [**EnumPrinters**](enumprinters.md) con *dwType* impostato su Printer \_ enum \_ Connection.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
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

[**EnumPrinters**](enumprinters.md)
</dt> </dl>

 

