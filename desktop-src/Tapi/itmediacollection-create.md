---
description: Il metodo Create crea un nuovo supporto con proprietà predefinite, lo aggiunge alla raccolta in corrispondenza dell'indice specificato e restituisce un puntatore all'interfaccia ITMedia.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'Metodo ITMediaCollection:: Create (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332920"
---
# <a name="itmediacollectioncreate-method"></a>Metodo ITMediaCollection:: create

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **create** crea un nuovo supporto con proprietà predefinite, lo aggiunge alla raccolta in corrispondenza dell'indice specificato e restituisce un puntatore all'interfaccia [**ITmedia**](itmedia.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

Indice per il nuovo elemento. Il valore minimo per l'indice è 1 e il valore massimo per l'indice è il numero corrente di elementi + 1.

</dd> <dt>

*ppMedia* \[ out\]
</dt> <dd>

Puntatore all'interfaccia [**ITmedia**](itmedia.md) creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppMedia* non è un puntatore valido.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro di *Indice* non è valido.<br/>                  |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

La maggior parte degli elenchi C e C++ sono basati su 0, ma questo indice è basato su 1 per la compatibilità con Visual Basic, ovvero il primo elemento ha un numero di indice pari a 1.

TAPI chiama il metodo **AddRef** sull'interfaccia [**ITmedia**](itmedia.md) restituita da **ITMediaCollection:: create**. L'applicazione deve chiamare **Release** sull'interfaccia [**ITmedia**](itmedia.md) per liberare risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




