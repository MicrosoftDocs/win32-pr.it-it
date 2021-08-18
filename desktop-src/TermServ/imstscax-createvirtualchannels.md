---
title: Metodo IMsTscAx CreateVirtualChannels
description: Crea un oggetto canale virtuale lato client per ogni nome di canale virtuale specificato.
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- Metodo CreateVirtualChannels Servizi Desktop remoto
- Metodo CreateVirtualChannels Servizi Desktop remoto , interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto , metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto , interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto , interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto , metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto , interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto , metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto , interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto , metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto , interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto , metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto , interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto , metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto , interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto , interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto metodo CreateVirtualChannels
- Metodo CreateVirtualChannels Servizi Desktop remoto , interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto , metodo CreateVirtualChannels
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d3ef4e7c8471c655d4ecfaf54a1c4b0f35b2362c67c334bd94e57da8e99d390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138484"
---
# <a name="imstscaxcreatevirtualchannels-method"></a>Metodo IMsTscAx::CreateVirtualChannels

Crea un oggetto canale virtuale lato client per ogni nome di canale virtuale specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ Pollici\]
</dt> <dd>

Elenco delimitato da virgole di nomi di canali virtuali validi. La lunghezza di ogni nome in questo elenco può essere almeno uno e un massimo di sette caratteri alfabetici. La lunghezza dell'intera stringa può essere almeno uno e un massimo di 300 caratteri alfabetici.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo. Restituisce **E \_ INVALIDARG** se il parametro passato non soddisfa i criteri specificati.

## <a name="remarks"></a>Commenti

Chiamare questo metodo prima di chiamare [**il Connessione.**](imstscax-connect.md)

Per informazioni [sulle restrizioni di denominazione dei canali](virtual-channel-client-registration.md) virtuali, vedere Registrazione client del canale virtuale.

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAx IID è definito come \_ 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





