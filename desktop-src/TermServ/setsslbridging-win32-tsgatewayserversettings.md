---
title: Metodo SetSslBridging della classe Win32_TSGatewayServerSettings
description: Imposta il tipo di bridging SSL che verrà utilizzato dal server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSslBridging
- Metodo SetSslBridging Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo SetSslBridging
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400728"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo SetSslBridging della \_ classe TSGatewayServerSettings Win32

Imposta il tipo di bridging SSL che verrà utilizzato dal server Gateway Desktop remoto (Gateway Desktop remoto). Questo valore viene archiviato nella proprietà **SslBridging** .

> [!IMPORTANT]
> Quando il tipo di bridging SSL viene modificato con questo metodo, il servizio Gateway Desktop remoto deve essere riavviato per rendere effettiva la modifica.

 

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SslBridging* \[ in\]
</dt> <dd>

Tipo: **UInt32**

Specifica il nuovo valore di bridging SSL. Può corrispondere a uno dei valori seguenti.

<dt>

0
</dt> <dd>

Nessun bridging SSL.

</dd> <dt>

1
</dt> <dd>

Bridging da HTTPS a HTTP.

</dd> <dt>

2
</dt> <dd>

Bridging da HTTPS a HTTPS.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                        |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

