---
description: La funzione PdhVbOpenQuery crea e Inizializza una struttura di query univoca usata per gestire la raccolta di dati sulle prestazioni.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: PdhVbOpenQuery (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131678"
---
# <a name="pdhvbopenquery-function"></a>PdhVbOpenQuery (funzione)

La funzione **PdhVbOpenQuery** crea e Inizializza una struttura di query univoca usata per gestire la raccolta di dati sulle prestazioni.

> [!IMPORTANT]
> La funzione descritta in questo argomento può essere modificata o non disponibile in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbOpenQuery ( \_ ByVal QueryHandle Long \_ ) Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*QueryHandle* 
</dt> <dd>

Variabile cancellata (uguale a 0) prima della chiamata della funzione e, se la funzione ha esito positivo, contiene l'ID univoco della query creata e aperta. Questo handle viene usato nelle chiamate successive ad altre funzioni PDH per identificare la query.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce un **Long** Integer uguale a Error \_ Success e un nuovo handle nella variabile *QueryHandle* .

Se la funzione ha esito negativo, il valore restituito è un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md). Di seguito sono riportati i valori possibili.



| Codice restituito                                                                                                     | Descrizione                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**\_argomento PDH non valido \_**</dt> </dl>           | L'argomento non è valido o non è corretto.<br/>             |
| <dl> <dt>**\_errore di \_ allocazione della memoria PDH \_**</dt> </dl> | Impossibile allocare un buffer di memoria temporaneo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

