---
description: La funzione PdhVbOpenQuery crea e inizializza una struttura di query univoca usata per gestire la raccolta di dati sulle prestazioni.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: Funzione PdhVbOpenQuery
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
ms.openlocfilehash: 70d207696f68b9ef86ba0bae1f596826bd6e400d05d011b330f67241e186f5eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962391"
---
# <a name="pdhvbopenquery-function"></a>Funzione PdhVbOpenQuery

La **funzione PdhVbOpenQuery** crea e inizializza una struttura di query univoca usata per gestire la raccolta di dati sulle prestazioni.

> [!IMPORTANT]
> La funzione descritta in questo argomento potrebbe essere modificata o non disponibile in futuro. È invece consigliabile usare le funzioni descritte in [Funzioni dei contatori delle prestazioni.](performance-counters-functions.md)

Funzione PdhVbOpenQuery( \_ ByVal QueryHandle As Long \_ ) As Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*QueryHandle* 
</dt> <dd>

Variabile cancellata (uguale a 0) prima che venga chiamata la funzione e, se la funzione ha esito positivo, contiene l'ID univoco della query creata e aperta. Questo handle viene usato nelle chiamate successive ad altre funzioni PDH per identificare la query.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce un **long** integer uguale a ERROR SUCCESS e \_ un nuovo handle nella variabile *QueryHandle.*

Se la funzione ha esito negativo, il valore restituito è un codice [di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di errore [PDH](pdh-error-codes.md). Di seguito sono riportati i valori possibili.



| Codice restituito                                                                                                     | Descrizione                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**ARGOMENTO PDH \_ NON \_ VALIDO**</dt> </dl>           | L'argomento non è valido o non è corretto.<br/>             |
| <dl> <dt>**ERRORE DI ALLOCAZIONE \_ DELLA MEMORIA PDH \_ \_**</dt> </dl> | Impossibile allocare un buffer di memoria temporaneo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

