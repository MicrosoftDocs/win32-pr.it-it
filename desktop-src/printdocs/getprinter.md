---
description: La funzione GetPrinter recupera informazioni su una stampante specificata.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: Funzione GetPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: b6823795ea715ac72dfdb7150dac08fd7feb34445fcfab94412cb2dd0c6bd7a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949090"
---
# <a name="getprinter-function"></a>Funzione GetPrinter

La **funzione GetPrinter** recupera informazioni su una stampante specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante per cui la funzione recupera informazioni. Usare la [**funzione OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Livello o tipo di struttura archiviato dalla funzione nel buffer a cui *punta pPrinter.*

Questo valore può essere 1, 2, 3, 4, 5, 6, 7, 8 o 9.

</dd> <dt>

*pPrinter* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve una struttura contenente informazioni sulla stampante specificata. Le dimensioni del buffer devono essere sufficienti per ricevere la struttura e le stringhe o altri dati a cui puntano i membri della struttura. Se il buffer è troppo piccolo, il *parametro pcbNeeded* restituisce le dimensioni del buffer richieste.

Il tipo di struttura è determinato dal valore di *Level.*



| Level                                                                                                | Struttura                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Struttura [**PRINTER \_ INFO \_ 1**](printer-info-1.md) contenente informazioni generali sulla stampante.<br/>                                                                                                        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Struttura [**PRINTER \_ INFO \_ 2**](printer-info-2.md) contenente informazioni dettagliate sulla stampante.<br/>                                                                                             |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Struttura [**PRINTER \_ INFO \_ 3**](printer-info-3.md) contenente le informazioni di sicurezza della stampante.<br/>                                                                                                 |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Struttura [**PRINTER \_ INFO \_ 4**](printer-info-4.md) contenente informazioni minime sulla stampante, tra cui il nome della stampante, il nome del server e se la stampante è remota o locale.<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Struttura [**PRINTER \_ INFO \_ 5**](printer-info-5.md) contenente informazioni sulla stampante, ad esempio attributi della stampante e impostazioni di timeout.<br/>                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Struttura [**PRINTER \_ INFO \_ 6**](printer-info-6.md) che specifica il valore di stato di una stampante.<br/>                                                                                                      |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Struttura [**PRINTER \_ INFO \_ 7**](printer-info-7.md) che indica se la stampante è pubblicata nel servizio directory.<br/>                                                                      |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Struttura [**PRINTER \_ INFO \_ 8**](printer-info-8.md) che specifica le impostazioni predefinite globali della stampante.<br/>                                                                                                |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Struttura [**PRINTER \_ INFO \_ 9**](printer-info-9.md) che specifica le impostazioni predefinite della stampante per utente.<br/>                                                                                              |



 

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pPrinter.*

</dd> <dt>

*pcbNeeded* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile impostata dalla funzione sulla dimensione, in byte, delle informazioni della stampante. Se *cbBuf è* minore di questo valore, **GetPrinter** ha esito negativo e il valore rappresenta le dimensioni del buffer richieste. Se *cbBuf* è uguale o maggiore di questo valore, **GetPrinter** ha esito positivo e il valore rappresenta il numero di byte archiviati nel buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Il **membro pDevMode** nelle strutture [**PRINTER INFO \_ \_ 2**](printer-info-2.md), [**PRINTER INFO \_ \_ 8**](printer-info-8.md)e [**PRINTER INFO \_ \_ 9**](printer-info-9.md) può essere **NULL.** In questo caso, la stampante è inutilizzabile fino a quando il driver non viene reinstallato correttamente.

Per le strutture [**PRINTER \_ INFO \_ 2**](printer-info-2.md) e [**PRINTER INFO \_ \_ 3**](printer-info-3.md) che contengono un puntatore a un descrittore di sicurezza, la funzione recupera solo i componenti del descrittore di sicurezza che il chiamante è autorizzato a leggere. Per recuperare determinati componenti del descrittore di sicurezza, è necessario specificare i diritti di accesso necessari quando si chiama la [**funzione OpenPrinter**](openprinter.md) per recuperare un handle per la stampante. La tabella seguente illustra i diritti di accesso necessari per leggere i vari componenti del descrittore di sicurezza.



| Diritto di accesso                        | Componente descrittore di sicurezza                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| CONTROLLO \_ DI LETTURA<br/>            | Proprietario<br/> Gruppo primario<br/> Elenco di controllo di accesso discrezionale (DACL)<br/> |
| ACCESSO \_ ALLA SICUREZZA DEL \_ SISTEMA<br/> | Elenco di controllo di accesso di sistema (SACL)<br/>                                                  |



 

Se si specifica il livello 7, il **membro dwAction** di [**PRINTER INFO \_ \_ 7**](printer-info-7.md) restituisce uno dei valori seguenti per indicare se la stampante è pubblicata nel servizio directory.



| Valore dwAction     | Significato                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PUBBLICAZIONE \_ DSPRINT   | La stampante viene pubblicata. Il **membro pszObjectGUID** contiene il GUID dell'oggetto coda di stampa dei servizi directory associato alla stampante.                                                                                                       |
| DSPRINT \_ UNPUBLISH | La stampante non è pubblicata.                                                                                                                                                                                                                            |
| DSPRINT \_ IN SOSPESO   | Indica che il sistema sta tentando di completare un'operazione di pubblicazione o annullamento della pubblicazione. Se una [**chiamata a SetPrinter**](setprinter.md) non riesce a pubblicare o annullare la pubblicazione di una stampante, il sistema tenta di completare l'operazione in background. |



 

A partire da Windows Vista, i dati della stampante restituiti da **GetPrinter** vengono recuperati da una cache locale quando *hPrinter* fa riferimento a una stampante ospitata da un server di stampa ed è presente almeno una connessione aperta al server di stampa. In tutte le altre configurazioni, i dati della stampante vengono sottoposti a query dal server di stampa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **GetPrinterW** (Unicode) e **GetPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AbortPrinter**](abortprinter.md)
</dt> <dt>

[**Addprinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**Enumprinters**](enumprinters.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 1**](printer-info-1.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 3**](printer-info-3.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 4**](printer-info-4.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 5**](printer-info-5.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 7**](printer-info-7.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 8**](printer-info-8.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 9**](printer-info-9.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> </dl>

 

 




