---
title: Metodo SetResourceGroup della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Imposta il tipo e il nome del gruppo di risorse.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetResourceGroup
- Metodo SetResourceGroup Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo SetResourceGroup
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22c2ceacbbbfc40372d0f0d084cf6525f754934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874137"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Metodo SetResourceGroup della \_ classe TSGatewayResourceAuthorizationPolicy Win32

Imposta il tipo e il nome del gruppo di risorse.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ResourceGroupName* \[ in\]
</dt> <dd>

Nome del gruppo di risorse. Questo valore sostituisce la proprietà **ResourceGroupName** esistente.

</dd> <dt>

*ResourceGroupType* \[ in\]
</dt> <dd>

Identifica il tipo del gruppo di risorse. Questo valore sostituisce la proprietà **ResourceGroupType** esistente.

<dt>

RG
</dt> <dd>

Gruppo di risorse.

</dd> <dt>

CG
</dt> <dd>

Gruppo di computer, come Archiviato in Active Directory Domain Services.

</dd> <dt>

TUTTI
</dt> <dd>

Tutte le risorse.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

