---
title: Metodo sedescription della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Imposta la proprietà Description per i criteri di autorizzazione delle risorse Desktop remoto (RD \ 160; RAP).
ms.assetid: 5a0f4c4b-50a4-4bd2-960f-8af7f4686d07
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo di descrizione
- Metodo sedescription Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo sedescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5dfdbcf67096dacc694061b5ff7e704c788bd2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400576"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Metodo sedescription della classe Win32 \_ TSGatewayResourceAuthorizationPolicy

Imposta la proprietà **Description** per i criteri di autorizzazione delle risorse Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrizione* \[ di in\]
</dt> <dd>

Descrizione del criterio di autorizzazione connessioni Desktop remoto.

</dd> </dl>

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

 

