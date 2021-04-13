---
title: Metodo IMsTscAx SendOnVirtualChannel
description: Invia dati al server host sessione Desktop remoto (host sessione Desktop remoto) su un canale virtuale creato in precedenza tramite il metodo CreateVirtualChannels.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo SendOnVirtualChannel
- Metodo SendOnVirtualChannel Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo SendOnVirtualChannel
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1371ae17978601a3194f755dd364d9227b8fc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475611"
---
# <a name="imstscaxsendonvirtualchannel-method"></a>Metodo IMsTscAx:: SendOnVirtualChannel

Invia dati al server host sessione Desktop remoto (host sessione Desktop remoto) su un canale virtuale creato in precedenza tramite il metodo [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Channame* \[ in\]
</dt> <dd>

Nome del canale virtuale specificato nella chiamata a [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).

</dd> <dt>

*ChanData* \[ in\]
</dt> <dd>

Dati da inviare sul canale virtuale, in formato **BSTR** . Non esiste alcuna restrizione che questi dati devono essere stringhe con terminazione null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Per informazioni sulle restrizioni di denominazione dei canali virtuali, vedere [registrazione client del canale virtuale](virtual-channel-client-registration.md) .

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





