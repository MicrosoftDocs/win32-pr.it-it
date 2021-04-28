---
description: "Metodo IDelaydC::Stop: il metodo Stop arresta l'acquisizione corrente."
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: Metodo IDelaydC::Stop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 38be5b6ba4c3f6edcd716f4d0235150e96dd692a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110779"
---
# <a name="idelaydcstop-method"></a>Metodo IDelaydC::Stop

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

Puntatore a una [struttura STATISTICS](statistics.md) che contiene statistiche di rete, ad esempio i frame totali e i byte totali acquisiti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                          | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl> | Il NPP non è connesso alla rete. Chiamare [IDelaydC::Connect](idelaydc-connect.md) per connettere il NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl> | Il NPP non acquisisce dati. Chiamare [IDelaydC::Start](idelaydc-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ NON \_ RITARDATO**</dt> </dl>   | Il NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connect.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Commenti

Quando **viene chiamato IDelaydC::Stop,** Network Monitor l'acquisizione dei dati e chiude il [*file di acquisizione*](c.md). Il nome del file di acquisizione è stato restituito quando è stato chiamato [IDelaydC::Start.](idelaydc-start.md) È ora possibile esaminare il contenuto del file di acquisizione.

Quando si arresta e si avvia l'acquisizione, assicurarsi di chiamare il metodo [IDelaydC::Configure](idelaydc-configure.md) ogni volta che si chiama [IDelaydC::Start](idelaydc-start.md) per riavviare l'acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[Statistiche](statistics.md)
</dt> </dl>

 

 




