---
description: La funzione GetPrinter recupera le informazioni su una stampante specificata.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: Funzione GetPrinter (winspool. h)
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
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318035"
---
# <a name="getprinter-function"></a>GetPrinter (funzione)

La funzione **GetPrinter** recupera le informazioni su una stampante specificata.

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

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante per il quale la funzione recupera le informazioni. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Il livello o il tipo di struttura archiviato dalla funzione nel buffer a cui punta *pPrinter*.

Questo valore può essere 1, 2, 3, 4, 5, 6, 7, 8 o 9.

</dd> <dt>

*pPrinter* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una struttura contenente informazioni sulla stampante specificata. Il buffer deve essere sufficientemente grande da ricevere la struttura e tutte le stringhe o altri dati a cui puntano i membri della struttura. Se il buffer è troppo piccolo, il parametro *pcbNeeded* restituisce le dimensioni del buffer richieste.

Il tipo di struttura è determinato dal valore di *Level*.



| Level                                                                                                | Struttura                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Una [**struttura \_ con \_ informazioni generali sulla stampante.**](printer-info-1.md)<br/>                                                                                                        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Struttura [**di \_ info \_ 2 della stampante**](printer-info-2.md) che contiene informazioni dettagliate sulla stampante.<br/>                                                                                             |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Struttura [**di \_ informazioni \_ sulla stampante 3**](printer-info-3.md) contenente le informazioni di sicurezza della stampante.<br/>                                                                                                 |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Struttura [**di \_ informazioni \_ di stampa 4**](printer-info-4.md) contenente informazioni minime sulla stampante, tra cui il nome della stampante, il nome del server e l'eventuale presenza di una stampante remota o locale.<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Struttura [**di \_ informazioni \_ sulla stampante 5**](printer-info-5.md) che contiene informazioni sulla stampante, ad esempio attributi della stampante e impostazioni di timeout.<br/>                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Struttura della [**stampante \_ info \_ 6**](printer-info-6.md) che specifica il valore di stato di una stampante.<br/>                                                                                                      |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Struttura [**di \_ info \_ 7 della stampante**](printer-info-7.md) che indica se la stampante è pubblicata nel servizio directory.<br/>                                                                      |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Una struttura di [**\_ Info stampa \_ 8**](printer-info-8.md) che specifica le impostazioni della stampante predefinite globali.<br/>                                                                                                |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Struttura [**Printer \_ info \_ 9**](printer-info-9.md) che specifica le impostazioni della stampante predefinite per utente.<br/>                                                                                              |



 

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pPrinter*.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a una variabile che la funzione imposta sulle dimensioni, in byte, delle informazioni sulla stampante. Se *cbBuf* è minore di questo valore, **GetPrinter** ha esito negativo e il valore rappresenta le dimensioni del buffer richieste. Se *cbBuf* è maggiore o uguale a questo valore, **GetPrinter** ha esito positivo e il valore rappresenta il numero di byte archiviati nel buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Il membro **pDevMode** nelle strutture Printer Info [**\_ \_ 2**](printer-info-2.md), [**Printer \_ info \_ 8**](printer-info-8.md)e [**Printer \_ info \_ 9**](printer-info-9.md) può essere **null**. In tal caso, la stampante è inutilizzabile fino a quando il driver non viene reinstallato correttamente.

Per le strutture [**Printer \_ info \_ 2**](printer-info-2.md) e [**Printer \_ info \_ 3**](printer-info-3.md) contenenti un puntatore a un descrittore di sicurezza, la funzione recupera solo i componenti del descrittore di sicurezza che il chiamante dispone delle autorizzazioni per la lettura. Per recuperare particolari componenti del descrittore di sicurezza, è necessario specificare i diritti di accesso necessari quando si chiama la funzione [**OpenPrinter**](openprinter.md) per recuperare un handle per la stampante. La tabella seguente illustra i diritti di accesso necessari per leggere i diversi componenti del descrittore di sicurezza.



| Diritto di accesso                        | Componente del descrittore di sicurezza                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| controllo di lettura \_<br/>            | Proprietario<br/> Gruppo primario<br/> Elenco di controllo di accesso discrezionale (DACL)<br/> |
| ACCESSO \_ alla \_ sicurezza del sistema<br/> | Elenco di controllo di accesso di sistema (SACL)<br/>                                                  |



 

Se si specifica Level 7, il membro **dwAction** di [**Printer \_ info \_ 7**](printer-info-7.md) restituisce uno dei valori seguenti per indicare se la stampante è pubblicata nel servizio directory.



| valore dwAction     | Significato                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_pubblicazione DSPRINT   | La stampante è pubblicata. Il membro **pszObjectGUID** contiene il GUID dell'oggetto coda di stampa dei servizi directory associato alla stampante.                                                                                                       |
| DSPRINT \_ annullare la pubblicazione | La stampante non è pubblicata.                                                                                                                                                                                                                            |
| DSPRINT \_ in sospeso   | Indica che il sistema sta tentando di completare un'operazione di pubblicazione o di Annulla pubblicazione. Se una chiamata del [**Seprinter**](setprinter.md) non riesce a pubblicare o annullare la pubblicazione di una stampante, il sistema tenta ulteriori tentativi di completare l'operazione in background. |



 

A partire da Windows Vista, i dati della stampante restituiti da **getprintable** viene recuperato da una cache locale quando *hPrinter* fa riferimento a una stampante ospitata da un server di stampa ed è presente almeno una connessione aperta al server di stampa. In tutte le altre configurazioni, viene eseguita una query sui dati della stampante dal server di stampa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **GetPrinterW** (Unicode) e **getprintera** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AbortPrinter**](abortprinter.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**\_Informazioni stampante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Informazioni stampante \_ 3**](printer-info-3.md)
</dt> <dt>

[**\_Informazioni stampante \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_Informazioni stampante \_ 5**](printer-info-5.md)
</dt> <dt>

[**Informazioni sulla stampante \_ \_ 7**](printer-info-7.md)
</dt> <dt>

[**\_Informazioni stampante \_ 8**](printer-info-8.md)
</dt> <dt>

[**Informazioni sulla stampante \_ \_ 9**](printer-info-9.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




