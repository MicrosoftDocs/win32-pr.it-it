---
title: Metodo IsTransportEnabled della classe Win32_TSGatewayServerSettings
description: Determina se il trasporto specificato è abilitato.
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- Metodo IsTransportEnabled Servizi Desktop remoto
- Metodo IsTransportEnabled Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto metodo , IsTransportEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7960748228e11f3749cd86daa2a323ca32ab9b05e1c17f98261ad4ae62b0fc9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515081"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo IsTransportEnabled della classe \_ TSGatewayServerSettings Win32

Determina se il trasporto specificato è abilitato.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
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

*Abilitato* \[ Cambio\]
</dt> <dd>

Valore **booleano** che indica se il trasporto è abilitato.

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

 

 





