---
description: La funzione DocumentProperties recupera o modifica le informazioni di inizializzazione della stampante o visualizza una finestra delle proprietà di configurazione della stampante per la stampante specificata.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: Funzione DocumentProperties (Winspool.h)
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
ms.openlocfilehash: 349a085cc8f55f391b33dd5048d23a35fdac3c2b33b3771290bcecd9fdbcfc8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235108"
---
# <a name="documentproperties-function"></a>Funzione DocumentProperties

La **funzione DocumentProperties** recupera o modifica le informazioni di inizializzazione della stampante o visualizza una finestra delle proprietà di configurazione della stampante per la stampante specificata.

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

*hWnd* \[ Pollici\]
</dt> <dd>

Handle per la finestra padre della finestra delle proprietà printer-configuration.

</dd> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per un oggetto stampante. Usare la [**funzione OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*pDeviceName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del dispositivo per cui viene visualizzata la finestra delle proprietà di configurazione della stampante.

</dd> <dt>

*pDevModeOutput* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che riceve i dati di configurazione della stampante specificati dall'utente.

</dd> <dt>

*pDevModeInput* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) utilizzata dal sistema operativo per inizializzare i controlli della finestra delle proprietà.

Questo parametro viene usato solo se il flag **\_ DM IN \_ BUFFER** è impostato nel *parametro fMode.* Se **DM \_ IN \_ BUFFER** non è impostato, il sistema operativo usa [**devMODE predefinito della stampante.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)

</dd> <dt>

*fMode* \[ Pollici\]
</dt> <dd>

Operazioni eseguite dalla funzione. Se questo parametro è zero, la **funzione DocumentProperties** restituisce il numero di byte richiesti dalla struttura di dati [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) del driver della stampante. In caso contrario, usare una o più delle costanti seguenti per costruire un valore per questo parametro. Si noti, tuttavia, che per modificare le impostazioni di stampa, un'applicazione deve specificare almeno un valore di input e un valore di output.



| Valore                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <dt>**DM \_ IN \_ BUFFER**</dt> </dl>    | Valore di input. Prima di richiedere, copiare o aggiornare, la funzione unisce le impostazioni di stampa correnti del driver della stampante con le impostazioni nella struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) specificata dal *parametro pDevModeInput.* La funzione aggiorna la struttura solo per i membri specificati dal membro **dmFields** della struttura **DEVMODE.** Questo valore è definito anche **come DM \_ MODIFY.** In caso di conflitto durante l'unione, le impostazioni nella struttura **DEVMODE** specificata da *pDevModeInput* sostituiscono le impostazioni di stampa correnti del driver della stampante.<br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <dt>**RICHIESTA \_ DM IN \_**</dt> </dl>    | Valore di input. La funzione presenta la finestra delle proprietà Imposta stampa del driver della stampante e quindi modifica le impostazioni nella struttura dei dati [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) della stampante in base ai valori specificati dall'utente. Questo valore è definito anche come **DM \_ PROMPT**.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <dt>**DM \_ OUT \_ BUFFER**</dt> </dl> | Valore di output. La funzione scrive le impostazioni di stampa correnti del driver della stampante, inclusi i dati privati, nella struttura di dati [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) specificata dal *parametro pDevModeOutput.* Il chiamante deve allocare un buffer sufficientemente grande per contenere le informazioni. Se il bit **DM \_ OUT BUFFER \_ set** è chiaro, il *parametro pDevModeOutput* può essere **NULL.** Questo valore è definito anche come **DM \_ COPY.**<br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il *parametro fMode* è zero, il valore restituito è la dimensione del buffer necessaria per contenere i dati di inizializzazione del driver della stampante. Si noti che questo buffer può essere maggiore di [**una struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) se il driver della stampante aggiunge dati privati alla struttura .

Se la funzione visualizza la finestra delle proprietà, il valore restituito è **IDOK** o **IDCANCEL,** a seconda del pulsante selezionato dall'utente.

Se la funzione non visualizza la finestra delle proprietà e ha esito positivo, il valore restituito è **IDOK**.

Se la funzione ha esito negativo, il valore restituito è minore di zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

La stringa a cui punta il *parametro pDeviceName* può essere ottenuta chiamando la [**funzione GetPrinter.**](getprinter.md)

La [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) effettivamente usata da un driver della stampante contiene la parte indipendente dal dispositivo (come definito in precedenza) seguita da una parte specifica del driver che varia in base alle dimensioni e al contenuto di ogni driver e versione del driver. A causa di questa dipendenza del driver, è molto importante per le applicazioni eseguire query sul driver per ottenere le dimensioni corrette della **struttura DEVMODE** prima di allocare un buffer.

**Per apportare modifiche alle impostazioni di stampa locali di un'applicazione, un'applicazione deve seguire questa procedura:**

1.  Ottenere il numero di byte necessari per la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa chiamando **DocumentProperties** e specificando zero nel *parametro fMode.*
2.  Allocare memoria per la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa.
3.  Ottenere le impostazioni correnti della stampante chiamando **DocumentProperties**. Passare un puntatore alla [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) allocata nel passaggio 2 come *parametro pDevModeOutput* e specificare il **valore DM OUT \_ \_ BUFFER.**
4.  Modificare i membri appropriati della struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituita e indicare quali membri sono stati modificati impostando i bit corrispondenti nel membro **dmFields** di **DEVMODE**.
5.  Chiamare **DocumentProperties** e passare di nuovo la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) modificata come parametri *pDevModeInput* e *pDevModeOutput* e specificare entrambi i valori **DM IN \_ \_ BUFFER** e **DM OUT \_ \_ BUFFER** (combinati con l'operatore OR). La **struttura DEVMODE** restituita dalla terza chiamata a **DocumentProperties** può essere usata come argomento in una chiamata alla [**funzione CreateDC.**](/windows/desktop/api/wingdi/nf-wingdi-createdca)

Per creare un handle per un contesto stampante-dispositivo usando le impostazioni correnti della stampante, è necessario chiamare due volte **DocumentProperties,** come descritto in precedenza. La prima chiamata ottiene le dimensioni dell'intero [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) e la seconda chiama inizializza **DEVMODE** con le impostazioni correnti della stampante. Passare **devMODE** inizializzato a [**CreateDC per**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ottenere l'handle per il contesto di dispositivo della stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
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

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

