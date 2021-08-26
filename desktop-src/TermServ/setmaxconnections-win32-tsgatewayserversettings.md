---
title: Metodo SetMaxConnections della classe Win32_TSGatewayServerSettings
description: Imposta le proprietà MaxConnections e UnlimitedConnections, che controllano il numero massimo di connessioni consentite al server Desktop remoto Gateway Desktop remoto.
ms.assetid: cfdbacb7-4969-4ec5-8301-e8020f3af0cd
ms.tgt_platform: multiple
keywords:
- Metodo SetMaxConnections Servizi Desktop remoto
- Metodo SetMaxConnections Servizi Desktop remoto , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Servizi Desktop remoto, metodo SetMaxConnections
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetMaxConnections
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e241b137f2a3a061be06538b934c163ea6445ff177fecf9aaf4dc7db5367990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009047"
---
# <a name="setmaxconnections-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo SetMaxConnections della classe \_ TSGatewayServerSettings Win32

Imposta le **proprietà MaxConnections** e **UnlimitedConnections,** che controllano il numero massimo di connessioni consentite al server Desktop remoto Gateway Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetMaxConnections(
  [in] uint32  Connections,
  [in] boolean IsUnlimited
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Connessioni* \[ Pollici\]
</dt> <dd>

Numero di connessioni che il server deve accettare. Per un numero illimitato di connessioni, impostare il *parametro IsUnlimited* su **True.**

</dd> <dt>

*IsUnlimited* \[ Pollici\]
</dt> <dd>

Se **True,** le connessioni al servizio non sono limitate a un numero specifico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

