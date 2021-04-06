---
title: Metodo SetSharedSecret della classe Win32_TSGatewayRADIUSServer
description: Imposta la proprietà SharedSecret per questo server Remote Authentication Dial-In User Service (RADIUS).
ms.assetid: b4f7afb7-862f-4c30-b60a-aa6a8dbbe3e9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSharedSecret
- Metodo SetSharedSecret Servizi Desktop remoto, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Servizi Desktop remoto, metodo SetSharedSecret
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetSharedSecret
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f17e22061467194bdb09fc3f2c6105706f58e587
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742367"
---
# <a name="setsharedsecret-method-of-the-win32_tsgatewayradiusserver-class"></a>Metodo SetSharedSecret della \_ classe TSGatewayRADIUSServer Win32

Imposta la proprietà **SharedSecret** per questo server Remote Authentication Dial-in User Service (RADIUS).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSharedSecret(
  [in] string SharedSecret
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SharedSecret* \[ in\]
</dt> <dd>

Nuovo segreto condiviso.

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

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

