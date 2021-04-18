---
description: Disconnette l'oggetto NPP dalla rete.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: IStats::D metodo di connessione (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a5fa56c05036380b5dba42089979b43d776a4b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315461"
---
# <a name="istatsdisconnect-method"></a>IStats::D metodo di connessione

Il metodo **Disconnect** disconnette l'oggetto NPP dalla rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                            | Descrizione                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR**</dt> </dl>        | Il NPP sta attualmente acquisendo i dati. Non è possibile disconnettersi dalla rete mentre è in corso un'acquisizione dei dati.<br/> |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>   | L'oggetto NPP non è connesso alla rete.<br/>                                                                         |
| <dl> <dt>**NMERR \_ non \_ \_ solo statistiche**</dt> </dl> | L'oggetto NPP è connesso alla rete, ma non con il metodo [**IStats:: Connect**](istats-connect.md) .<br/>          |



 

## <a name="remarks"></a>Commenti

Questo metodo non può essere chiamato quando l'oggetto NPP sta acquisendo i dati. Chiamare il metodo **IStats::D** prima la connessione e quindi chiamare [**IStats:: Stop**](istats-stop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats:: Connect**](istats-connect.md)
</dt> <dt>

[**IStats:: Stop**](istats-stop.md)
</dt> </dl>

 

 




