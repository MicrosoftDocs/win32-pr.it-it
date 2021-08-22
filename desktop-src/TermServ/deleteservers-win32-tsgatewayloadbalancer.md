---
title: Metodo DeleteServers della classe Win32_TSGatewayLoadBalancer
description: Elimina i server dalla proprietà Server.
ms.assetid: 5ef44725-82b6-464a-abab-a68cc8799669
ms.tgt_platform: multiple
keywords:
- Metodo DeleteServers Servizi Desktop remoto
- Metodo DeleteServers Servizi Desktop remoto , Win32_TSGatewayLoadBalancer classe
- Win32_TSGatewayLoadBalancer classe Servizi Desktop remoto , metodo DeleteServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3c37380694706a368fb834807460c9625eb2317e87e3e5523cb93b49d9b16f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609606"
---
# <a name="deleteservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Metodo DeleteServers della classe \_ Win32 TSGatewayLoadBalancer

Elimina i server dalla **proprietà Server.**

## <a name="syntax"></a>Sintassi


```mof
uint32 DeleteServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Server* \[ Pollici\]
</dt> <dd>

Elenco delimitato da punto e virgola dei server di bilanciamento del carico di Gateway Desktop remoto da eliminare dalla **proprietà Server.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Se nel parametro *Servers sono* presenti più server e uno dei server non può essere elaborato, non verrà elaborato nessuno dei server.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per Windows di strumentazione di gestione (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

