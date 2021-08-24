---
description: La funzione EnumPrinters enumera le stampanti, i server di stampa, i domini o i provider di stampa disponibili.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Funzione EnumPrinters (Winspool.h)
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
ms.openlocfilehash: fb88cef081010f1319fb194904933ba2366d6593f0d2517c696bb6d6490ace20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119353841"
---
# <a name="enumprinters-function"></a>Funzione EnumPrinters

La **funzione EnumPrinters** enumera le stampanti, i server di stampa, i domini o i provider di stampa disponibili.

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

*Flag* \[ Pollici\]
</dt> <dd>

Tipi di oggetti di stampa che la funzione deve enumerare. Questo valore può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <dt>**PRINTER \_ ENUM \_ LOCAL**</dt> </dl>                       | Se non viene passato anche il flag PRINTER ENUM NAME, la funzione ignora il parametro Name ed \_ \_ enumera le stampanti installate localmente.  Se viene passato anche PRINTER \_ ENUM \_ NAME, la funzione enumera le stampanti locali in *Name*. <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <dt>**NOME \_ DELL'ENUMERAZIONE \_ PRINTER**</dt> </dl>                          | La funzione enumera la stampante identificata da *Name*. Può trattarsi di un server, di un dominio o di un provider di stampa. Se *Name* è **NULL,** la funzione enumera i provider di stampa disponibili.<br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <dt>**ENUMERAZIONE \_ PRINTER \_ SHARED**</dt> </dl>                    | La funzione enumera le stampanti con l'attributo condiviso. Non può essere usato in isolamento. usare un'operazione OR da combinare con un altro tipo PRINTER \_ ENUM.<br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <dt>**CONNESSIONI \_ DI ENUMERAZIONE DELLA \_ STAMPANTE**</dt> </dl>     | La funzione enumera l'elenco di stampanti a cui l'utente ha effettuato connessioni precedenti.<br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <dt>**PRINTER \_ ENUM \_ NETWORK**</dt> </dl>                 | La funzione enumera le stampanti di rete nel dominio del computer. Questo valore è valido solo se *Level* è 1.<br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <dt>**PRINTER \_ ENUM \_ REMOTE**</dt> </dl>                    | La funzione enumera le stampanti di rete e i server di stampa nel dominio del computer. Questo valore è valido solo se *Level* è 1.<br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <dt>**PRINTER \_ ENUM \_ CATEGORY \_ 3D**</dt> </dl>    | La funzione enumera solo le stampanti 3D.<br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <dt>**CATEGORIA \_ PRINTER ENUM \_ \_ ALL**</dt> </dl> | La funzione enumera tutti i dispositivi di stampa, incluse le stampanti 3D.<br/>                                                                                                                                                                           |



 

Se *Level* è 4, è possibile usare solo le costanti PRINTER ENUM CONNECTIONS e \_ PRINTER \_ \_ ENUM \_ LOCAL.

> [!Note]  
> I dispositivi di stampa 3D non vengono enumerati per impostazione predefinita. È necessario includere **SIA PRINTER \_ ENUM CATEGORY \_ \_ 3D** che **PRINTER \_ ENUM \_ LOCAL** per enumerare solo le stampanti 3D. Per includere le stampanti 3D, insieme a tutte le altre stampanti locali, usare **PRINTER \_ ENUM \_ CATEGORY \_ ALL** e **PRINTER \_ ENUM \_ LOCAL**.

 

</dd> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Se *Level* è 1, *Flags* contiene PRINTER ENUM NAME e Name è diverso da NULL, Name è un puntatore a una stringa con terminazione Null che specifica il nome dell'oggetto \_ da \_ enumerare.    Questa stringa può essere il nome di un server, di un dominio o di un provider di stampa.

Se *Level* è 1, *Flags* contiene PRINTER ENUM NAME e Name è NULL, la funzione \_ enumera i provider di stampa \_ disponibili.  

Se *Level* è 1, *Flags* contiene PRINTER ENUM REMOTE e Name è NULL, la funzione enumera le stampanti nel \_ dominio \_ dell'utente.  

Se *Level* è 2 o 5,*Name* è un puntatore a una stringa con terminazione Null che specifica il nome di un server le cui stampanti devono essere enumerate. Se questa stringa è **NULL,** la funzione enumera le stampanti installate nel computer locale.

