---
description: Configura la preferenza delle funzionalità predefinite.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: Metodo IH323LineEx::SetDefaultCapabilityPreferrence (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64eb3385edb758529f27f9fb90eb0cce998eca60f202c72a28ba48a5318c6b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992081"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a>Metodo IH323LineEx::SetDefaultCapabilityPreferrence

\[**SetDefaultCapabilityPreferrence** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo SetDefaultCapabilityPreferrence** configura la preferenza delle funzionalità predefinite. Le funzionalità hanno un peso predefinito di 100. Se l'applicazione specifica un peso maggiore per una funzionalità, avrà una priorità più alta durante la negoziazione H.245. Se l'applicazione imposta il peso di una funzionalità su 0, non verrà usata nella negoziazione H.245.

Questo metodo è cumulativo. Ad esempio, se questo metodo viene chiamato per primo per disabilitare una funzionalità e viene chiamato di nuovo per disabilitare un'altra funzionalità, entrambe le funzionalità verranno disabilitate come risultato di queste due chiamate.

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

*dwNumCaps* \[ Pollici\]
</dt> <dd>

Valore **DWORD** che contiene il numero di funzionalità impostate con questo metodo.

</dd> <dt>

*pCapabilities* \[ Pollici\]
</dt> <dd>

Matrice di funzionalità. Ogni elemento della matrice è un [**valore \_ CAPABILITY H245.**](h245-capability.md)

</dd> <dt>

*pWeights* \[ Pollici\]
</dt> <dd>

Matrice di pesi associati alle funzionalità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                                                                                                                                                                                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pCapabilities* è **NULL** o il *parametro pWeights* è **NULL** oppure *pCapabilities* e *pWeights* sono **NULL** oppure la matrice pCapabilities contiene un oggetto funzionalità H.245 non valido.<br/> |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Impossibile leggere un elemento della matrice *pWeights* o un elemento della *matrice pCapabilities.*<br/>                                                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




