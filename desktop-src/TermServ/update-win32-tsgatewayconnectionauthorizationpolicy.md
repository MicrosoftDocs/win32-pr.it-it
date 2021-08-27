---
title: Metodo Update della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Aggiorna i criteri di Desktop remoto di connessione corrente (Rd \ 160; CAP).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Metodo Update Servizi Desktop remoto
- Metodo Update Servizi Desktop remoto , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Servizi Desktop remoto , metodo Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ec7c3d1802f4faa3da8e382d00aa14fc8b3e091baef9659ad45322ec2a909c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118850880"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo Update della classe \_ TSGatewayConnectionAuthorizationPolicy Win32

Aggiorna i criteri di autorizzazione Desktop remoto connessione desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 Update(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Nome del cap rd. Il nome deve contenere al massimo 64 caratteri, univoco (la distinzione tra maiuscole e minuscole viene ignorata) e non può contenere i caratteri riservati seguenti:

<> : ; " / \\ \| ? \*\[SCHEDA\]

</dd> <dt>

*UserGroupNames* \[ Pollici\]
</dt> <dd>

Elenco di nomi di gruppi di utenti separati da punti e virgola. I nomi sono nel formato *Dominio \\ UserGroupName*. Se l'utente appartiene a uno di questi gruppi di utenti, l'utente sarà autorizzato ad accedere al server Gateway Desktop remoto.

</dd> <dt>

*ComputerGroupNames* \[ Pollici\]
</dt> <dd>

Elenco di nomi di gruppi di computer separati da punto e virgola. Questo valore può essere vuoto. I nomi sono nel formato *Dominio \\ ComputerGroupName*. Se viene specificato un valore, il computer client deve appartenere a uno di questi gruppi di computer per l'accesso dell'utente al server Gateway Desktop remoto.

</dd> <dt>

*SmartCard* \[ Pollici\]
</dt> <dd>

Specifica se le smart card possono essere usate per l'autenticazione con il server Gateway Desktop remoto.

</dd> <dt>

*Password* \[ Pollici\]
</dt> <dd>

Specifica se è possibile usare le password per l'autenticazione con il server Gateway Desktop remoto.

</dd> <dt>

*SecureId* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> <dt>

*Abilitato* \[ Pollici\]
</dt> <dd>

Specifica se questo criterio di autorizzazione connessioni Desktop remoto è abilitato.

</dd> <dt>

*DeviceRedirectionType* \[ Pollici\]
</dt> <dd>

Specifica i tipi di dispositivo che verranno reindirizzati.

<dt>

0
</dt> <dd>

Tutti i dispositivi verranno reindirizzati.

</dd> <dt>

1
</dt> <dd>

Nessun dispositivo verrà reindirizzato.

</dd> <dt>

2
</dt> <dd>

I dispositivi specificati non verranno reindirizzati. I parametri *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* e *PlugAndPlayDevicesDisabled* controllano quali dispositivi non verranno reindirizzati.

</dd> </dl> </dd> <dt>

*DiskDrivesDisabled* \[ Pollici\]
</dt> <dd>

Specifica se disabilitare il reindirizzamento delle unità disco se il *parametro DeviceRedirectionType* è "2".

</dd> <dt>

*StampantiDisabled* \[ Pollici\]
</dt> <dd>

Specifica se disabilitare il reindirizzamento della stampante se il *parametro DeviceRedirectionType* è "2".

</dd> <dt>

*SerialPortsDisabled* \[ Pollici\]
</dt> <dd>

Specifica se disabilitare il reindirizzamento delle porte seriali se il *parametro DeviceRedirectionType* è "2".

</dd> <dt>

*AppuntiDisabled* \[ Pollici\]
</dt> <dd>

Specifica se disabilitare il reindirizzamento degli Appunti se il *parametro DeviceRedirectionType* è "2".

</dd> <dt>

*PlugAndPlayDevicesDisabled* \[ Pollici\]
</dt> <dd>

Specifica se disabilitare il reindirizzamento Plug and Play dispositivi se il *parametro DeviceRedirectionType* è "2".

</dd> <dt>

*IdleTimeout* \[ Pollici\]
</dt> <dd>

Valore di timeout di inattività in minuti

</dd> <dt>

*SessionTimeout* \[ Pollici\]
</dt> <dd>

Valore di timeout sessione in minuti

</dd> <dt>

*SessionTimeoutAction* \[ Pollici\]
</dt> <dd>

Azione di timeout sessione in minuti

</dd> <dt>

*AllowOnlySDRServers* \[ Pollici\]
</dt> <dd>

Indica se le connessioni sono consentite solo ai server TS SDR

</dd> <dt>

*CookieAuthentication* \[ Pollici\]
</dt> <dd>

Indica se è possibile usare l'autenticazione tramite cookie per connettersi al server gateway di Servizi terminal

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

