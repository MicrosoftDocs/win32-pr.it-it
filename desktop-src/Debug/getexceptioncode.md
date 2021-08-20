---
description: Recupera un codice che identifica il tipo di eccezione che si verifica. La funzione può essere chiamata solo dall'interno dell'espressione di filtro o del blocco del gestore eccezioni di un gestore di eccezioni.
ms.assetid: f3c4a9f3-c9ae-4d20-85a7-787cb32278d1
title: Macro GetExceptionCode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5c1badd5317b5a12eb97ed6418873b5c576f520f4a8106361abb1a6f7c95921e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162662"
---
# <a name="getexceptioncode-macro"></a>Macro GetExceptionCode

Recupera un codice che identifica il tipo di eccezione che si verifica. La funzione può essere chiamata solo dall'interno dell'espressione di filtro o del blocco del gestore eccezioni di un gestore di eccezioni.

> [!Note]  
> Il compilatore di ottimizzazione di Microsoft C/C++ interpreta questa funzione come una parola chiave e il relativo uso al di fuori della sintassi di gestione delle eccezioni appropriata genera un errore del compilatore.

 

## <a name="syntax"></a>Sintassi


```C++
DWORD GetExceptionCode(void);
```



## <a name="parameters"></a>Parametri

Questa macro non ha parametri.

## <a name="return-value"></a>Valore restituito

Il valore restituito identifica il tipo di eccezione. La tabella seguente identifica i codici di eccezione che possono verificarsi a causa di errori di programmazione comuni. Questi valori sono definiti in WinBase.h e WinNT.h.



