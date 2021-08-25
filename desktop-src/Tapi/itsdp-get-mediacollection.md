---
description: Il metodo get \_ MediaCollection ottiene un puntatore all'interfaccia ITMediaCollection per la conferenza.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: Metodo ITSdp::get_MediaCollection (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf358089a394775c753adc0642897021e91df5bfcd5f23418e638df82db03a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774511"
---
# <a name="itsdpget_mediacollection-method"></a>Metodo ITSdp::get \_ MediaCollection

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo get \_ MediaCollection** ottiene un puntatore [**all'interfaccia ITMediaCollection**](itmediacollection.md) per la conferenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppMediaCollection* \[ Cambio\]
</dt> <dd>

Puntatore a [**ITMediaCollection.**](itmediacollection.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                                                           | Significato                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                            | Il metodo è riuscito.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | Il *parametro ppMediaCollection* non è un puntatore valido.<br/>                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                   | Memoria insufficiente per eseguire l'operazione.<br/>                             |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                                          | Errore non specificato.<br/>                                                               |
| <dl> <dt>**HRESULT \_ DAL CODICE DI ERRORE \_ \_ (DATI NON VALIDI PER \_ \_ L'ERRORE)**</dt> </dl> | Si è verificato un errore interno, in genere a causa dell'errore di un metodo precedente.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                       | Questo metodo non è ancora implementato.<br/>                                              |



 

## <a name="remarks"></a>Commenti

È anche possibile ottenere un puntatore [**ITMediaCollection**](itmediacollection.md) usando **QueryInterface**.

TAPI chiama il **metodo AddRef** [**sull'interfaccia ITMediaCollection**](itmediacollection.md) restituita da **ITSdp::get \_ MediaCollection**. L'applicazione deve **chiamare Release** **sull'interfaccia ITMediaCollection** per liberare le risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




