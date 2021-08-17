---
description: "Metodo IRTC::Stop: il metodo Stop arresta l'acquisizione corrente."
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: Metodo IRTC::Stop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 285d26e4eb141904e8a1951e6e42d0df0ef5d9738e5849057bbfe1e0a978e0b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743001"
---
# <a name="irtcstop-method"></a>Metodo IRTC::Stop

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



| Codice restituito                                                                                          | Descrizione                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl> | Il NPP non è connesso alla rete. Chiamare [IRTC::Connessione](irtc-connect.md) per connettere il protocollo NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl> | Il NPP non acquisisce dati. Chiamare [IRTC::Start](irtc-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt> </dl>  | Il NPP è connesso alla rete, ma non con il [metodo IRTC::Connessione.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Commenti

Quando si riavvia l'acquisizione dopo aver chiamato il metodo **IRTC::Stop,** assicurarsi di chiamare [IRTC::Configure](irtc-configure.md) ogni volta che si chiama [IRTC::Start](irtc-start.md) per riavviare l'acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Connessione](irtc-connect.md)
</dt> <dt>

[IRTC::Configure](irtc-configure.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> </dl>

 

 




