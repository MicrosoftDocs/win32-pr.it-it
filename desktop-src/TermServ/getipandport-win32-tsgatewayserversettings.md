---
title: Metodo GetIPAndPort della classe Win32_TSGatewayServerSettings
description: Ottiene l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetIPAndPort
- Metodo GetIPAndPort Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo GetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340462"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo GetIPAndPort della \_ classe TSGatewayServerSettings Win32

Ottiene l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
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

*Indirizzo IP* \[ out\]
</dt> <dd>

Stringa che riceve l'indirizzo IP di ascolto, in formato ottetto (ad esempio, "192.168.1.1").

</dd> <dt>

*Porta* \[ out\]
</dt> <dd>

Specifica il numero della porta di attesa.

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

 

 





