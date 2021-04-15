---
title: Metodo IMsRdpClient SetVirtualChannelOptions
description: Imposta le opzioni del canale virtuale per il controllo ActiveX Desktop remoto.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo SetVirtualChannelOptions
- Metodo SetVirtualChannelOptions Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo SetVirtualChannelOptions
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
ms.openlocfilehash: 10e727fd3486b9d1b31fb3a421ea6ff268949790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400396"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a>Metodo IMsRdpClient:: SetVirtualChannelOptions

Imposta le opzioni del canale virtuale per il controllo ActiveX Desktop remoto.

Chiamare questo metodo dopo avere chiamato il metodo [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) , ma prima di stabilire una connessione con il metodo [**Connect**](imstscax-connect.md) . Questo metodo consente di impostare opzioni aggiuntive nei canali virtuali creati con **CreateVirtualChannels**.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Channame* \[ in\]
</dt> <dd>

Nome del canale virtuale specificato nella chiamata al metodo [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .

</dd> <dt>

*chanOptions* \[ in\]
</dt> <dd>

Opzioni da impostare per il canale virtuale specificato dal parametro *channame* . Per una descrizione delle possibili opzioni, vedere [**Channel \_ def**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def). Per ulteriori informazioni, vedere la sezione Osservazioni successiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Un esempio di utilizzo di questo metodo consiste nel dichiarare il canale come controllo remoto persistente impostando il flag **\_ \_ \_ \_ permanente controllo remoto opzioni canale** . Ciò significa che il canale non verrà chiuso quando un controllo remoto si connette o si disconnette dalla sessione connessa al client. Per ulteriori informazioni, vedere la pagina relativa ai [canali virtuali persistenti del controllo remoto](remote-control-persistent-virtual-channels.md).

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a<br/>        |



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

[**\_def canale**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





