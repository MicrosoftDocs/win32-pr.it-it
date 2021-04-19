---
description: Il metodo pause interrompe temporaneamente l'acquisizione corrente.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: IStats::P metodo ause (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319940"
---
# <a name="istatspause-method"></a>IStats::P metodo ause

Il metodo **pause** interrompe temporaneamente l'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                            | Descrizione                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR \_ sospesa**</dt> </dl>  | Acquisizione già sospesa.<br/>                                                                                                    |
| <dl> <dt>**NMERR \_ non \_ acquisizione**</dt> </dl>   | L'oggetto NPP non sta acquisendo dati. Chiamare il metodo [IStats:: Start](istats-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>   | L'oggetto NPP non è connesso alla rete. Chiamare il metodo [IStats:: Connect](istats-connect.md) per connettere l'oggetto NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ non \_ \_ solo statistiche**</dt> </dl> | L'oggetto NPP è connesso alla rete, ma non con il metodo [IStats:: Connect](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Commenti

Quando l'acquisizione viene sospesa, i nuovi frame non vengono acquisiti fino a quando una chiamata al metodo [IStats:: Resume](istats-resume.md) riavvia l'acquisizione.

Quando si usano i metodi **IStats::P ause** e **IStats:: Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) ogni volta che viene eseguita l'acquisizione.

Per riavviare la chiamata di acquisizione [IStats:: Resume](istats-resume.md). Per arrestare l'acquisizione, chiamare [IStats:: Stop](istats-stop.md).

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

[IStats:: Resume](istats-resume.md)
</dt> <dt>

[IStats:: Start](istats-start.md)
</dt> <dt>

[IStats:: Stop](istats-stop.md)
</dt> </dl>

 

 




