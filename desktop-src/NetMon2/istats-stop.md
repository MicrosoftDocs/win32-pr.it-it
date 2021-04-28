---
description: "Metodo IStats::Stop: il metodo Stop arresta l'acquisizione corrente."
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: Metodo IStats::Stop (Netmon.h)
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
ms.openlocfilehash: ef51aff870a3193963b3802332112c51f1024826
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114609"
---
# <a name="istatsstop-method"></a>Metodo IStats::Stop

Il **metodo Stop** arresta l'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                            | Descrizione                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>   | NPP non è connesso alla rete. Chiamare il [metodo IStats::Connect](istats-connect.md) per connettere NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl>   | NPP non acquisisce dati. Chiamare il [metodo IStats::Start](istats-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ NON \_ STATS \_ ONLY**</dt> </dl> | NPP è connesso alla rete, ma non con il [metodo IStats::Connect.](istats-connect.md)<br/>                                |



 

## <a name="remarks"></a>Commenti

Quando si riavvia l'acquisizione dopo la chiamata di **IStats::Stop,** assicurarsi di chiamare il metodo [IStats::Configure](istats-configure.md) ogni volta che si chiama [IStats::Start](istats-start.md) per riavviare l'acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStat](istats.md)
</dt> <dt>

[IStats::Connect](istats-connect.md)
</dt> <dt>

[IStats::Configure](istats-configure.md)
</dt> <dt>

[IStats::Start](istats-start.md)
</dt> </dl>

 

 




