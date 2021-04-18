---
description: Il metodo sealias configura un alias H. 323 predefinito per l'indirizzo. Questo alias verrà usato nello scambio di configurazione della chiamata H. 323, in modo che l'altra parte conosca il nome di questa entità.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: 'Metodo IH323LineEx:: sealias (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326149"
---
# <a name="ih323lineexsetalias-method"></a>Metodo IH323LineEx:: sealias

\[L' **alias** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **sealias** configura un alias H. 323 predefinito per l'indirizzo. Questo alias verrà usato nello scambio di configurazione della chiamata H. 323, in modo che l'altra parte conosca il nome di questa entità.

Se si chiama questo metodo una seconda volta, l'alias precedente verrà sovrascritto.

Il set di alias su questa interfaccia verrà utilizzato solo quando non esiste un altro modo per trovare un alias appropriato da parte del TSP. In futuro, quando viene aggiunto il supporto per gatekeeper nel TSP, l'alias registrato sul gatekeeper o assegnato dal Gatekeeper eseguirà l'override di qualsiasi valore impostato tramite questo metodo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strAlias* \[ in\]
</dt> <dd>

Alias da utilizzare in Unicode. Non è necessaria la terminazione **null** .

</dd> <dt>

*dwLength* \[ in\]
</dt> <dd>

Lunghezza del nome alias in numero di caratteri, incluso il terminatore **null** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                               | Descrizione                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Il metodo è riuscito.<br/>                                                                                                     |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Il numero di caratteri indicato in *dwLength* supera il numero effettivo di caratteri nel parametro *strAlias* .<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




