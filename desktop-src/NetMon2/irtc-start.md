---
description: Il metodo Start avvia l'acquisizione.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'Metodo IRTC:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880709"
---
# <a name="irtcstart-method"></a>Metodo IRTC:: Start

Il metodo **Start** avvia l'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                           | Descrizione                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR \_ sospesa**</dt> </dl> | L'acquisizione si trova in uno stato di sospensione e deve essere arrestata prima di poter essere riavviata. Chiamare [IRTC:: Stop](idelaydc-stop.md) per arrestare l'acquisizione.<br/> |
| <dl> <dt>**\_acquisizione NMERR**</dt> </dl>       | Acquisizione già avviata.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>  | L'oggetto NPP non è connesso alla rete. Chiamare [IRTC:: Connect](irtc-connect.md) per connettere l'oggetto NPP alla rete.<br/>                         |
| <dl> <dt>**NMERR \_ non in \_ tempo reale**</dt> </dl>   | L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .<br/>                                             |



 

## <a name="remarks"></a>Commenti

Quando si riavvia l'acquisizione usando i metodi IRTC:: Start e [IRTC:: Stop](irtc-stop.md) , è necessario chiamare il metodo [IRTC:: Configure](irtc-configure.md) per riconfigurare la connessione ogni volta che si chiama IRTC:: Start per riavviare l'acquisizione dei dati.

> [!Note]  
> È anche possibile avviare e arrestare l'acquisizione usando i metodi [IRTC::P ause](irtc-pause.md) e [IRTC:: Resume](irtc-resume.md) .

 

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

[IRTC:: Configure](irtc-configure.md)
</dt> <dt>

[IRTC:: Connect](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC:: Resume](irtc-resume.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> </dl>

 

 




