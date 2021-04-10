---
description: La funzione DocumentProperties recupera o modifica le informazioni di inizializzazione della stampante o Visualizza una finestra delle proprietà di configurazione della stampante per la stampante specificata.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: Funzione DocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 732cb6901b444117d0599a2899327ebcb749cf74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131910"
---
# <a name="documentproperties-function"></a>DocumentProperties (funzione)

La funzione **DocumentProperties** Recupera o modifica le informazioni di inizializzazione della stampante o Visualizza una finestra delle proprietà di configurazione della stampante per la stampante specificata.

## <a name="syntax"></a>Sintassi


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle per la finestra padre della finestra delle proprietà di configurazione della stampante.

</dd> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per un oggetto Printer. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pDeviceName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del dispositivo per il quale viene visualizzata la finestra delle proprietà di configurazione della stampante.

</dd> <dt>

*pDevModeOutput* \[ out\]
</dt> <dd>

Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che riceve i dati di configurazione della stampante specificati dall'utente.

</dd> <dt>

*pDevModeInput* \[ in\]
</dt> <dd>

Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) utilizzata dal sistema operativo per inizializzare i controlli della finestra delle proprietà.

Questo parametro viene utilizzato solo se il flag **DM \_ in \_ buffer** è impostato nel parametro *fmode* . Se **DM \_ in \_ buffer** non è impostato, il sistema operativo usa la funzione [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)predefinita della stampante.

</dd> <dt>

*fmode* \[ in\]
</dt> <dd>

Operazioni eseguite dalla funzione. Se questo parametro è zero, la funzione **DocumentProperties** restituisce il numero di byte necessari per la struttura dei dati [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) del driver della stampante. In caso contrario, utilizzare una o più delle seguenti costanti per costruire un valore per questo parametro. Si noti, tuttavia, che per modificare le impostazioni di stampa, un'applicazione deve specificare almeno un valore di input e un valore di output.



| Valore                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <dt>**DM \_ in \_ buffer**</dt> </dl>    | Valore di input. Prima di richiedere, copiare o aggiornare, la funzione unisce le impostazioni di stampa correnti del driver della stampante con le impostazioni nella struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) specificata dal parametro *pDevModeInput* . La funzione aggiorna la struttura solo per i membri specificati dal membro **dmFields** della struttura **DEVMODE** . Questo valore è definito anche come **DM \_ Modify**. In caso di conflitto durante l'Unione, le impostazioni nella struttura **DEVMODE** specificata da *pDevModeInput* sostituiscono le impostazioni di stampa correnti del driver della stampante.<br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <dt>**DM \_ nella \_ richiesta**</dt> </dl>    | Valore di input. La funzione Visualizza la finestra delle proprietà di installazione di stampa del driver della stampante e quindi modifica le impostazioni nella struttura dei dati [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) della stampante in base ai valori specificati dall'utente. Questo valore viene definito anche come **\_ prompt DM**.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <dt>**\_buffer out \_ DM**</dt> </dl> | Valore di output. La funzione scrive le impostazioni di stampa correnti del driver della stampante, inclusi i dati privati, nella struttura di dati [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) specificata dal parametro *pDevModeOutput* . Il chiamante deve allocare un buffer sufficientemente grande per contenere le informazioni. Se il set **di \_ \_ buffer di bit DM out** è chiaro, il parametro *pDevModeOutput* può essere **null**. Questo valore è definito anche **\_ copia DM**.<br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il parametro *fmode* è zero, il valore restituito corrisponde alla dimensione del buffer necessaria per contenere i dati di inizializzazione del driver della stampante. Si noti che questo buffer può essere più grande di una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) se il driver della stampante aggiunge dati privati alla struttura.

Se la funzione Visualizza la finestra delle proprietà, il valore restituito è **IDOK** o **IDCANCEL**, a seconda del pulsante selezionato dall'utente.

Se la funzione non Visualizza la finestra delle proprietà e ha esito positivo, il valore restituito è **IDOK**.

Se la funzione ha esito negativo, il valore restituito è minore di zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

La stringa a cui punta il parametro *pDeviceName* può essere ottenuta chiamando la funzione [**GetPrinter**](getprinter.md) .

La struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) effettivamente utilizzata da un driver della stampante contiene la parte indipendente dal dispositivo (come definito in precedenza) seguita da una parte specifica del driver che varia in base alla dimensione e al contenuto con ogni driver e versione del driver. A causa di questa dipendenza del driver, è molto importante per le applicazioni eseguire una query sul driver per la corretta dimensione della struttura **DEVMODE** prima di allocare un buffer.

**Per apportare modifiche alle impostazioni di stampa locali per un'applicazione, è necessario eseguire le operazioni seguenti:**

1.  Ottenere il numero di byte necessari per la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa chiamando **DocumentProperties** e specificando zero nel parametro *fmode* .
2.  Allocare memoria per la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa.
3.  Ottenere le impostazioni della stampante correnti chiamando **DocumentProperties**. Passare un puntatore alla struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) allocata nel passaggio 2 come parametro *pDevModeOutput* e specificare il valore **del \_ \_ buffer out di DM** .
4.  Modificare i membri appropriati della struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituita e indicare i membri modificati impostando i bit corrispondenti nel membro **DmFields** dell'oggetto **DEVMODE**.
5.  Chiamare **DocumentProperties** e passare la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) modificata come entrambi i parametri *pDevModeInput* e *pDevModeOutput* e specificare sia il **DM \_ in \_ buffer** che i valori del **\_ \_ buffer out DM** (combinati con l'operatore OR). La struttura **DEVMODE** restituita dalla terza chiamata a **DocumentProperties** può essere utilizzata come argomento in una chiamata alla funzione [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) .

Per creare un handle per un contesto di dispositivo stampante usando le impostazioni della stampante correnti, è sufficiente chiamare **DocumentProperties** due volte, come descritto in precedenza. La prima chiamata ottiene le dimensioni dell'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completo e la seconda chiamata Inizializza il **DEVMODE** con le impostazioni della stampante correnti. Passare l'oggetto **DEVMODE** inizializzato a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) per ottenere l'handle per il contesto di dispositivo stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **DocumentPropertiesW** (Unicode) e **DocumentPropertiesA** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AdvancedDocumentProperties**](advanceddocumentproperties.md)
</dt> <dt>

[**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

