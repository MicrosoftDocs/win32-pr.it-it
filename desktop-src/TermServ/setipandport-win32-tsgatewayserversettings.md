---
title: Metodo SetIPAndPort della classe Win32_TSGatewayServerSettings
description: Imposta l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetIPAndPort
- Metodo SetIPAndPort Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo SetIPAndPort
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
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517686"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo SetIPAndPort della \_ classe TSGatewayServerSettings Win32

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

*TransportType* \[ in\]
</dt> <dd>

Specifica il tipo di trasporto. Deve essere uno dei valori seguenti.

<dt>

0
</dt> <dd>

RPC sul trasporto HTTP.

</dd> <dt>

1
</dt> <dd>

Trasporto HTTP.

</dd> <dt>

2
</dt> <dd>

Trasporto UDP.

</dd> </dl> </dd> <dt>

*Indirizzo IP* \[ in\]
</dt> <dd>

Specifica l'indirizzo IP di ascolto, in formato ottetto (ad esempio, "192.168.1.1").

</dd> <dt>

*Porta* \[ in\]
</dt> <dd>

Specifica il numero della porta di attesa.

</dd> <dt>

*OverrideExisting* \[ in\]
</dt> <dd>

Indica se eseguire l'override dell'associazione IP/porta esistente per HTTP. Questo parametro viene usato solo se il parametro *TransportType* contiene 0 (RPC su http) o 1 (http).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





