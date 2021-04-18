---
title: Proprietà NetworkConnectionType di IMsRdpClientAdvancedSettings7
description: Ottiene o imposta il tipo di connessione di rete utilizzato tra il client e il server. Le informazioni sul tipo di connessione di rete passate al server consentono al server di ottimizzare diversi parametri in base al tipo di connessione di rete.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà NetworkConnectionType
- Servizi Desktop remoto proprietà NetworkConnectionType, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà NetworkConnectionType
- Servizi Desktop remoto proprietà NetworkConnectionType, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà NetworkConnectionType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301891"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a>Proprietà IMsRdpClientAdvancedSettings7:: NetworkConnectionType

Ottiene o imposta il tipo di connessione di rete utilizzato tra il client e il server. Le informazioni sul tipo di connessione di rete passate al server consentono al server di ottimizzare diversi parametri in base al tipo di connessione di rete.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a>Valore proprietà

Tipo di connessione di rete.

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Connessione \_ a TIPO \_ modem** (1 (0x1))


</dt> <dd>

Modem (56 Kbps)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Connessione \_ a TIPO \_ Broadband \_ low** (2 (0x2))


</dt> <dd>

Banda larga a bassa velocità (256 kbps a 2 Mbps)

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Connessione \_ a Digitare \_ satellite** (3 (0x3))


</dt> <dd>

Satellite (da 2 Mbps a 16 Mbps, con latenza elevata)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Connessione \_ a Digitare \_ Broadband \_ High** (4 (0x4))


</dt> <dd>

Banda larga ad alta velocità (da 2 Mbps a 10 Mbps)

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Connessione \_ a Digitare \_ WAN** (5 (0x5))


</dt> <dd>

WAN (Wide Area Network) (10 Mbps o superiore, con latenza elevata)

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Connessione \_ a Digitare \_ LAN** (6 (0x6))


</dt> <dd>

LAN (Local Area Network) (10 Mbps o versione successiva)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                             |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





