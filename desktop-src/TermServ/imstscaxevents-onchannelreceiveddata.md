---
title: Metodo IMsTscAxEvents OnChannelReceivedData
description: Chiamato quando il client riceve i dati su un canale virtuale con script.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnChannelReceivedData
- Metodo OnChannelReceivedData Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnChannelReceivedData
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
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119630"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a>Metodo IMsTscAxEvents:: OnChannelReceivedData

Chiamato quando il client riceve i dati su un canale virtuale con script.

## <a name="syntax"></a>Sintassi


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*channame* \[ in\]
</dt> <dd>

Nome del canale virtuale in cui sono stati ricevuti i dati. Questo nome corrisponde a uno dei canali creati dalla chiamata a [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md).

</dd> <dt>

*dati* \[ di in\]
</dt> <dd>

Dati ricevuti sul canale virtuale con script.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su questo evento, vedere l'articolo relativo all' [implementazione di canali virtuali utilizzabili tramite script con connessione Web Desktop remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) .

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





