---
description: La funzione EnumPrinterData enumera i dati di configurazione per una stampante specificata.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Funzione EnumPrinterData (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a542b6a0432ccf7065d94eeb8ebb3acbd8e2ace22044f2cc8984a1f4b2404299
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846081"
---
# <a name="enumprinterdata-function"></a>Funzione EnumPrinterData

La **funzione EnumPrinterData** enumera i dati di configurazione per una stampante specificata.

Per recuperare i dati di configurazione in una singola chiamata, usare la [**funzione EnumPrinterDataEx.**](enumprinterdataex.md)

## <a name="syntax"></a>Sintassi


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante i cui dati di configurazione devono essere ottenuti. Usare la [**funzione OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*dwIndex* \[ Pollici\]
</dt> <dd>

Valore di indice che specifica il valore dei dati di configurazione da recuperare.

Impostare questo parametro su zero per la prima chiamata a **EnumPrinterData per** un handle di stampante specificato. Incrementare quindi il parametro di uno per le chiamate successive che coinvolgono la stessa stampante, fino a quando la funzione non restituisce ERROR \_ NO \_ MORE \_ ITEMS. Per altre informazioni, vedere la sezione Osservazioni seguente.

Se si usa la tecnica indicata nelle descrizioni dei parametri *cbValueName* e *cbData* per ottenere valori adeguati per le dimensioni del buffer, impostando entrambi i parametri su zero in una prima chiamata a **EnumPrinterData** per un handle di stampante specificato, il valore *di dwIndex* non è importante per tale chiamata. Impostare *dwIndex su* zero nella chiamata successiva a **EnumPrinterData** per avviare il processo di enumerazione effettivo.

I valori dei dati di configurazione non vengono ordinati. I nuovi valori avranno un indice arbitrario. Ciò significa che la **funzione EnumPrinterData** può restituire valori in qualsiasi ordine.

</dd> <dt>

*pValueName* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve il nome del valore dei dati di configurazione, incluso un carattere Null di terminazione.

</dd> <dt>

*cbValueName* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pValueName.*

Se si vuole che il sistema operativo fornisse una dimensione del buffer adeguata, impostare sia questo parametro che il parametro *cbData* su zero per la prima chiamata a **EnumPrinterData** per un handle di stampante specificato. Quando la funzione viene restituita, la variabile a cui punta *pcbValueName* conterrà una dimensione del buffer sufficientemente grande da enumerare correttamente tutti i nomi dei valori dei dati di configurazione della stampante.

</dd> <dt>

*pcbValueName* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte archiviati nel buffer a cui *punta pValueName*.

</dd> <dt>

*pType* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve un codice che indica il tipo di dati archiviati nel valore specificato. Per un elenco dei codici di tipo possibili, vedere Tipi [di valori del Registro di sistema](/windows/desktop/SysInfo/registry-value-types). Il *parametro pType* può essere **NULL** se il codice del tipo non è obbligatorio.

</dd> <dt>

*pData* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve il valore dei dati di configurazione.

Questo parametro può essere **NULL se** il valore dei dati di configurazione non è obbligatorio.

</dd> <dt>

*cbData* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pData.*

Se si vuole che il sistema operativo fornisse una dimensione del buffer adeguata, impostare sia questo parametro che il parametro *cbValueName* su zero per la prima chiamata a **EnumPrinterData** per un handle di stampante specificato. Quando la funzione viene restituita, la variabile a cui punta *pcbData* conterrà dimensioni del buffer sufficientemente grandi da enumerare correttamente tutti i nomi dei valori dei dati di configurazione della stampante.

</dd> <dt>

*pcbData* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte archiviati nel buffer a cui punta *pData*.

Questo parametro può essere **NULL** se *pData* è **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore di sistema.

La funzione restituisce ERROR NO MORE ITEMS quando non sono presenti altri valori di dati di configurazione \_ da recuperare per un handle di stampante \_ \_ specificato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

**EnumPrinterData** recupera i dati di configurazione della stampante impostati dalla [**funzione SetPrinterData.**](setprinterdata.md) I dati di configurazione di una stampante sono costituiti da un set di valori denominati e tipidati. La **funzione EnumPrinterData** ottiene uno di questi valori e il relativo nome e un codice di tipo, ogni volta che viene chiamato. Chiamare la **funzione EnumPrinterData** più volte in successione per ottenere tutti i valori dei dati di configurazione di una stampante.

I dati di configurazione della stampante vengono archiviati nel Registro di sistema. Durante l'enumerazione dei dati di configurazione della stampante, è consigliabile evitare di chiamare funzioni del Registro di sistema che potrebbero modificare i dati.

Per fare in modo che il sistema operativo fornisse una dimensione del buffer adeguata, chiamare **prima EnumPrinterData** con entrambi i parametri *cbValueName* e *cbData* impostati su zero, come illustrato in precedenza nella sezione Parametri. Il valore *di dwIndex* non è importante per questa chiamata. Quando la funzione viene restituita, \* *pcbValueName* e \* *pcbData* conterranno dimensioni del buffer sufficientemente grandi da enumerare tutti i nomi e i valori dei valori dei dati di configurazione della stampante. Nella chiamata successiva allocare il nome del valore e i buffer di dati, impostare *cbValueName* e *cbData* sulle dimensioni in byte dei buffer allocati e *impostare dwIndex* su zero. Successivamente, continuare a chiamare la funzione **EnumPrinterData,** incrementando *dwIndex* di uno ogni volta, fino a quando la funzione non restituisce ERROR \_ NO MORE \_ \_ ITEMS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumPrinterDataW** (Unicode) ed **EnumPrinterDataA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterData**](deleteprinterdata.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> </dl>

 

