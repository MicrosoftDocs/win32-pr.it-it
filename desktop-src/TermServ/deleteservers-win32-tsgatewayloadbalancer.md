---
title: Metodo DeleteServers della classe Win32_TSGatewayLoadBalancer
description: Elimina i server dalla proprietà Servers.
ms.assetid: 5ef44725-82b6-464a-abab-a68cc8799669
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DeleteServers
- Metodo DeleteServers Servizi Desktop remoto, classe Win32_TSGatewayLoadBalancer
- Classe Win32_TSGatewayLoadBalancer Servizi Desktop remoto, metodo DeleteServers
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
ms.openlocfilehash: b889f37b783853fbca0b9cb399a83959e2522d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400328"
---
# <a name="deleteservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Metodo DeleteServers della \_ classe TSGatewayLoadBalancer Win32

Elimina i server dalla proprietà **Servers** .

## <a name="syntax"></a>Sintassi


```mof
uint32 DeleteServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Server* \[ di in\]
</dt> <dd>

Elenco delimitato da punti e virgola dei server di bilanciamento del carico di Gateway Desktop remoto da eliminare dalla proprietà **Server** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Se più server si trovano nel parametro *Server* e uno dei server non può essere elaborato, nessuno dei server verrà elaborato.

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

