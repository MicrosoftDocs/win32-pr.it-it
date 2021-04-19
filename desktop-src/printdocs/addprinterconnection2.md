---
description: Aggiunge una connessione alla stampante specificata per l'utente corrente e specifica i dettagli della connessione.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: Funzione AddPrinterConnection2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311566"
---
# <a name="addprinterconnection2-function"></a>AddPrinterConnection2 (funzione)

Aggiunge una connessione alla stampante specificata per l'utente corrente e specifica i dettagli della connessione.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle per la finestra padre in cui verrà visualizzata la finestra di dialogo se il sistema di stampa deve scaricare un driver della stampante dal server di stampa per questa connessione.

</dd> <dt>

*pszName* \[ in\]
</dt> <dd>

Puntatore a una stringa costante con terminazione null che specifica il nome della stampante a cui l'utente corrente desidera connettersi.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Versione della struttura a cui punta *pConnectionInfo*. Attualmente, viene definito solo il livello 1, pertanto il valore di *dwLevel* deve essere 1.

</dd> <dt>

*pConnectionInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ informazioni di connessione della stampante \_ \_ 1**](printer-connection-info-1.md) . Per ulteriori informazioni su questo parametro, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero. Per informazioni estese sugli errori, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Quando Windows Vista effettua una connessione a una stampante, potrebbe essere necessario copiare i file del driver della stampante dal server a cui è collegata la stampante. Se l'utente non dispone delle autorizzazioni per copiare i file nel percorso appropriato, la funzione **AddPrinterConnection2** ha esito negativo e [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore di \_ accesso \_ negato.

Se i file del driver della stampante devono essere copiati dal server di stampa ma non possono essere copiati in modo invisibile a causa dei criteri di gruppo in vigore e \_ la connessione alla stampante \_ non \_ è impostata alcuna interfaccia utente in *pConnectionInfo->dwFlags*, non verrà visualizzata alcuna finestra di dialogo e la chiamata avrà esito negativo.

Se il driver della stampante locale può essere utilizzato per eseguire il rendering dei processi di stampa per questa stampante e la versione del driver locale non deve corrispondere alla versione del driver della stampante nel server, impostare la \_ mancata corrispondenza della connessione della stampante \_ in *PConnectionInfo->dwFlags* e assegnare il puntatore a una variabile di stringa che contiene il percorso del driver della stampante locale a *pConnectionInfo->pszDriverName*.

Una connessione stampante stabilita chiamando **AddPrinterConnection2** verrà enumerata quando viene chiamato [**EnumPrinters**](enumprinters.md) con *dwType* impostato su Printer \_ enum \_ Connection.

La versione ANSI di questa funzione, **AddPrinterConnection2A**, non è supportata e restituisce l' **errore \_ non \_ supportato**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddPrinterConnection2W** (Unicode)<br/>                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> </dl>

 

