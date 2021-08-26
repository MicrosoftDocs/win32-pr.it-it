---
description: Il metodo SetAlias configura un alias H.323 predefinito per l'indirizzo. Questo alias verrà usato nello scambio di configurazione delle chiamate H.323 in modo che l'altra parte conosca il nome di questa parte.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: Metodo IH323LineEx::SetAlias (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464c6707c3221fda1ef245e0302731ee7c6a1cf274c7ecac537c55f7f48437a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992191"
---
# <a name="ih323lineexsetalias-method"></a>Metodo IH323LineEx::SetAlias

\[**SetAlias** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo SetAlias** configura un alias H.323 predefinito per l'indirizzo. Questo alias verrà usato nello scambio di configurazione delle chiamate H.323 in modo che l'altra parte conosca il nome di questa parte.

Se si chiama questo metodo una seconda volta, l'alias precedente verrà sovrascritto.

L'alias impostato in questa interfaccia verrà usato solo quando il provider di servizi di configurazione non è in grado di trovare un alias appropriato. In futuro, quando il supporto di gatekeeper verrà aggiunto al TSP, l'alias registrato per il gatekeeper o assegnato dal gatekeeper eseguirà l'override di qualsiasi elemento impostato tramite questo metodo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strAlias* \[ Pollici\]
</dt> <dd>

Alias da utilizzare, in Unicode. **La** terminazione Null non è obbligatoria.

</dd> <dt>

*dwLength* \[ Pollici\]
</dt> <dd>

Lunghezza del nome dell'alias in numero di caratteri, incluso il **carattere di terminazione** Null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                               | Descrizione                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il metodo è riuscito.<br/>                                                                                                     |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Il numero di caratteri indicato in *dwLength* supera il numero effettivo di caratteri nel *parametro strAlias.*<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