| Codice restituito                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VIOLAZIONE \_ DI ACCESSO ALLE \_ ECCEZIONI**</dt> </dl>         | Il thread tenta di leggere o scrivere in un indirizzo virtuale per il quale non ha accesso.<br/> Questo valore è definito come VIOLAZIONE \_ DI ACCESSO \_ DI STATO.<br/>                                                                                                                                                 |
| <dl> <dt>**LIMITI \_ DELLA MATRICE DI \_ \_ ECCEZIONI SUPERATI**</dt> </dl>   | Il thread tenta di accedere a un elemento della matrice non in limiti e l'hardware sottostante supporta il controllo dei limiti.<br/> Questo valore è definito come STATUS \_ ARRAY \_ BOUNDS \_ EXCEEDED.<br/>                                                                                                                 |
| <dl> <dt>**PUNTO DI INTERRUZIONE \_ ECCEZIONE**</dt> </dl>                | Viene rilevato un punto di interruzione.<br/> Questo valore è definito come STATUS \_ BREAKPOINT.<br/>                                                                                                                                                                                                                             |
| <dl> <dt>**EXCEPTION \_ DATATYPE \_ MISALIGNMENT**</dt> </dl>    | Il thread tenta di leggere o scrivere dati non allineati su hardware che non fornisce allineamento. Ad esempio, i valori a 16 bit devono essere allineati su limiti a 2 byte, valori a 32 bit su limiti a 4 byte e così via.<br/> Questo valore è definito come STATUS \_ DATATYPE \_ MISALIGNMENT.<br/>                    |
| <dl> <dt>**\_ \_ OPERANDO DENORMALE FLT \_ ECCEZIONE**</dt> </dl>    | Uno degli operandi in un'operazione a virgola mobile è denormale. Un valore denormale è troppo piccolo per essere rappresentato come valore a virgola mobile standard.<br/> Questo valore è definito come \_ OPERANDO DENORMALE DI STATUS \_ \_ FLOAT.<br/>                                                                                  |
| <dl> <dt>**EXCEPTION \_ FLT \_ DIVIDE \_ BY \_ ZERO**</dt> </dl>     | Il thread tenta di dividere un valore a virgola mobile per un divisore a virgola mobile pari a 0 (zero).<br/> Questo valore è definito come STATUS \_ FLOAT \_ DIVIDE BY \_ \_ ZERO.<br/>                                                                                                                                               |
| <dl> <dt>**RISULTATO \_ \_ DELL'ECCEZIONE FLT INEXACT \_**</dt> </dl>      | Il risultato di un'operazione a virgola mobile non può essere rappresentato esattamente come frazione decimale.<br/> Questo valore è definito come STATUS \_ FLOAT \_ INEXACT \_ RESULT.<br/>                                                                                                                                                |
| <dl> <dt>**EXCEPTION \_ FLT \_ INVALID \_ OPERATION**</dt> </dl>   | Eccezione a virgola mobile non inclusa nell'elenco.<br/> Questo valore è definito come STATUS \_ FLOAT \_ INVALID \_ OPERATION.<br/>                                                                                                                                                                             |
| <dl> <dt>**EXCEPTION \_ FLT \_ OVERFLOW**</dt> </dl>             | L'esponente di un'operazione a virgola mobile è maggiore della grandezza consentita dal tipo corrispondente.<br/> Questo valore è definito come STATUS \_ FLOAT \_ OVERFLOW.<br/>                                                                                                                                         |
| <dl> <dt>**CONTROLLO \_ STACK FLT \_ \_ ECCEZIONI**</dt> </dl>         | Overflow o underflow dello stack a causa di un'operazione a virgola mobile.<br/> Questo valore è definito come STATUS \_ FLOAT \_ STACK \_ CHECK.<br/>                                                                                                                                                                 |
| <dl> <dt>**UNDERFLOW \_ FLT \_ ECCEZIONE**</dt> </dl>            | L'esponente di un'operazione a virgola mobile è minore della grandezza consentita dal tipo corrispondente.<br/> Questo valore è definito come STATUS \_ FLOAT \_ UNDERFLOW.<br/>                                                                                                                                           |
| <dl> <dt>**PAGINA \_ EXCEPTION \_ GUARD**</dt> </dl>               | Il thread ha eseguito l'accesso alla memoria allocata con il modificatore PAGE \_ GUARD.<br/> Questo valore è definito come VIOLAZIONE DI PAGINA DI STATUS \_ \_ \_ GUARD.<br/>                                                                                                                                                                          |
| <dl> <dt>**ISTRUZIONE DI \_ ECCEZIONE NON \_ VALIDA**</dt> </dl>      | Il thread tenta di eseguire un'istruzione non valida.<br/> Questo valore è definito come ISTRUZIONE STATUS \_ \_ ILLEGAL.<br/>                                                                                                                                                                                            |
| <dl> <dt>**ECCEZIONE \_ \_ NELL'ERRORE \_ DI PAGINA**</dt> </dl>           | Il thread tenta di accedere a una pagina non presente e il sistema non è in grado di caricare la pagina. Ad esempio, questa eccezione può verificarsi se una connessione di rete viene persa durante l'esecuzione di un programma in rete.<br/> Questo valore è definito come STATUS \_ IN \_ PAGE \_ ERROR.<br/>                                   |
| <dl> <dt>**EXCEPTION \_ INT \_ DIVIDE \_ BY \_ ZERO**</dt> </dl>     | Il thread tenta di dividere un valore intero per un divisore intero pari a 0 (zero).<br/> Questo valore è definito come STATUS \_ INTEGER \_ DIVIDE BY \_ \_ ZERO.<br/>                                                                                                                                                         |
| <dl> <dt>**EXCEPTION \_ INT \_ OVERFLOW**</dt> </dl>             | Il risultato di un'operazione integer crea un valore troppo grande per essere mantenuto dal registro di destinazione. In alcuni casi, ciò comporta un'operazione di estrazione del bit più significativo del risultato. Alcune operazioni non impostano il flag carry.<br/> Questo valore è definito come STATUS \_ INTEGER \_ OVERFLOW.<br/> |
| <dl> <dt>**DISPOSIZIONE \_ ECCEZIONE \_ NON VALIDA**</dt> </dl>      | Un gestore di eccezioni restituisce una disposizione non valida al dispatcher di eccezioni. I programmatori che usano un linguaggio di alto livello, ad esempio C, non devono mai riscontrare questa eccezione.<br/> Questo valore è definito come STATUS \_ INVALID \_ DISPOSITION.<br/>                                                                      |
| <dl> <dt>**HANDLE DI \_ ECCEZIONE NON \_ VALIDO**</dt> </dl>           | Il thread ha usato un handle per un oggetto kernel non valido (probabilmente perché è stato chiuso).<br/> Questo valore è definito come HANDLE DI \_ STATO NON \_ VALIDO.<br/>                                                                                                                                                 |
| <dl> <dt>**EXCEPTION \_ NONCONTINUABLE \_ EXCEPTION**</dt> </dl> | Il thread tenta di continuare l'esecuzione dopo che si verifica un'eccezione non continuabile.<br/> Questo valore è definito come STATUS \_ NONCONTINUABLE \_ EXCEPTION.<br/>                                                                                                                                                       |
| <dl> <dt>**ISTRUZIONE \_ PRIV \_ EXCEPTION**</dt> </dl>         | Il thread tenta di eseguire un'istruzione con un'operazione non consentita nella modalità computer corrente.<br/> Questo valore è definito come ISTRUZIONE CON \_ PRIVILEGI \_ DI STATO.<br/>                                                                                                                           |
| <dl> <dt>**SINGOLO \_ PASSAGGIO \_ DELL'ECCEZIONE**</dt> </dl>              | Una trap di traccia o un altro meccanismo di istruzione singola segnala l'esecuzione di un'istruzione.<br/> Questo valore è definito come STATUS \_ SINGLE \_ STEP.<br/>                                                                                                                                                           |
| <dl> <dt>**OVERFLOW \_ DELLO STACK DI \_ ECCEZIONI**</dt> </dl>           | Il thread usa lo stack.<br/> Questo valore è definito come STATUS \_ STACK \_ OVERFLOW.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**CONSOLIDAMENTO \_ STATO RIMOZIONE \_**</dt> </dl>          | È stato eseguito un consolidamento dei frame.<br/>                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Commenti

