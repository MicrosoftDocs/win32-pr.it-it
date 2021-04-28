---
description: "Metodo IRTC::P ause: il metodo Pause sospende l'acquisizione corrente."
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: Metodo IRTC::P ause (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d42af1912365a4237889e4e46d0fb3343377c772
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110679"
---
# <a name="irtcpause-method"></a>Metodo IRTC::P ause

Il **metodo Pause** sospende l'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                           | Descrizione                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE NMERR \_ \_ SOSPESA**</dt> </dl> | L'acquisizione è già sospesa.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl>  | Il NPP non acquisisce dati. Chiamare [IRTC::Start](irtc-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>  | Il NPP non è connesso alla rete. Chiamare [IRTC::Connect](irtc-connect.md) per connettere il NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt> </dl>   | Il protocollo NPP è connesso alla rete, ma non con [il metodo IRTC::Connect.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione è sospesa, i nuovi fotogrammi non vengono acquisiti fino a quando non viene chiamato il metodo [IRTC::Resume](irtc-resume.md) per riavviare l'acquisizione.

Quando si usano i metodi **IRTC::P ause** e **IRTC::Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione ogni volta che l'acquisizione è in esecuzione. [](c.md)

Per riavviare l'acquisizione, [chiamare IRTC::Resume](irtc-resume.md). Per arrestare l'acquisizione, [chiamare IRTC::Stop](irtc-stop.md).

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

[IRTC::Connect](irtc-connect.md)
</dt> <dt>

[IRTC::Resume](irtc-resume.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




