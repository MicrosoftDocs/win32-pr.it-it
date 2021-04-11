---
description: Il metodo Disconnect disconnette l'oggetto NPP dalla rete.
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: 'IRTC: metodo:D di connessione (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: df58d6ac0e61ecc370510474c3bc067726d9824b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226966"
---
# <a name="irtcdisconnect-method"></a>IRTC::D metodo di connessione

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



| Codice restituito                                                                                          | Descrizione                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR**</dt> </dl>      | L'oggetto NPP sta acquisendo i dati. Non è possibile disconnettersi dalla rete mentre è in corso l'acquisizione dei dati.<br/> |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl> | L'oggetto NPP non è connesso alla rete.<br/>                                                                 |
| <dl> <dt>**NMERR \_ non in \_ tempo reale**</dt> </dl>  | L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .<br/>           |



 

## <a name="remarks"></a>Commenti

Questo metodo non può essere chiamato quando l'oggetto NPP sta acquisendo i dati. È necessario chiamare il metodo [IRTC:: Stop](irtc-stop.md) prima di chiamare IRTC::D Disconnect.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: Connect](irtc-connect.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> </dl>

 

 




