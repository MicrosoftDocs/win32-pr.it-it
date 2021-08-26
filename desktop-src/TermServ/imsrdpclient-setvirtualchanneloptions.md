---
title: Metodo IMsRdpClient SetVirtualChannelOptions
description: Imposta le opzioni del canale virtuale per il controllo Desktop remoto ActiveX virtuale.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Metodo SetVirtualChannelOptions Servizi Desktop remoto
- Metodo SetVirtualChannelOptions Servizi Desktop remoto , interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto , interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto , interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto , metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto , interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto , metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto , interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto , metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto , interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto , interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto , interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto , interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto , interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto metodo SetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 804d4bde2fec9cb6273cc78f79d733f61a08772746439aa1cbb6e7b2d3c29716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871583"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a>Metodo IMsRdpClient::SetVirtualChannelOptions

Imposta le opzioni del canale virtuale per il controllo Desktop remoto ActiveX virtuale.

Chiamare questo metodo dopo aver chiamato il [**metodo CreateVirtualChannels,**](imstscax-createvirtualchannels.md) ma prima di stabilire una connessione con il [**metodo Connessione.**](imstscax-connect.md) Questo metodo imposta opzioni aggiuntive nei canali virtuali creati con **CreateVirtualChannels.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ChanName* \[ Pollici\]
</dt> <dd>

Nome del canale virtuale specificato nella chiamata al [**metodo CreateVirtualChannels.**](imstscax-createvirtualchannels.md)

</dd> <dt>

*chanOptions* \[ Pollici\]
</dt> <dd>

Opzioni da impostare per il canale virtuale specificato dal *parametro ChanName.* Per una descrizione delle opzioni possibili, vedere [**CHANNEL \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def). Per ulteriori informazioni, vedere la sezione Osservazioni successiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

Un esempio di utilizzo di questo metodo è la dichiarazione persistente del canale come controllo remoto impostando il flag **PERSISTENT CHANNEL OPTION REMOTE \_ \_ \_ CONTROL. \_** Ciò significa che il canale non verrebbe chiuso quando un controllo remoto si connette o si disconnette dalla sessione connessa al client. Per altre informazioni, vedere [Remote Control Persistent Virtual Channels](remote-control-persistent-virtual-channels.md).

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsRdpClient IID è definito come \_ 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



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

[**DEF \_ DEL CANALE**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





