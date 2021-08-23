---
title: Metodo DisablePrinters della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà PrintersDisabled. Se il valore della proprietà DeviceRedirectionType è \ 0034;2 \ 0034;, la proprietà PrintersDisabled controlla il reindirizzamento delle stampanti per le sessioni stabilite tramite il server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: bf58d226-e3de-4c2b-aaa9-9e7ddbf49d31
ms.tgt_platform: multiple
keywords:
- Metodo DisablePrinters Servizi Desktop remoto
- Metodo DisablePrinters Servizi Desktop remoto , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Servizi Desktop remoto , metodo DisablePrinters
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePrinters
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f89ba8110d60df83410d0904d68b32cb849bfadbff7205f969842cb71a385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657981"
---
# <a name="disableprinters-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo DisablePrinters della classe \_ TSGatewayConnectionAuthorizationPolicy Win32

Imposta la **proprietà PrintersDisabled.** Se il valore della proprietà **DeviceRedirectionType** è "2", la proprietà **PrintersDisabled** controlla il reindirizzamento delle stampanti per le sessioni stabilite tramite il server Gateway Desktop remoto (Gateway Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 DisablePrinters(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disabilitato* \[ Pollici\]
</dt> <dd>

Nuovo valore per la **proprietà PrintersDisabled.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco dei codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

