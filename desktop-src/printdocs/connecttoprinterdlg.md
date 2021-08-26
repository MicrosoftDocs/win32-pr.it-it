---
description: La funzione ConnectToPrinterDlg visualizza una finestra di dialogo che consente agli utenti di esplorare e connettersi alle stampanti in una rete.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: Funzione ConnectToPrinterDlg (Winspool.h)
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
ms.openlocfilehash: f7bbeda17f5cbafa46785577243df9e50b3bf7109631166ffb8894bbb678393e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950431"
---
# <a name="connecttoprinterdlg-function"></a>Funzione ConnectToPrinterDlg

La **funzione ConnectToPrinterDlg** visualizza una finestra di dialogo che consente agli utenti di esplorare e connettersi alle stampanti in una rete. Se l'utente seleziona una stampante, la funzione tenta di crearne una connessione. se nel server non è installato un driver appropriato, all'utente viene data la possibilità di creare una stampante in locale.

## <a name="syntax"></a>Sintassi


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwnd* \[ Pollici\]
</dt> <dd>

Specifica la finestra padre della finestra di dialogo.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo e l'utente seleziona una stampante, il valore restituito è un handle per la stampante selezionata.

Se la funzione ha esito negativo o l'utente annulla la finestra di dialogo senza selezionare una stampante, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

La **funzione ConnectToPrinterDlg** tenta di creare una connessione alla stampante selezionata. Tuttavia, se nel server in cui risiede la stampante non è installato un driver appropriato, la funzione offre all'utente la possibilità di creare una stampante in locale. Un'applicazione chiamante può determinare se la funzione ha creato una stampante in locale chiamando [**GetPrinter**](getprinter.md) con una struttura [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) quindi esaminando il membro **Attributes di tale** struttura.

Un'applicazione deve chiamare [**DeletePrinter**](deleteprinter.md) per eliminare una stampante locale. Un'applicazione deve chiamare [**DeletePrinterConnection**](deleteprinterconnection.md) per eliminare una connessione a una stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |



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

[**INFORMAZIONI \_ STAMPANTE \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




