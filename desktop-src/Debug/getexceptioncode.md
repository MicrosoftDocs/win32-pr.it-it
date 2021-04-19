---
description: Recupera un codice che identifica il tipo di eccezione che si verifica. La funzione può essere chiamata solo dall'interno dell'espressione di filtro o del blocco del gestore di eccezioni di un gestore di eccezioni.
ms.assetid: f3c4a9f3-c9ae-4d20-85a7-787cb32278d1
title: GetExceptionCode (macro)
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
ms.openlocfilehash: 3b87b77ddb2d2e2af3a22e30d1204cf178ee6981
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305148"
---
# <a name="getexceptioncode-macro"></a>GetExceptionCode (macro)

Recupera un codice che identifica il tipo di eccezione che si verifica. La funzione può essere chiamata solo dall'interno dell'espressione di filtro o del blocco del gestore di eccezioni di un gestore di eccezioni.

> [!Note]  
> Il compilatore di ottimizzazione di Microsoft C/C++ interpreta questa funzione come una parola chiave e il suo utilizzo al di fuori della sintassi di gestione delle eccezioni appropriata genera un errore del compilatore.

 

## <a name="syntax"></a>Sintassi


```C++
DWORD GetExceptionCode(void);
```



## <a name="parameters"></a>Parametri

Questa macro non contiene parametri.

## <a name="return-value"></a>Valore restituito

Il valore restituito identifica il tipo di eccezione. La tabella seguente identifica i codici di eccezione che possono verificarsi a causa di errori di programmazione comuni. Questi valori sono definiti in WinBase. h e WinNT. h.



| Codice restituito                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_violazione di accesso alle eccezioni \_**</dt> </dl>         | Il thread tenta di leggere o scrivere in un indirizzo virtuale per cui non ha accesso.<br/> Questo valore è definito come violazione di accesso allo stato \_ \_ .<br/>                                                                                                                                                 |
| <dl> <dt>**\_ \_ superati i limiti della matrice di eccezioni \_**</dt> </dl>   | Il thread tenta di accedere a un elemento di matrice fuori limite e l'hardware sottostante supporta il controllo dei limiti.<br/> Questo valore è definito come limiti della matrice di stato \_ \_ \_ superati.<br/>                                                                                                                 |
| <dl> <dt>**punto di \_ interruzione eccezione**</dt> </dl>                | Viene rilevato un punto di interruzione.<br/> Questo valore è definito come punto di interruzione dello stato \_ .<br/>                                                                                                                                                                                                                             |
| <dl> <dt>**disallineamento del tipo di dati eccezione \_ \_**</dt> </dl>    | Il thread tenta di leggere o scrivere dati non allineati all'hardware che non fornisce l'allineamento. Ad esempio, i valori a 16 bit devono essere allineati su limiti di 2 byte, valori a 32 bit su limiti di 4 byte e così via.<br/> Questo valore è definito come disallineamento del tipo di dati di stato \_ \_ .<br/>                    |
| <dl> <dt>**\_operando di eccezione flt \_ denormal \_**</dt> </dl>    | Uno degli operandi in un'operazione a virgola mobile è denormalizzato. Un valore denormalizzato è troppo piccolo per essere rappresentato come valore a virgola mobile standard.<br/> Questo valore è definito come \_ \_ operando denormalizzato di stato float \_ .<br/>                                                                                  |
| <dl> <dt>**ECCEZIONE \_ flt \_ divisione \_ per \_ zero**</dt> </dl>     | Il thread tenta di dividere un valore a virgola mobile per un divisore a virgola mobile pari a 0 (zero).<br/> Questo valore è definito come \_ float \_ di stato divisione \_ per \_ zero.<br/>                                                                                                                                               |
| <dl> <dt>**risultato di eccezione \_ flt \_ inesatto \_**</dt> </dl>      | Il risultato di un'operazione a virgola mobile non può essere rappresentato esattamente come una frazione decimale.<br/> Questo valore è definito come \_ \_ risultato inesatto float di stato \_ .<br/>                                                                                                                                                |
| <dl> <dt>**\_operazione FLT di eccezione \_ non valida \_**</dt> </dl>   | Eccezione a virgola mobile non inclusa nell'elenco.<br/> Questo valore è definito come operazione di stato \_ float \_ non valido \_ .<br/>                                                                                                                                                                             |
| <dl> <dt>**\_overflow flt \_ eccezione**</dt> </dl>             | L'esponente di un'operazione a virgola mobile è maggiore della grandezza consentita dal tipo corrispondente.<br/> Questo valore è definito come overflow di stato \_ float \_ .<br/>                                                                                                                                         |
| <dl> <dt>**\_ \_ controllo dello stack flt eccezione \_**</dt> </dl>         | Si è verificato un overflow o un overflow dello stack a causa di un'operazione a virgola mobile.<br/> Questo valore è definito come \_ \_ controllo dello stack float di stato \_ .<br/>                                                                                                                                                                 |
| <dl> <dt>**UNDERFLOW di eccezione \_ flt \_**</dt> </dl>            | L'esponente di un'operazione a virgola mobile è minore della grandezza consentita dal tipo corrispondente.<br/> Questo valore è definito come underflow di stato \_ float \_ .<br/>                                                                                                                                           |
| <dl> <dt>**\_pagina di protezione delle eccezioni \_**</dt> </dl>               | Il thread ha eseguito l'accesso alla memoria allocata con il \_ modificatore di Page Guard.<br/> Questo valore è definito come violazione della pagina di Guard di stato \_ \_ \_ .<br/>                                                                                                                                                                          |
| <dl> <dt>**\_istruzione non valida eccezione \_**</dt> </dl>      | Il thread tenta di eseguire un'istruzione non valida.<br/> Questo valore è definito come istruzione di stato non \_ valida \_ .<br/>                                                                                                                                                                                            |
| <dl> <dt>**ECCEZIONE \_ nell' \_ errore di pagina \_**</dt> </dl>           | Il thread tenta di accedere a una pagina che non è presente e il sistema non è in grado di caricare la pagina. Ad esempio, questa eccezione può verificarsi se una connessione di rete viene persa durante l'esecuzione di un programma in una rete.<br/> Questo valore è definito come stato \_ nell' \_ errore di pagina \_ .<br/>                                   |
| <dl> <dt>**ECCEZIONE \_ int \_ Divide \_ per \_ zero**</dt> </dl>     | Il thread tenta di dividere un valore integer per un divisore integer pari a 0 (zero).<br/> Questo valore è definito come intero dello stato \_ \_ diviso \_ per \_ zero.<br/>                                                                                                                                                         |
| <dl> <dt>**\_overflow int \_ eccezione**</dt> </dl>             | Il risultato di un'operazione Integer crea un valore troppo grande per essere utilizzato dal registro di destinazione. In alcuni casi, questa operazione comporterà l'esecuzione del bit del risultato più significativo. Alcune operazioni non impostano il flag Carry.<br/> Questo valore è definito come overflow di Integer dello stato \_ \_ .<br/> |
| <dl> <dt>**\_disposizione non valida eccezione \_**</dt> </dl>      | Un gestore di eccezioni restituisce una disposizione non valida al dispatcher di eccezioni. I programmatori che usano un linguaggio di alto livello, ad esempio C, non dovrebbero mai riscontrare questa eccezione.<br/> Questo valore è definito come stato \_ non valido \_ .<br/>                                                                      |
| <dl> <dt>**\_handle non valido eccezione \_**</dt> </dl>           | Il thread usava un handle per un oggetto kernel non valido, probabilmente perché era stato chiuso.<br/> Questo valore è definito come handle di stato \_ non valido \_ .<br/>                                                                                                                                                 |
| <dl> <dt>**eccezione non \_ continuabile \_ eccezione**</dt> </dl> | Il thread tenta di continuare l'esecuzione dopo che si è verificata un'eccezione non continua.<br/> Questo valore è definito come eccezione di stato non \_ continuabile \_ .<br/>                                                                                                                                                       |
| <dl> <dt>**\_istruzione priv dell'eccezione \_**</dt> </dl>         | Il thread tenta di eseguire un'istruzione con un'operazione non consentita nella modalità computer corrente.<br/> Questo valore è definito come istruzione con privilegi di stato \_ \_ .<br/>                                                                                                                           |
| <dl> <dt>**\_singolo \_ passaggio eccezione**</dt> </dl>              | Un trap di traccia o un altro meccanismo di istruzione singola segnala l'esecuzione di un'istruzione.<br/> Questo valore è definito come \_ singolo passaggio di stato \_ .<br/>                                                                                                                                                           |
| <dl> <dt>**\_overflow dello stack di eccezioni \_**</dt> </dl>           | Il thread usa il relativo stack.<br/> Questo valore è definito come \_ overflow dello stack di stato \_ .<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**consolidamento dello stato di \_ rimozione \_**</dt> </dl>          | È stato eseguito un consolidamento dei frame.<br/>                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Commenti

