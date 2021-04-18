---
description: Il metodo Stop arresta l'acquisizione corrente.
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'Metodo IESP:: Stop (Netmon. h)'
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
ms.openlocfilehash: 50dfb274e1355af93c473609f95607e6b3faf1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305872"
---
# <a name="iespstop-method"></a>Metodo IESP:: Stop

Il metodo **Stop** arresta l'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpStats* \[ out\]
</dt> <dd>

Puntatore a una struttura di [statistiche](statistics.md) che contiene le statistiche di rete, ad esempio i frame totali e i byte totali acquisiti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                          | Descrizione                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl> | L'oggetto NPP non è connesso alla rete. Chiamare [IESP:: Connect](iesp-connect.md) per connettere l'oggetto NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ non \_ acquisizione**</dt> </dl> | L'oggetto NPP non sta acquisendo dati. Chiamare [IESP:: Start](iesp-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ ESP**</dt> </dl>       | L'oggetto NPP è connesso alla rete, ma non con il metodo [IESP:: Connect](iesp-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Commenti

Quando viene chiamato il metodo **IESP:: Stop** , Network Monitor interrompe l'acquisizione dei dati e chiude il [*file di acquisizione.*](c.md) (Il nome del file di acquisizione è stato restituito quando è stato chiamato [IESP:: Start](iesp-start.md) ). È ora possibile esaminare il contenuto del file di acquisizione.

Quando si arresta e si riavvia l'acquisizione, assicurarsi di chiamare il metodo [IESP:: Configure](iesp-configure.md) ogni volta che si chiama [IESP:: Start](iesp-start.md) per riavviare l'acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP:: Connect](iesp-connect.md)
</dt> <dt>

[IESP:: Start](iesp-start.md)
</dt> <dt>

[Statistiche](statistics.md)
</dt> </dl>

 

 




