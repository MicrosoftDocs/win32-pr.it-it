---
title: Metodo EnableTransport della classe Win32_TSGatewayServerSettings
description: Abilita o disabilita il trasporto specificato.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- Metodo EnableTransport Servizi Desktop remoto
- Metodo EnableTransport Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto metodo EnableTransport
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08087c4a28b0867f7457bed597a71c5156ea968fb50f3f2509c8da5ef3057fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059599"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo EnableTransport della classe \_ TSGatewayServerSettings Win32

Abilita o disabilita il trasporto specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TransportType* \[ Pollici\]
</dt> <dd>

Specifica il tipo di trasporto. Deve essere uno dei valori seguenti.

<dt>

0
</dt> <dd>

Trasporto RPC su HTTP.

</dd> <dt>

1
</dt> <dd>

Trasporto HTTP.

</dd> <dt>

2
</dt> <dd>

Trasporto UDP.

</dd> </dl> </dd> <dt>

*Abilita* \[ Pollici\]
</dt> <dd>

Specifica se il trasporto è abilitato o disabilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                           |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





