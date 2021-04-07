---
description: La funzione AdvancedDocumentProperties Visualizza una finestra di dialogo di configurazione della stampante per la stampante specificata, consentendo all'utente di configurare la stampante.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: Funzione AdvancedDocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759560"
---
# <a name="advanceddocumentproperties-function"></a>AdvancedDocumentProperties (funzione)

La funzione **AdvancedDocumentProperties** Visualizza una finestra di dialogo di configurazione della stampante per la stampante specificata, consentendo all'utente di configurare la stampante.

Questa funzione è un caso speciale della funzione [**DocumentProperties**](documentproperties.md) . Per ulteriori informazioni, vedere la sezione Osservazioni.

## <a name="syntax"></a>Sintassi


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle per la finestra padre della finestra di dialogo Printer-Configuration.

</dd> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per un oggetto Printer. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pDeviceName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del dispositivo per il quale deve essere visualizzata una finestra di dialogo di configurazione della stampante.

</dd> <dt>

*pDevModeOutput* \[ out\]
</dt> <dd>

Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che conterrà i dati di configurazione specificati dall'utente.

</dd> <dt>

*pDevModeInput* \[ in\]
</dt> <dd>

Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che contiene i dati di configurazione utilizzati per inizializzare i controlli della finestra di dialogo di configurazione della stampante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione [**DocumentProperties**](documentproperties.md) con questi parametri ha esito positivo, il valore restituito di **AdvancedDocumentProperties** è 1. In caso contrario, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Questa funzione può visualizzare solo la finestra di dialogo di configurazione della stampante, in modo che un utente possa configurarla. Per un maggiore controllo, usare [**DocumentProperties**](documentproperties.md). I parametri di input per questa funzione vengono passati direttamente a **DocumentProperties** e il valore *fmode* è impostato su DM \_ in \_ buffer \| DM \_ in \_ prompt \| DM \_ out \_ buffer. A differenza di **DocumentProperties**, questa funzione restituisce solo 1 o 0. Pertanto, non è possibile determinare la dimensione richiesta di [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) impostando *pDevMode* su zero.

Un'applicazione può ottenere il nome a cui punta il parametro *pDeviceName* chiamando la funzione [**GetPrinter**](getprinter.md) e quindi esaminando il membro **pPrinterName** della struttura [**Printer \_ info \_ 2**](printer-info-2.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AdvancedDocumentPropertiesW** (Unicode) e **AdvancedDocumentPropertiesA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**DocumentProperties**](documentproperties.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




