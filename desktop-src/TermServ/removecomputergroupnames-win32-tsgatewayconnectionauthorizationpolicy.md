---
title: Metodo RemoveComputerGroupNames della Win32_TSGatewayConnectionAuthorizationPolicy classe
description: Rimuove i nomi dei gruppi di computer specificati dalla proprietà ComputerGroupNames.
ms.assetid: 5f4e566a-1a2e-459d-ab6c-53ffd42271d8
ms.tgt_platform: multiple
keywords:
- Metodo RemoveComputerGroupNames Servizi Desktop remoto
- Metodo RemoveComputerGroupNames Servizi Desktop remoto , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Servizi Desktop remoto, metodo RemoveComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2df87623ff9a6fe4ee7596b21db3fc03957473c1be8b0bff421aa342864edfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127621"
---
# <a name="removecomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo RemoveComputerGroupNames della classe \_ Win32 TSGatewayConnectionAuthorizationPolicy

Rimuove i nomi dei gruppi di computer specificati **dalla proprietà ComputerGroupNames.**

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerGroupNames* \[ Pollici\]
</dt> <dd>

Elenco delimitato da punto e virgola dei nomi dei gruppi di computer da rimuovere dalla **proprietà ComputerGroupNames.** I nomi dei gruppi di computer devono essere nel formato *\\ DominioNomeGruppoComputer*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco dei codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Commenti

Se nel parametro *ComputerGroupNames* sono presenti più nomi di gruppo di computer e uno dei nomi non può essere elaborato, non verrà elaborato nessuno dei nomi.

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