La **funzione GetExceptionCode** può essere chiamata solo dall'interno dell'espressione di filtro o del blocco del gestore eccezioni di un gestore di eccezioni. L'espressione di filtro viene valutata se si verifica un'eccezione durante l'esecuzione del blocco **\_ \_ try** e determina se viene eseguito o meno il **\_ \_ blocco** except.

L'espressione di filtro può richiamare una funzione di filtro. La funzione di filtro non può **chiamare GetExceptionCode**. Tuttavia, il valore restituito di **GetExceptionCode** può essere passato come parametro a una funzione di filtro. Il valore restituito della [**funzione GetExceptionInformation**](getexceptioninformation.md) può anche essere passato come parametro a una funzione di filtro. **GetExceptionInformation restituisce** un puntatore a una struttura che include le informazioni sul codice dell'eccezione.

Se sono presenti gestori annidati, ogni espressione di filtro viene valutata fino a quando non ne viene valutata una come EXCEPTION \_ EXECUTE HANDLER o EXCEPTION CONTINUE \_ \_ \_ EXECUTION. Ogni espressione di filtro può richiamare **GetExceptionCode** per ottenere il codice dell'eccezione.

Il codice di eccezione restituito è il codice generato da un'eccezione hardware o il codice specificato nella [**funzione RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) per un'eccezione generata dal software.

Quando si gestisce l'eccezione del punto di interruzione, è importante incrementare il puntatore all'istruzione nel record di contesto per continuare da questa eccezione.

## <a name="examples"></a>Esempio

Per un esempio, vedere [Uso di un gestore eccezioni.](using-an-exception-handler.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetExceptionInformation**](getexceptioninformation.md)
</dt> <dt>

[**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)
</dt> <dt>

[Funzioni di gestione strutturata delle eccezioni](structured-exception-handling-functions.md)
</dt> <dt>

[Cenni preliminari sulla gestione strutturata delle eccezioni](structured-exception-handling.md)
</dt> </dl>

 

 
