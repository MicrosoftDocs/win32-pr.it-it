---
description: Configura la preferenza delle funzionalità predefinite.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'Metodo IH323LineEx:: SetDefaultCapabilityPreferrence (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326148"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a>Metodo IH323LineEx:: SetDefaultCapabilityPreferrence

\[**SetDefaultCapabilityPreferrence** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **SetDefaultCapabilityPreferrence** configura la preferenza delle funzionalità predefinite. Le funzionalità hanno un peso predefinito di 100. Se l'applicazione specifica un peso maggiore per una funzionalità, avrà una priorità maggiore durante la negoziazione H. 245. Se l'applicazione imposta il peso di una funzionalità su 0, non verrà utilizzata nella negoziazione H. 245.

Questo metodo è cumulativo. Se, ad esempio, questo metodo viene chiamato per primo per disabilitare una funzionalità e viene chiamato di nuovo per disabilitarne un altro, entrambe le funzionalità verranno disabilitate come risultato di queste due chiamate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwNumCaps* \[ in\]
</dt> <dd>

Valore **DWORD** che contiene il numero di funzionalità impostate con questo metodo.

</dd> <dt>

*pCapabilities* \[ in\]
</dt> <dd>

Matrice di funzionalità. Ogni elemento della matrice è un valore [**della \_ funzionalità h245**](h245-capability.md) .

</dd> <dt>

*pWeights* \[ in\]
</dt> <dd>

Matrice di pesi associati alle funzionalità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                                                                                                                                                                                |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *pCapabilities* è **null** o il parametro *PWeights* è **null** oppure sia *pCapabilities* che *PWeights* sono **null** oppure la matrice pCapabilities contiene un oggetto funzionalità H. 245 non valido.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Impossibile leggere un elemento della matrice *pWeights* o un elemento della matrice *pCapabilities* .<br/>                                                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




