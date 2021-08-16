---
title: Metodo GetIPAndPort della Win32_TSGatewayServerSettings classe
description: Ottiene l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Metodo GetIPAndPort Servizi Desktop remoto
- Metodo GetIPAndPort Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto metodo , GetIPAndPort
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
ms.openlocfilehash: faf1cb1d4f597e734ac66456cd515193afed5ad31b7b6543d4e52c09717346a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353852"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo GetIPAndPort della classe \_ Win32 TSGatewayServerSettings

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

*Indirizzo IP* \[ Cambio\]
</dt> <dd>

Stringa che riceve l'indirizzo IP di ascolto, in formato ottetto (ad esempio, "192.168.1.1").

</dd> <dt>

*Porta* \[ Cambio\]
</dt> <dd>

Specifica il numero di porta di ascolto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