La funzione **GetExceptionCode** può essere chiamata solo dall'interno dell'espressione di filtro o del blocco del gestore di eccezioni di un gestore di eccezioni. L'espressione di filtro viene valutata se si verifica un'eccezione durante l'esecuzione del blocco **\_ \_ try** e determina se il blocco **\_ \_ except** viene eseguito o meno.

L'espressione di filtro può richiamare una funzione di filtro. La funzione Filter non può chiamare **GetExceptionCode**. Tuttavia, il valore restituito di **GetExceptionCode** può essere passato come parametro a una funzione di filtro. Il valore restituito della funzione [**GetExceptionInformation**](getexceptioninformation.md) può essere passato anche come parametro a una funzione di filtro. **GetExceptionInformation** restituisce un puntatore a una struttura che include le informazioni sul codice di eccezione.

Quando sono presenti gestori nidificati, ogni espressione di filtro viene valutata fino a quando non viene valutata come gestore di esecuzione delle eccezioni \_ \_ oppure \_ l'esecuzione dell'eccezione continua \_ . Ogni espressione di filtro può richiamare **GetExceptionCode** per ottenere il codice di eccezione.

Il codice di eccezione restituito è il codice generato da un'eccezione hardware oppure il codice specificato nella funzione [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) per un'eccezione generata dal software.

Quando si gestisce l'eccezione del punto di interruzione, è importante incrementare il puntatore all'istruzione nel record di contesto per continuare da questa eccezione.

## <a name="examples"></a>Esempio

Per un esempio, vedere [uso di un gestore di eccezioni](using-an-exception-handler.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetExceptionInformation**](getexceptioninformation.md)
</dt> <dt>

[**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)
</dt> <dt>

[Funzioni di gestione delle eccezioni strutturate](structured-exception-handling-functions.md)
</dt> <dt>

[Cenni preliminari sulla gestione delle eccezioni strutturata](structured-exception-handling.md)
</dt> </dl>

 

 
