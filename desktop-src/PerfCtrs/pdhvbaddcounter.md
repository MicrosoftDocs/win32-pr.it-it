---
description: La funzione PdhVbAddCounter crea una voce del contatore nell'oggetto query specificato e restituisce un handle per tale contatore al completamento corretto.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: Funzione PdhVbAddCounter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 6605e2fb02edad23831b22334b960eaa2e89f23206673608500f248452094ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061149"
---
# <a name="pdhvbaddcounter-function"></a>Funzione PdhVbAddCounter

La **funzione PdhVbAddCounter** crea una voce del contatore nell'oggetto query specificato e restituisce un handle per tale contatore al completamento corretto.

> [!IMPORTANT]
> La funzione descritta in questo argomento potrebbe essere modificata o non disponibile in futuro. Microsoft consiglia invece di usare le funzioni descritte in [Funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbAddCounter( \_ ByVal QueryHandle As Long, \_ ByVal CounterPath as String, \_ ByVal CounterHandle As Long \_ ) As Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*QueryHandle* 
</dt> <dd>

ID della query a cui deve essere assegnato questo contatore. Questo valore viene restituito dalla [**funzione PdhVbOpenQuery.**](pdhvbopenquery.md)

</dd> <dt>

*CounterPath* 
</dt> <dd>

Stringa di testo che specifica il nome del percorso del contatore da aggiungere alla query. Il contenuto di questa stringa deve essere un percorso contatore valido, ottenuto dal visualizzatore contatori o da un'altra origine.

</dd> <dt>

*CounterHandle* 
</dt> <dd>

Riferimento univoco che identifica questo contatore nella query. Questa variabile deve essere inizializzata su zero prima che venga chiamata la funzione . Contiene un valore valido in caso di restituzione solo se la funzione viene completata correttamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce un **valore Long** integer uguale a ERROR SUCCESS e un nuovo handle nella \_ variabile *CounterHandle.*

Se la funzione ha esito negativo, il valore restituito è un codice di errore [di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md). Di seguito sono riportati i valori possibili.



| Codice restituito                                                                                                     | Descrizione                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**ARGOMENTO PDH \_ NON \_ VALIDO**</dt> </dl>           | Uno o più argomenti non sono validi o non sono corretti.<br/>              |
| <dl> <dt>**ERRORE DI ALLOCAZIONE \_ DELLA MEMORIA PDH \_ \_**</dt> </dl> | Impossibile allocare un buffer di memoria.<br/>                            |
| <dl> <dt>**HANDLE PDH \_ NON \_ VALIDO**</dt> </dl>             | L'handle di query non è valido.<br/>                                     |
| <dl> <dt>**PDH \_ CSTATUS \_ NO \_ COUNTER**</dt> </dl>        | Il contatore specificato non è stato trovato.<br/>                               |
| <dl> <dt>**PDH \_ CSTATUS \_ NO \_ OBJECT**</dt> </dl>         | Impossibile trovare l'oggetto specificato.<br/>                           |
| <dl> <dt>**PDH \_ CSTATUS \_ NO \_ MACHINE**</dt> </dl>        | Impossibile creare una voce del computer.<br/>                             |
| <dl> <dt>**PDH \_ CSTATUS \_ NOME \_ CONTATORE NON VALIDO**</dt> </dl>   | È stata passata una stringa di percorso del nome del contatore vuota.<br/>                   |
| <dl> <dt>**FUNZIONE PDH \_ \_ NON \_ TROVATA**</dt> </dl>        | Impossibile determinare la funzione di calcolo per questo contatore.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbOpenQuery**](pdhvbopenquery.md)
</dt> </dl>

 

