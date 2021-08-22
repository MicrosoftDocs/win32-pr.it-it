---
description: Il metodo Create crea un nuovo supporto con proprietà predefinite, lo aggiunge alla raccolta in corrispondenza dell'indice specificato e restituisce un puntatore all'interfaccia ITMedia.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: Metodo ITMediaCollection::Create (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a2b11624b6a22a9bf1bff7b87538d3c7e915892a4ec7b816ee3d6c4d03821d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060869"
---
# <a name="itmediacollectioncreate-method"></a>Metodo ITMediaCollection::Create

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo Create** crea un nuovo supporto con proprietà predefinite, lo aggiunge alla raccolta in corrispondenza dell'indice specificato e restituisce un puntatore [**all'interfaccia ITMedia.**](itmedia.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Indice per il nuovo elemento. Il valore minimo per l'indice è 1 e il valore massimo per l'indice è il numero corrente di elementi + 1.

</dd> <dt>

*ppMedia* \[ Cambio\]
</dt> <dd>

Puntatore [**all'interfaccia ITMedia**](itmedia.md) creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Il *parametro ppMedia* non è un puntatore valido.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro Index* non è valido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

La maggior parte degli elenchi C e C++ è basata su 0, ma questo indice è basato su 1 per la compatibilità Visual Basic, ovvero il primo elemento ha un numero di indice 1.

TAPI chiama il **metodo AddRef** sull'interfaccia [**ITMedia**](itmedia.md) restituita da **ITMediaCollection::Create**. L'applicazione deve **chiamare Release** [**sull'interfaccia ITMedia**](itmedia.md) per liberare le risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




