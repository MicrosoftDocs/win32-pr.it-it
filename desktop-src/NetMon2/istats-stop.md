---
description: Il metodo Stop arresta l'acquisizione corrente.
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'Metodo IStats:: Stop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7b7b58527e7bde0c3bbdec4fc162b705dd178c10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308168"
---
# <a name="istatsstop-method"></a>IStats:: Stop (metodo)

Il metodo **Stop** arresta l'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                            | Descrizione                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>   | L'oggetto NPP non è connesso alla rete. Chiamare il metodo [IStats:: Connect](istats-connect.md) per connettere l'oggetto NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ non \_ acquisizione**</dt> </dl>   | L'oggetto NPP non sta acquisendo dati. Chiamare il metodo [IStats:: Start](istats-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ \_ solo statistiche**</dt> </dl> | L'oggetto NPP è connesso alla rete, ma non con il metodo [IStats:: Connect](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Commenti

Quando si riavvia l'acquisizione dopo **IStats:: Stop** è stato chiamato, assicurarsi di chiamare il metodo [IStats:: Configure](istats-configure.md) ogni volta che si chiama [IStats:: Start](istats-start.md) per riavviare l'acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats:: Connect](istats-connect.md)
</dt> <dt>

[IStats:: Configure](istats-configure.md)
</dt> <dt>

[IStats:: Start](istats-start.md)
</dt> </dl>

 

 




