---
description: La funzione ConnectToPrinterDlg Visualizza una finestra di dialogo che consente agli utenti di esplorare e connettersi alle stampanti in una rete.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: Funzione ConnectToPrinterDlg (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318036"
---
# <a name="connecttoprinterdlg-function"></a>ConnectToPrinterDlg (funzione)

La funzione **ConnectToPrinterDlg** Visualizza una finestra di dialogo che consente agli utenti di esplorare e connettersi alle stampanti in una rete. Se l'utente seleziona una stampante, la funzione tenta di crearvi una connessione. Se nel server non è installato un driver idoneo, all'utente viene offerta la possibilità di creare una stampante localmente.

## <a name="syntax"></a>Sintassi


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Specifica la finestra padre della finestra di dialogo.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Questo parametro è riservato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo e l'utente seleziona una stampante, il valore restituito è un handle per la stampante selezionata.

Se la funzione ha esito negativo o se l'utente annulla la finestra di dialogo senza selezionare una stampante, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

La funzione **ConnectToPrinterDlg** tenta di creare una connessione alla stampante selezionata. Tuttavia, se il server in cui risiede la stampante non dispone di un driver idoneo, la funzione offre all'utente la possibilità di creare una stampante localmente. Un'applicazione chiamante è in grado di determinare se la funzione ha creato localmente una stampante chiamando [**GetPrinter**](getprinter.md) con una struttura di [**\_ info \_ 2 della stampante**](printer-info-2.md) , quindi esaminando il membro degli **attributi** della struttura.

Per eliminare una stampante locale, un'applicazione deve chiamare [**DeletePrinter**](deleteprinter.md) . Un'applicazione deve chiamare [**DeletePrinterConnection**](deleteprinterconnection.md) per eliminare una connessione a una stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterConnection**](addprinterconnection.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




