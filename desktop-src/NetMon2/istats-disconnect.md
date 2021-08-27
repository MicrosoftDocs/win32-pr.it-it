---
description: Disconnette NPP dalla rete.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: Metodo IStats::D isconnect (Netmon.h)
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
ms.openlocfilehash: eabba7b5cf234d48b2839074ec1ad07380a7ed14858f6bd43b07f7d2eaa033b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037191"
---
# <a name="istatsdisconnect-method"></a>Metodo IStats::D isconnect

Il **metodo Disconnect** disconnette NPP dalla rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                            | Descrizione                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE DI \_ NMERR**</dt> </dl>        | NPP sta attualmente acquisendo dati. Non è possibile disconnettersi dalla rete mentre è in corso un'acquisizione dati.<br/> |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>   | NPP non è connesso alla rete.<br/>                                                                         |
| <dl> <dt>**NMERR \_ NON \_ STATS \_ ONLY**</dt> </dl> | NPP è connesso alla rete, ma non con il [**metodo IStats::Connessione.**](istats-connect.md)<br/>          |



 

## <a name="remarks"></a>Commenti

Questo metodo non può essere chiamato quando il NPP acquisisce i dati. Chiamare prima il metodo **IStats::D isconnect** e quindi [**IStats::Stop**](istats-stop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IStat**](istats.md)
</dt> <dt>

[**IStats::Connessione**](istats-connect.md)
</dt> <dt>

[**IStats::Stop**](istats-stop.md)
</dt> </dl>

 

 




