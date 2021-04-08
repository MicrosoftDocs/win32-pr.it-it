---
title: Metodo Sename della classe Win32_TSGatewayRADIUSServer
description: Imposta la proprietà Name per questo server Remote Authentication Dial-In User Service (RADIUS).
ms.assetid: 2dabc6fb-7740-4039-9bbd-5b2490fe5988
ms.tgt_platform: multiple
keywords:
- Metodo senamer Servizi Desktop remoto
- Metodo senamer Servizi Desktop remoto, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Servizi Desktop remoto, metodo SetValue
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc4b563c59ce1546b4cf471653407e3390676625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741482"
---
# <a name="setname-method-of-the-win32_tsgatewayradiusserver-class"></a>Metodo Sename della classe Win32 \_ TSGatewayRADIUSServer

Imposta la proprietà **Name** per questo server Remote Authentication Dial-in User Service (RADIUS).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ in\]
</dt> <dd>

Nuovo nome.

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

 

