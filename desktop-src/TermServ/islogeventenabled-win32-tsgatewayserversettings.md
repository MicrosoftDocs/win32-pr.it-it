---
title: Metodo IsLogEventEnabled della classe Win32_TSGatewayServerSettings
description: Indica se il tipo di registro eventi specificato è abilitato.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLogEventEnabled
- Metodo IsLogEventEnabled Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo IsLogEventEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acefe60a9ba50c49146d25c7bccddf706f198c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301981"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Metodo IsLogEventEnabled della \_ classe TSGatewayServerSettings Win32

Indica se il tipo di registro eventi specificato è abilitato.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EventName* \[ in\]
</dt> <dd>

Nome del tipo di registro eventi. Questo valore deve essere recuperato tramite il metodo [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) .

<dt>

LogChannelDisconnect
</dt> <dd>

L'utente è stato disconnesso dalla risorsa.

</dd> <dt>

LogFailedChannelConnect
</dt> <dd>

L'utente non è riuscito a connettersi alla risorsa.

</dd> <dt>

LogFailureNetworkAccessCheck
</dt> <dd>

Autorizzazione connessione utente non riuscita.

</dd> <dt>

LogFailureResourceAccessCheck
</dt> <dd>

Autorizzazione risorse utente non riuscita.

</dd> <dt>

LogSuccessChannelConnect
</dt> <dd>

L'utente ha eseguito la connessione alla risorsa.

</dd> <dt>

LogSuccessfulNetworkAccessCheck
</dt> <dd>

L'utente ha superato l'autorizzazione di connessione.

</dd> <dt>

LogSuccessfulResourceAccessCheck
</dt> <dd>

L'utente ha superato l'autorizzazione risorse.

</dd> </dl> </dd> <dt>

*Abilitato* \[ out\]
</dt> <dd>

Indica se il tipo di registro eventi specificato è abilitato.

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

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

