---
description: "Metodo IESP::Stop: il metodo Stop arresta l'acquisizione corrente."
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: Metodo IESP::Stop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d22333bcaad688fa9ebb805857db3673f48e70591e1d8953274598acef2b368b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037511"
---
# <a name="iespstop-method"></a>Metodo IESP::Stop

Il **metodo Stop** arresta l'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpStats* \[ Cambio\]
</dt> <dd>

Puntatore a una [struttura STATISTICS](statistics.md) che contiene statistiche di rete, ad esempio frame totali e byte totali acquisiti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                          | Descrizione                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl> | NPP non è connesso alla rete. Chiamare [IESP::Connessione](iesp-connect.md) per connettere NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl> | NPP non acquisisce dati. Chiamare [IESP::Start](iesp-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ NON \_ ESP**</dt> </dl>       | NPP è connesso alla rete, ma non con il metodo [IESP::Connessione.](iesp-connect.md)<br/>                     |



 

## <a name="remarks"></a>Commenti

Quando viene **chiamato il metodo IESP::Stop,** Network Monitor l'acquisizione dei dati e chiude il [*file di acquisizione.*](c.md) Il nome del file di acquisizione è stato restituito quando è stato chiamato [IESP::Start.](iesp-start.md) È ora possibile esaminare il contenuto del file di acquisizione.

Quando si arresta e si riavvia l'acquisizione, assicurarsi di chiamare il metodo [IESP::Configure](iesp-configure.md) ogni volta che si chiama [IESP::Start](iesp-start.md) per riavviare l'acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Connessione](iesp-connect.md)
</dt> <dt>

[IESP::Start](iesp-start.md)
</dt> <dt>

[Statistiche](statistics.md)
</dt> </dl>

 

 