Se *Level* è 4, *Name* deve essere **NULL.** La funzione esegue sempre query sul computer locale.

Quando *Name* è **NULL,** l'impostazione *di* Flags su PRINTER ENUM LOCAL PRINTER ENUM CONNECTIONS enumera le stampanti \_ installate nel computer \_ \| \_ \_ locale. Queste stampanti includono quelle collegate fisicamente al computer locale e le stampanti remote a cui ha una connessione di rete.

Quando *Nome* non è  **NULL,** l'impostazione di Flag su PRINTER \_ ENUM \_ LOCAL PRINTER \| \_ ENUM \_ NAME enumera le stampanti locali installate nel server Nome .

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Tipo di strutture di dati a cui punta *pPrinterEnum*. I valori validi sono 1, 2, 4 e 5, che corrispondono alle strutture di dati [**PRINTER \_ INFO \_ 1,**](printer-info-1.md) [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4**](printer-info-4.md)e [**PRINTER INFO \_ \_ 5.**](printer-info-5.md)

Questo valore può essere 1, 2, 4 o 5.

</dd> <dt>

*pPrinterEnum* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve una matrice di strutture [**PRINTER \_ INFO \_ 1,**](printer-info-1.md) [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4**](printer-info-4.md)o [**PRINTER INFO \_ \_ 5.**](printer-info-5.md) Ogni struttura contiene dati che descrivono un oggetto di stampa disponibile.

Se *Level* è 1, la matrice contiene [**strutture PRINTER INFO \_ \_ 1.**](printer-info-1.md) Se *Level* è 2, la matrice contiene [**strutture PRINTER INFO \_ \_ 2.**](printer-info-2.md) Se *Level* è 4, la matrice contiene [**strutture PRINTER INFO \_ \_ 4.**](printer-info-4.md) Se *Level* è 5, la matrice contiene [**strutture PRINTER INFO \_ \_ 5.**](printer-info-5.md)

Il buffer deve essere sufficientemente grande da ricevere la matrice di strutture di dati e le stringhe o altri dati a cui puntano i membri della struttura. Se il buffer è troppo piccolo, il *parametro pcbNeeded* restituisce le dimensioni del buffer richieste.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer a cui punta *pPrinterEnum*.

</dd> <dt>

*pcbNeeded* \[ Cambio\]
</dt> <dd>

Puntatore a un valore che riceve il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.

</dd> <dt>

*pcReturned* \[ Cambio\]
</dt> <dd>

