---
description: 'Metodo IESP::D isconnect: il metodo Disconnect disconnette il NPP dalla rete.'
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: Metodo IESP::D isconnect (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d0a07748781a567c889e879e2e99462d8cfb876a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110759"
---
# <a name="iespdisconnect-method"></a>Metodo IESP::D isconnect

Il **metodo Disconnect** disconnette il NPP dalla rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                          | Descrizione                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE DI \_ NMERR**</dt> </dl>      | Il NPP acquisisce i dati. Non è possibile disconnettersi dalla rete mentre è in corso l'acquisizione dei dati.<br/> |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl> | Il NPP non è connesso alla rete.<br/>                                                             |
| <dl> <dt>**NMERR \_ NON \_ ESP**</dt> </dl>       | Il NPP è connesso alla rete, ma non con il [metodo IESP::Connect.](iesp-connect.md)<br/>       |



 

## <a name="remarks"></a>Commenti

Questo metodo non può essere chiamato quando il NPP acquisisce dati. È necessario chiamare il **metodo IESP::Stop** prima di chiamare **IESP::D isconnect.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Connect](iesp-connect.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> </dl>

 

 




