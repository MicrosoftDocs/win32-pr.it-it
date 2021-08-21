---
title: Metodo SetName della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Imposta la proprietà Name per i Desktop remoto di autorizzazione delle risorse (RD \ 160; RAP).
ms.assetid: 3a652ece-11fe-4aa7-913d-39ef96ab1633
ms.tgt_platform: multiple
keywords:
- Metodo SetName Servizi Desktop remoto
- Metodo SetName Servizi Desktop remoto , Win32_TSGatewayResourceAuthorizationPolicy classe
- Win32_TSGatewayResourceAuthorizationPolicy classe Servizi Desktop remoto, metodo SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df296ec4fc9dbb1b28a6cc5382f8197241c7e8557192dcf2ffe30af19cf9bed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350012"
---
# <a name="setname-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Metodo SetName della classe \_ TSGatewayResourceAuthorizationPolicy Win32

Imposta la **proprietà Name** per i criteri Desktop remoto di autorizzazione delle risorse (RD RAP).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Nome dell'istanza di Criteri di gruppo di Desktop remoto. Il nome deve contenere al massimo 64 caratteri, univoco (la distinzione tra maiuscole e minuscole viene ignorata) e non può contenere i caratteri riservati seguenti:

<> : ; " / \\ \| ? \*\[TAB\]

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

