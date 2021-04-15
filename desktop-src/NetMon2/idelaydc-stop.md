---
description: Il metodo Stop arresta l'acquisizione corrente.
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'Metodo IDelaydC:: Stop (Netmon. h)'
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
ms.openlocfilehash: 42c9cc1c4b6da7b5f934dd96f26aa9348c43ac0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484308"
---
# <a name="idelaydcstop-method"></a>Metodo IDelaydC:: Stop

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



| Codice restituito                                                                                          | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl> | L'oggetto NPP non è connesso alla rete. Chiamare [IDelaydC:: Connect](idelaydc-connect.md) per connettere l'oggetto NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ non \_ acquisizione**</dt> </dl> | L'oggetto NPP non sta acquisendo dati. Chiamare [IDelaydC:: Start](idelaydc-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ ritardato**</dt> </dl>   | L'oggetto NPP è connesso alla rete, ma non con il metodo [IDelaydC:: Connect](idelaydc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Commenti

Quando viene chiamato **IDelaydC:: Stop** , Network Monitor interrompe l'acquisizione dei dati e chiude il [*file di acquisizione*](c.md). (Il nome del file di acquisizione è stato restituito quando è stato chiamato [IDelaydC:: Start](idelaydc-start.md) ). È ora possibile esaminare il contenuto del file di acquisizione.

Quando si arresta e si avvia l'acquisizione, assicurarsi di chiamare il metodo [IDelaydC:: Configure](idelaydc-configure.md) ogni volta che si chiama [IDelaydC:: Start](idelaydc-start.md) per riavviare l'acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC:: Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC:: Configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC:: Start](idelaydc-start.md)
</dt> <dt>

[Statistiche](statistics.md)
</dt> </dl>

 

 




