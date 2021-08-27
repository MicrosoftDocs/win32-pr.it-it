---
title: Metodo IMsTscAxEvents OnChannelReceivedData
description: Chiamato quando il client riceve i dati in un canale virtuale che può essere eseguito da script.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Metodo OnChannelReceivedData Servizi Desktop remoto
- Metodo OnChannelReceivedData Servizi Desktop remoto , interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnChannelReceivedData
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f411eae7e03f134f4adfd6fdc6108634e4e58c06bb8645e9f97f27e8489a3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125191"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a>Metodo IMsTscAxEvents::OnChannelReceivedData

Chiamato quando il client riceve i dati in un canale virtuale che può essere eseguito da script.

## <a name="syntax"></a>Sintassi


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chanName* \[ Pollici\]
</dt> <dd>

Nome del canale virtuale in cui sono stati ricevuti i dati. Questo nome corrisponde a uno dei canali creati dalla chiamata a [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md).

</dd> <dt>

*dati* \[ Pollici\]
</dt> <dd>

Dati ricevuti nel canale virtuale che può essere eseguito tramite script.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per altre [informazioni su questo evento, vedere Implementing Scriptable Virtual Channels using Connessione Web Desktop remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) (Implementazione di canali virtuali Connessione Web Desktop remoto script).

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





