---
title: Metodo SetPortNumbers della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Imposta i numeri di porta consentiti per la connessione alla risorsa tramite Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetPortNumbers
- Metodo SetPortNumbers Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo SetPortNumbers
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b938435abab23e3ad27cf13dbe65e64b9ec859eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477722"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Metodo SetPortNumbers della \_ classe TSGatewayResourceAuthorizationPolicy Win32

Imposta i numeri di porta consentiti per la connessione alla risorsa tramite Gateway Desktop remoto (Gateway Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PortNumbers* \[ in\]
</dt> <dd>

Elenco di numeri di porta separati da punti e virgola consentiti per questo Desktop remoto Criteri di autorizzazione risorse (RD RAP). Per consentire qualsiasi numero di porta, impostare " \* ".

</dd> </dl>

## <a name="remarks"></a>Commenti

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

 

