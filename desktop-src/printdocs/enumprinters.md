---
description: La funzione EnumPrinters enumera le stampanti disponibili, i server di stampa, i domini o i provider di stampa.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Funzione EnumPrinters (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6d82e8e6ff4f56a3c67fa29c48e982ebe0fd4599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881614"
---
# <a name="enumprinters-function"></a>EnumPrinters (funzione)

La funzione **EnumPrinters** enumera le stampanti disponibili, i server di stampa, i domini o i provider di stampa.

## <a name="syntax"></a>Sintassi


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipi di oggetti di stampa che la funzione deve enumerare. Questo valore può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <dt>**\_enumerazione stampante \_ locale**</dt> </dl>                       | Se \_ \_ non viene passato anche il flag del nome enum della stampante, la funzione ignora il parametro *Name* ed enumera le stampanti installate localmente. Se \_ viene passato anche il nome dell'enum della stampante \_ , la funzione enumera le stampanti locali nel *nome*. <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <dt>**\_Nome enum \_ stampante**</dt> </dl>                          | La funzione enumera la stampante identificata in base al *nome*. Può trattarsi di un server, di un dominio o di un provider di stampa. Se *Name* è **null**, la funzione enumera i provider di stampa disponibili.<br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <dt>**\_enumerazione stampante \_ condivisa**</dt> </dl>                    | La funzione enumera le stampanti che dispongono dell'attributo Shared. Non può essere usato in isolamento; utilizzare un'operazione o per combinare con un altro \_ tipo di enumerazione Printer.<br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <dt>**\_connessioni enum \_ stampanti**</dt> </dl>     | La funzione enumera l'elenco di stampanti a cui l'utente ha eseguito le connessioni precedenti.<br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <dt>**\_rete enum \_ Printer**</dt> </dl>                 | La funzione enumera le stampanti di rete nel dominio del computer. Questo valore è valido solo se *Level* è 1.<br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <dt>**\_enumerazione stampanti \_ Remote**</dt> </dl>                    | La funzione enumera le stampanti di rete e i server di stampa nel dominio del computer. Questo valore è valido solo se *Level* è 1.<br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <dt>**\_Categoria enumerazione \_ stampanti \_ 3D**</dt> </dl>    | La funzione enumera solo le stampanti 3D.<br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <dt>**\_categoria enum \_ stampanti \_ All**</dt> </dl> | La funzione enumera tutti i dispositivi di stampa, incluse le stampanti 3D.<br/>                                                                                                                                                                           |



 

Se *Level* è 4, è possibile utilizzare solo le \_ \_ costanti locali Printer enum Connections e Printer \_ enum \_ .

> [!Note]  
> i dispositivi di stampa 3D non vengono enumerati per impostazione predefinita. Per enumerare solo le stampanti 3D, è necessario includere sia la **\_ categoria di enumerazione stampanti \_ \_ 3D** che la **stampante \_ enum \_ local** . Per includere stampanti 3D, insieme a tutte le altre stampanti locali, utilizzare **Printer \_ enum \_ Category \_ All** e **Printer \_ enum \_ local**.

 

</dd> <dt>

*Nome* \[ in\]
</dt> <dd>

Se *Level* è 1, *Flags* contiene \_ il nome enum della stampante \_ e il *nome* è diverso da **null**, il *nome* è un puntatore a una stringa con terminazione null che specifica il nome dell'oggetto da enumerare. Questa stringa può essere il nome di un server, di un dominio o di un provider di stampa.

Se *Level* è 1, *Flags* contiene \_ il nome enum della stampante \_ e *Name* è **null**, la funzione enumera i provider di stampa disponibili.

Se *Level* è 1, *Flags* contiene Printer \_ enum \_ remote e *Name* è **null**, la funzione enumera le stampanti nel dominio dell'utente.

Se *Level* è 2 o 5,*Name* è un puntatore a una stringa con terminazione null che specifica il nome di un server di cui è necessario enumerare le stampanti. Se questa stringa è **null**, la funzione enumera le stampanti installate nel computer locale.

Se *Level* è 4, il *nome* deve essere **null**. La funzione esegue sempre query sul computer locale.

Quando *Name* è **null**, l'impostazione dei *flag* per Printer \_ enum \_ Local \| Printer \_ enum \_ Connections enumera le stampanti installate nel computer locale. Queste stampanti includono quelle fisicamente collegate al computer locale e le stampanti remote a cui ha una connessione di rete.

Quando il *nome* non è **null**, l'impostazione dei *flag* sul \_ \_ Nome enum della stampante locale enum \| \_ \_ enumera le stampanti locali installate nel *nome* del server.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Tipo di strutture di dati a cui punta *pPrinterEnum*. I valori validi sono 1, 2, 4 e 5, che corrispondono alle strutture di dati Printer Info [**\_ \_ 1**](printer-info-1.md), [**Printer \_ info \_ 2**](printer-info-2.md) , [**Printer \_ info \_ 4**](printer-info-4.md)e [**Printer \_ info \_ 5**](printer-info-5.md) .

Questo valore può essere 1, 2, 4 o 5.

</dd> <dt>

*pPrinterEnum* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di strutture di informazioni stampante [**\_ \_ 1**](printer-info-1.md), [**\_ informazioni stampante \_ 2**](printer-info-2.md), [**\_ informazioni stampante \_ 4**](printer-info-4.md)o [**stampanti \_ \_ 5**](printer-info-5.md) . Ogni struttura contiene dati che descrivono un oggetto Print disponibile.

Se *Level* è 1, la matrice contiene le strutture delle [**informazioni di stampa \_ \_ 1**](printer-info-1.md) . Se *Level* è 2, la matrice contiene le strutture [**\_ info \_ 2 della stampante**](printer-info-2.md) . Se *Level* è 4, la matrice contiene le strutture delle [**informazioni di stampa \_ \_ 4**](printer-info-4.md) . Se *Level* è 5, la matrice contiene le strutture [**info della stampante \_ \_ 5**](printer-info-5.md) .

Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture di dati e qualsiasi stringa o altri dati a cui puntano i membri della struttura. Se il buffer è troppo piccolo, il parametro *pcbNeeded* restituisce le dimensioni del buffer richieste.

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pPrinterEnum*.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a un valore che riceve il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntatore a un valore che riceve il numero di strutture per le informazioni sulle stampanti [**\_ \_ 1**](printer-info-1.md), le informazioni sulla stampante [**\_ \_ 2**](printer-info-2.md) , le informazioni sulla stampante [**\_ \_ 4**](printer-info-4.md)o le [**informazioni della stampante \_ \_ 5**](printer-info-5.md) che la funzione restituisce nella matrice a cui punta *pPrinterEnum* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Non chiamare questo metodo in [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Se **EnumPrinters** restituisce una struttura [**Printer \_ info \_ 1**](printer-info-1.md) in cui \_ è specificato il contenitore enum della stampante \_ , significa che esiste una gerarchia di oggetti Printer. Un'applicazione può enumerare la gerarchia chiamando di nuovo **EnumPrinters** , impostando *Name* sul valore del membro **pname** della struttura **Printer \_ info \_ 1** .

La funzione **EnumPrinters** non recupera le informazioni di sicurezza. Se le strutture [**\_ info \_ 2 della stampante**](printer-info-2.md) vengono restituite nella matrice a cui punta *PPrinterEnum*, i relativi membri *pSecurityDescriptor* verranno impostati su **null**.

Per ottenere informazioni sulla stampante predefinita, chiamare [**GetDefaultPrinter**](getdefaultprinter.md).

La struttura delle [**informazioni di stampa \_ \_ 4**](printer-info-4.md) fornisce un metodo semplice ed estremamente rapido per recuperare i nomi delle stampanti installate in un computer locale, nonché le connessioni remote stabilite da un utente. Quando **EnumPrinters** viene chiamato con una struttura di dati **Printer \_ info \_ 4** , tale funzione esegue una query sul Registro di sistema per ottenere le informazioni specificate, quindi restituisce immediatamente un risultato. Questo comportamento è diverso da quello di **EnumPrinters** quando viene chiamato con altri livelli di **informazioni sulle stampanti \_ \_ \* *_ strutture dei dati. In particolare, quando _* EnumPrinters** viene chiamato con una struttura di dati di livello 2 ([**Printer \_ info \_ 2**](printer-info-2.md)), esegue una chiamata [**OpenPrinter**](openprinter.md) su ogni connessione remota. Se una connessione remota non è attiva o il server remoto non esiste più oppure la stampante remota non esiste più, la funzione deve attendere il timeout di RPC e, di conseguenza, interrompere la chiamata **OpenPrinter** . L'operazione può richiedere un po' di tempo. Il passaggio di una struttura **Printer \_ info \_ 4** consente a un'applicazione di recuperare un minimo di informazioni obbligatorie; se si desidera ottenere informazioni più dettagliate, è possibile effettuare una chiamata di **EnumPrinters** Level 2 successiva.

**Windows Vista:** I dati della stampante restituiti da **EnumPrinters** vengono recuperati da una cache locale quando il valore di *Level* è 4.

La tabella seguente mostra l'output di **EnumPrinters** per i diversi valori di *flag* quando il parametro *Level* è impostato su 1.

Nella colonna parametro *nome* della tabella è necessario sostituire un nome appropriato per provider di stampa, dominio e computer. Per "Print Provider", ad esempio, è possibile utilizzare il nome del provider di stampa di rete o il nome del provider di stampa locale. Per recuperare i nomi dei provider di stampa, chiamare **EnumPrinters** con il *nome* impostato su **null**.



| *Flags* -parametro                                  | Parametro del *nome*                            | Risultato                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| PRINTER \_ enum \_ locale (e non \_ Nome enum Printer \_ ) | Il parametro *Name* viene ignorato.<br/> | Tutte le stampanti locali.<br/>                                                                    |
| \_Nome enum \_ stampante                                | "Provider di stampa"<br/>                 | Tutti i nomi di dominio<br/>                                                                       |
| \_Nome enum \_ stampante                                | "Provider di stampa! Dominio<br/>          | Tutte le stampanti e i server di stampa nel dominio del computer<br/>                                |
| \_Nome enum \_ stampante                                | "Provider di stampa!! \\ \\ Macchina<br/>    | Tutte le stampanti condivise nel \\ \\ computer<br/>                                                     |
| \_Nome enum \_ stampante                                | Una stringa vuota ""<br/>              | Tutte le stampanti locali.<br/>                                                                    |
| \_Nome enum \_ stampante                                | **NULL**<br/>                         | Tutti i provider di stampa nel dominio del computer<br/>                                           |
| \_connessioni enum \_ stampanti                         | Il parametro *Name* viene ignorato.<br/> | Tutte le stampanti remote connesse<br/>                                                          |
| \_rete enum \_ Printer                             | Il parametro *Name* viene ignorato.<br/> | Tutte le stampanti nel dominio del computer<br/>                                                  |
| \_enumerazione stampanti \_ Remote                              | Una stringa vuota ""<br/>              | Tutte le stampanti e i server di stampa nel dominio del computer<br/>                                |
| \_enumerazione stampanti \_ Remote                              | "Provider di stampa"<br/>                 | Uguale al \_ Nome enum della stampante \_<br/>                                                            |
| \_enumerazione stampanti \_ Remote                              | "Provider di stampa! Dominio<br/>          | Tutte le stampanti e i server di stampa nel dominio del computer, indipendentemente dal *dominio* specificato.<br/> |
| \_Categoria enumerazione \_ stampanti \_ 3D                        | Il parametro *Name* viene ignorato.<br/> | Vengono enumerate solo le stampanti 3D.<br/>                                                       |
| \_categoria enum \_ stampanti \_ All                       | Il parametro *Name* viene ignorato.<br/> | le stampanti 3D vengono enumerate insieme a tutte le altre stampanti.<br/>                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumPrintersW** (Unicode) e **EnumPrintersA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**\_Informazioni stampante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Informazioni stampante \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_Informazioni stampante \_ 5**](printer-info-5.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

