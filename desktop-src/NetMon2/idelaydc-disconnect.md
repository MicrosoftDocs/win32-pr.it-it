---
description: Il metodo Disconnect disconnette l'oggetto NPP dalla rete.
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: 'IDelaydC: metodo:D di connessione (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d192aa80f543706eea4bc197bc3dc8d57dd64aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128335"
---
# <a name="idelaydcdisconnect-method"></a>IDelaydC::D metodo di connessione

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



| Codice restituito                                                                                          | Descrizione                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR**</dt> </dl>      | L'oggetto NPP sta acquisendo i dati. Non è possibile disconnettere l'oggetto NPP dalla rete durante un'acquisizione.<br/>            |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl> | L'oggetto NPP non è connesso alla rete.<br/>                                                               |
| <dl> <dt>**NMERR \_ non \_ ritardato**</dt> </dl>   | L'oggetto NPP è connesso alla rete, ma non con il metodo [IDelaydC:: Connect](idelaydc-connect.md) .<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo non può essere chiamato quando l'oggetto NPP sta acquisendo i dati. Prima di chiamare **Disconnect**, è necessario chiamare il metodo **IDelaydC:: Stop** .

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

[IDelaydC:: Stop](idelaydc-stop.md)
</dt> </dl>

 

 




