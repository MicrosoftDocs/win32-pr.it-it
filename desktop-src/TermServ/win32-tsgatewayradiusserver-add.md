---
title: Metodo Add della classe Win32_TSGatewayRADIUSServer
description: Aggiunge un nuovo server Remote Authentication Dial-In User Service (RADIUS).
ms.assetid: 78f74bb6-8f70-4bc1-8e4d-1670a3ae3f31
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Aggiungi metodo
- Aggiungi Servizi Desktop remoto metodo, interfaccia Win32_TSGatewayRADIUSServer
- Interfaccia Win32_TSGatewayRADIUSServer Servizi Desktop remoto, Aggiungi metodo
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Add
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6869c55a6704944c34c68af065875cad92e8385c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302428"
---
# <a name="add-method-of-the-win32_tsgatewayradiusserver-class"></a>Metodo Add della \_ classe TSGatewayRADIUSServer di Win32

Aggiunge un nuovo server Remote Authentication Dial-In User Service (RADIUS).

## <a name="syntax"></a>Sintassi


```mof
uint32 Add(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ in\]
</dt> <dd>

Nome del server RADIUS.

</dd> <dt>

*SharedSecret* \[ in\]
</dt> <dd>

Segreto condiviso per il server RADIUS.

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

 

