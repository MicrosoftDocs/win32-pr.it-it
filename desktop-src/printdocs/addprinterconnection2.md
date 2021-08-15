---
description: Aggiunge una connessione alla stampante specificata per l'utente corrente e specifica i dettagli della connessione.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: Funzione AddPrinterConnection2 (Winspool.h)
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
ms.openlocfilehash: f54cdafc2bc5c957f21ed4f9a14355d6a70f7df817e975c1fe701e2b20af35a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868969"
---
# <a name="addprinterconnection2-function"></a>Funzione AddPrinterConnection2

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

*hWnd* \[ Pollici\]
</dt> <dd>

Handle per la finestra padre in cui verrà visualizzata la finestra di dialogo se il sistema di stampa deve scaricare un driver della stampante dal server di stampa per questa connessione.

</dd> <dt>

*pszName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica il nome della stampante a cui l'utente corrente desidera connettersi.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Versione della struttura a cui punta *pConnectionInfo*. Attualmente è definito solo il livello 1, quindi il valore di *dwLevel* deve essere 1.

</dd> <dt>

*pConnectionInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura PRINTER CONNECTION INFO \_ \_ \_ 1.**](printer-connection-info-1.md) Per altre informazioni su questo parametro, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero. Per informazioni estese sugli errori, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Quando Windows Vista effettua una connessione a una stampante, potrebbe essere necessario copiare i file del driver della stampante dal server a cui è collegata la stampante. Se l'utente non dispone dell'autorizzazione per copiare i file nel percorso appropriato, la **funzione AddPrinterConnection2** ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ ACCESS \_ DENIED.

Se i file del driver della stampante devono essere copiati dal server di stampa ma non possono essere copiati automaticamente a causa dei criteri di gruppo in vigore e PRINTER CONNECTION NO UI è impostata \_ \_ in \_ *pConnectionInfo->dwFlags*, non verrà visualizzata alcuna finestra di dialogo e la chiamata avrà esito negativo.

Se il driver della stampante locale può essere usato per eseguire il rendering dei processi di stampa per questa stampante e la versione del driver locale non deve corrispondere alla versione del driver della stampante nel server, impostare PRINTER \_ CONNECTION \_ MISMATCH in *pConnectionInfo->dwFlags* e assegnare il puntatore a una variabile stringa contenente il percorso del driver della stampante locale *su pConnectionInfo->pszDriverName*.

Una connessione stampante stabilita chiamando **AddPrinterConnection2** verrà enumerata quando [**EnumPrinters**](enumprinters.md) viene chiamato con *dwType* impostato su PRINTER \_ ENUM \_ CONNECTION.

La versione ANSI di questa funzione, **AddPrinterConnection2A,** non è supportata e restituisce **ERROR NOT \_ \_ SUPPORTED.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddPrinterConnection2W** (Unicode)<br/>                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> <dt>

[**Enumprinters**](enumprinters.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> </dl>

 

