---
title: Metodo IMsRdpClient GetVirtualChannelOptions
description: Recupera le opzioni impostate per un canale virtuale.
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- Metodo GetVirtualChannelOptions Servizi Desktop remoto
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto metodo , GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo GetVirtualChannelOptions
- Metodo GetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto metodo , GetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d51ad6ccd1924c78817f76f385d65e1963b68c1b1329c3d6ba924f25a827a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059089"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a>Metodo IMsRdpClient::GetVirtualChannelOptions

Recupera le opzioni impostate per un canale virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ChanName* \[ Pollici\]
</dt> <dd>

Nome di un canale virtuale specificato nella chiamata al [**metodo CreateVirtualChannels.**](imstscax-createvirtualchannels.md)

</dd> <dt>

*pChanOptions* \[ Cambio\]
</dt> <dd>

Opzioni impostate per il canale virtuale specificato dal *parametro ChanName.* Per una descrizione delle opzioni possibili, vedere [**CHANNEL \_ DEF.**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient è definito come 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**CHANNEL \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





