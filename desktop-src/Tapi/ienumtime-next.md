---
description: 'Metodo IEnumTime::Next: il metodo Next ottiene il successivo numero specificato di elementi nella sequenza di enumerazione.'
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: Metodo IEnumTime::Next (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6068d23fae96d5623ced72f44e6e8d185f861b6c49ff085f1b6e9e58bc489b89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905961"
---
# <a name="ienumtimenext-method"></a>Metodo IEnumTime::Next

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo Next** ottiene il successivo numero specificato di elementi nella sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ Pollici\]
</dt> <dd>

Numero di elementi richiesti.

</dd> <dt>

*pVal* \[ Cambio\]
</dt> <dd>

Puntatore [**all'interfaccia ITTime.**](ittime.md)

</dd> <dt>

*pceltFetched* \[ Cambio\]
</dt> <dd>

Puntatore al numero di elementi effettivamente forniti. Può essere **NULL se** *celt* è 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                     | Significato                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il metodo ha restituito il numero di elementi *celt.*<br/>         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Il numero di elementi rimanenti è minore di *celt*.<br/> |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Il *parametro pVal* non è un puntatore valido.<br/>       |



 

## <a name="remarks"></a>Commenti

TAPI chiama il **metodo AddRef** sull'interfaccia [**ITTime**](ittime.md) restituita da **IEnumTime::Next.** L'applicazione deve **chiamare Release** **sull'interfaccia ITTime** per liberare le risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




