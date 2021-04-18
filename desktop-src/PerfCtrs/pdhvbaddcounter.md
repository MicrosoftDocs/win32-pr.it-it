---
description: La funzione PdhVbAddCounter crea una voce del contatore nell'oggetto query specificato e restituisce un handle al contatore al termine del completamento.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: PdhVbAddCounter (funzione)
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
ms.openlocfilehash: 19f97abeec74af0d08f340b70aa139e1bec7bf1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312154"
---
# <a name="pdhvbaddcounter-function"></a>PdhVbAddCounter (funzione)

La funzione **PdhVbAddCounter** crea una voce del contatore nell'oggetto query specificato e restituisce un handle al contatore al termine del completamento.

> [!IMPORTANT]
> La funzione descritta in questo argomento può essere modificata o non disponibile in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbAddCounter ( \_ ByVal QueryHandle Long, \_ ByVal CounterPath As String, \_ ByVal CounterHandle Long \_ ) Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*QueryHandle* 
</dt> <dd>

ID della query a cui deve essere assegnato questo contatore. Questo valore viene restituito dalla funzione [**PdhVbOpenQuery**](pdhvbopenquery.md) .

</dd> <dt>

*CounterPath* 
</dt> <dd>

Stringa di testo che specifica il nome del percorso del contatore da aggiungere alla query. Il contenuto di questa stringa deve essere un percorso di contatore valido, come ottenuto dal browser del contatore o da un'altra origine.

</dd> <dt>

*CounterHandle* 
</dt> <dd>

Riferimento univoco che identifica questo contatore nella query. Questa variabile deve essere inizializzata su zero prima della chiamata della funzione. Contiene un valore valido per return solo se la funzione viene completata correttamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce un **Long** Integer uguale a Error \_ Success e un nuovo handle nella variabile *CounterHandle* .

Se la funzione ha esito negativo, il valore restituito è un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md). Di seguito sono riportati i valori possibili.



| Codice restituito                                                                                                     | Descrizione                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_argomento PDH non valido \_**</dt> </dl>           | Uno o più argomenti non sono validi o sono errati.<br/>              |
| <dl> <dt>**\_errore di \_ allocazione della memoria PDH \_**</dt> </dl> | Impossibile allocare un buffer di memoria.<br/>                            |
| <dl> <dt>**\_handle PDH non valido \_**</dt> </dl>             | Handle di query non valido.<br/>                                     |
| <dl> <dt>**PDH \_ CSTATUS \_ senza \_ contatore**</dt> </dl>        | Il contatore specificato non è stato trovato.<br/>                               |
| <dl> <dt>**PDH \_ CSTATUS \_ nessun \_ oggetto**</dt> </dl>         | Impossibile trovare l'oggetto specificato.<br/>                           |
| <dl> <dt>**PDH \_ CSTATUS \_ nessun \_ computer**</dt> </dl>        | Non è stato possibile creare una voce del computer.<br/>                             |
| <dl> <dt>**PDH \_ CSTATUS \_ - \_ counterName non valido**</dt> </dl>   | È stata passata una stringa vuota del percorso del nome del contatore.<br/>                   |
| <dl> <dt>**\_funzione PDH \_ non \_ trovata**</dt> </dl>        | Impossibile determinare la funzione di calcolo per questo contatore.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbOpenQuery**](pdhvbopenquery.md)
</dt> </dl>

 