Puntatore a un valore che riceve il numero di strutture [**PRINTER \_ INFO \_ 1,**](printer-info-1.md) [**PRINTER INFO \_ \_ 2,**](printer-info-2.md) [**PRINTER INFO \_ \_ 4**](printer-info-4.md)o [**PRINTER INFO \_ \_ 5**](printer-info-5.md) restituite dalla funzione nella matrice a cui *punta pPrinterEnum.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Non chiamare questo metodo in [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Se **EnumPrinters** restituisce una struttura [**PRINTER INFO \_ \_ 1**](printer-info-1.md) in cui è specificato PRINTER ENUM CONTAINER, significa che è presente una gerarchia \_ di oggetti \_ stampante. Un'applicazione può enumerare la gerarchia chiamando **nuovamente EnumPrinters,** impostando *Name* sul valore del membro **pName** della struttura **PRINTER INFO \_ \_ 1.**

La **funzione EnumPrinters** non recupera le informazioni di sicurezza. Se [**le strutture PRINTER INFO \_ \_ 2**](printer-info-2.md) vengono restituite nella matrice a cui punta *pPrinterEnum*, i relativi *membri pSecurityDescriptor* verranno impostati su **NULL.**

Per ottenere informazioni sulla stampante predefinita, chiamare [**GetDefaultPrinter**](getdefaultprinter.md).

La [**struttura PRINTER INFO \_ \_ 4**](printer-info-4.md) offre un modo semplice ed estremamente rapido per recuperare i nomi delle stampanti installate in un computer locale, nonché le connessioni remote stabilite da un utente. Quando **EnumPrinters viene** chiamato con una struttura di dati **PRINTER INFO \_ \_ 4,** tale funzione esegue una query nel Registro di sistema per ottenere le informazioni specificate, quindi restituisce immediatamente . Questo comportamento differisce dal comportamento di **EnumPrinters** quando viene chiamato con altri livelli di strutture di dati **PRINTER INFO \_ \_ \* *_. In particolare,* quando _ EnumPrinters** viene chiamato con una struttura di dati di livello 2 ([**PRINTER INFO \_ \_ 2**](printer-info-2.md)), esegue una chiamata [**OpenPrinter**](openprinter.md) su ogni connessione remota. Se una connessione remota non è attiva o il server remoto non esiste più o la stampante remota non esiste più, la funzione deve attendere il timeout di RPC e di conseguenza non riesce la chiamata **openPrinter.** L'operazione può richiedere un po' di tempo. Il passaggio di una struttura **PRINTER \_ INFO \_ 4** consente a un'applicazione di recuperare un minimo di informazioni necessarie. Se si desidera ottenere informazioni più dettagliate, è possibile eseguire una chiamata di livello 2 di **EnumPrinters** successiva.

**Windows Vista:** I dati della stampante restituiti **da EnumPrinters** vengono recuperati da una cache locale quando il valore *di Level* è 4.

Nella tabella seguente viene illustrato **l'output EnumPrinters** per vari *valori Flags* quando il *parametro Level* è impostato su 1.

Nella colonna *Parametro* Nome della tabella è necessario sostituire un nome appropriato per Provider di stampa, Dominio e Computer. Ad esempio, per "Provider di stampa", è possibile usare il nome del provider di stampa di rete o il nome del provider di stampa locale. Per recuperare i nomi dei provider di stampa, chiamare **EnumPrinters** con *Name impostato* su **NULL.**



| *Parametro Flags*                                  | *Parametro Name*                            | Risultato                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| PRINTER \_ ENUM \_ LOCAL (e non PRINTER \_ ENUM \_ NAME) | Il *parametro Name* viene ignorato.<br/> | Tutte le stampanti locali.<br/>                                                                    |
| NOME \_ DELL'ENUMERAZIONE \_ PRINTER                                | "Provider di stampa"<br/>                 | Tutti i nomi di dominio<br/>                                                                       |
| PRINTER \_ ENUM \_ NAME                                | "Print Provider! Dominio"<br/>          | Tutte le stampanti e i server di stampa nel dominio del computer<br/>                                |
| PRINTER \_ ENUM \_ NAME                                | "Print Provider" \\ \\ Computer"<br/>    | Tutte le stampanti condivise nel \\ \\ computer<br/>                                                     |
| PRINTER \_ ENUM \_ NAME                                | Una stringa vuota, ""<br/>              | Tutte le stampanti locali.<br/>                                                                    |
| PRINTER \_ ENUM \_ NAME                                | **NULL**<br/>                         | Tutti i provider di stampa nel dominio del computer<br/>                                           |
| CONNESSIONI \_ DI ENUMERAZIONE \_ STAMPANTI                         | Il *parametro Name* viene ignorato.<br/> | Tutte le stampanti remote connesse<br/>                                                          |
| PRINTER \_ ENUM \_ NETWORK                             | Il *parametro Name* viene ignorato.<br/> | Tutte le stampanti nel dominio del computer<br/>                                                  |
| PRINTER \_ ENUM \_ REMOTE                              | Una stringa vuota, ""<br/>              | Tutte le stampanti e i server di stampa nel dominio del computer<br/>                                |
| PRINTER \_ ENUM \_ REMOTE                              | "Provider di stampa"<br/>                 | Uguale a PRINTER \_ ENUM \_ NAME<br/>                                                            |
| PRINTER \_ ENUM \_ REMOTE                              | "Print Provider! Dominio"<br/>          | Tutte le stampanti e i server di stampa nel dominio del computer, indipendentemente dal *dominio* specificato.<br/> |
| ENUMERAZIONE \_ \_ STAMPANTI CATEGORIA \_ 3D                        | Il *parametro Name* viene ignorato.<br/> | Vengono enumerate solo le stampanti 3D.<br/>                                                       |
| CATEGORIA \_ ENUMERAZIONE \_ STAMPANTI \_ ALL                       | Il *parametro Name* viene ignorato.<br/> | Le stampanti 3D vengono enumerate insieme a tutte le altre stampanti.<br/>                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumPrintersW** (Unicode) ed **EnumPrintersA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinter**](addprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 1**](printer-info-1.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 2**](printer-info-2.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 4**](printer-info-4.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 5**](printer-info-5.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> </dl>

 

