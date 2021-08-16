---
title: Metodo SetServers della classe Win32_TSGatewayLoadBalancer
description: Imposta la proprietà Server con l'elenco di server di bilanciamento del carico Desktop remoto Gateway Desktop remoto.
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- Metodo SetServers Servizi Desktop remoto
- Metodo SetServers Servizi Desktop remoto , Win32_TSGatewayLoadBalancer classe
- Win32_TSGatewayLoadBalancer classe Servizi Desktop remoto , metodo SetServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.SetServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2c23ac6cf965687a022c5ae5ba8c1ce690c39c45f9149076f36ab13bc2d222
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349617"
---
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Metodo SetServers della classe \_ Win32 TSGatewayLoadBalancer

Imposta la **proprietà Server** con l'elenco dei server di bilanciamento del carico Desktop remoto Gateway Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Server* \[ Pollici\]
</dt> <dd>

Elenco delimitato da punto e virgola dei server di bilanciamento del carico di Gateway Desktop remoto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Se nel parametro *Servers sono* presenti più server e uno dei server non può essere elaborato, non verrà elaborato nessuno dei server.

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

