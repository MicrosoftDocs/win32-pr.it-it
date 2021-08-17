---
title: Metodo SetIPAndPort della classe Win32_TSGatewayServerSettings
description: Imposta l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Metodo SetIPAndPort Servizi Desktop remoto
- Metodo SetIPAndPort Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto, metodo SetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af40c52523869e07268a26d858e0e70b933431a6583998c9d0041f476678d243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137974"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo SetIPAndPort della classe \_ TSGatewayServerSettings Win32

Imposta l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
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

*Indirizzo IP* \[ Pollici\]
</dt> <dd>

Specifica l'indirizzo IP di ascolto, in formato ottetto (ad esempio, "192.168.1.1").

</dd> <dt>

*Porta* \[ Pollici\]
</dt> <dd>

Specifica il numero di porta di ascolto.

</dd> <dt>

*OverrideExisting* \[ Pollici\]
</dt> <dd>

Indica se eseguire l'override dell'associazione IP/porta esistente per HTTP. Questo parametro viene usato solo se il *parametro TransportType* contiene 0 (RPC su HTTP) o 1 (HTTP).

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

 

 





