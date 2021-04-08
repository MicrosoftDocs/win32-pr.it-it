---
title: Metodo Create della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Crea un criterio di autorizzazione di connessione Desktop remoto (RD \ 160; Con i valori specificati. Il nuovo RD \ 160; Il CAP verrà inserito nella parte superiore della RD \ 160; Ordine di valutazione CAP, con valore della proprietà Order pari a \ 0034; 1 \ 0034;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto crea metodo
- Create Method Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo create
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc027c2f7fc90318bd1af6fd1254077a860a5d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048029"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Metodo Create della classe Win32 \_ TSGatewayConnectionAuthorizationPolicy

Crea un criterio di autorizzazione di connessione Desktop remoto (RD) utilizzando i valori specificati. Il nuovo criterio di autorizzazione connessioni Desktop remoto verrà inserito all'inizio dell'ordine di valutazione del CAP RD, con un valore della proprietà **Order** pari a "1".

## <a name="syntax"></a>Sintassi


```mof
uint32 Create(
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

*Nome* \[ in\]
</dt> <dd>

Nome del CAP di desktop remoto. Il nome deve essere composto da un massimo di 64 caratteri, univoco (caso ignorato) e non può contenere i caratteri riservati seguenti:

<> :; " / \\ \| ? \*\[Scheda\]

</dd> <dt>

*UserGroupNames* \[ in\]
</dt> <dd>

Elenco di nomi di gruppi di utenti, separati da punti e virgola, per il nuovo CAP RD.

</dd> <dt>

*ComputerGroupNames* \[ in\]
</dt> <dd>

Elenco di nomi di gruppi di computer, separati da punti e virgola, per il nuovo CAP RD.

</dd> <dt>

*Smart Card* \[ in\]
</dt> <dd>

Specifica se è possibile utilizzare smart card per l'autenticazione con il server Gateway Desktop remoto.

</dd> <dt>

*Password* \[ di in\]
</dt> <dd>

Specifica se è possibile utilizzare le password per l'autenticazione con il server Gateway Desktop remoto.

</dd> <dt>

*SecureId* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> <dt>

*Abilitato* \[ in\]
</dt> <dd>

Specifica se il CAP RD è abilitato.

</dd> <dt>

*DeviceRedirectionType* \[ in\]
</dt> <dd>

Specifica i tipi di dispositivo che verranno reindirizzati.

<dt>

0
</dt> <dd>

Verranno reindirizzati tutti i dispositivi.

</dd> <dt>

1
</dt> <dd>

Non verrà reindirizzato alcun dispositivo.

</dd> <dt>

2
</dt> <dd>

I dispositivi specificati non verranno reindirizzati. I parametri *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* e *PlugAndPlayDevicesDisabled* controllano i dispositivi che non verranno reindirizzati.

</dd> </dl> </dd> <dt>

*DiskDrivesDisabled* \[ in\]
</dt> <dd>

Specifica se disabilitare il reindirizzamento dell'unità disco se il parametro *DeviceRedirectionType* è "2".

</dd> <dt>

*PrintersDisabled* \[ in\]
</dt> <dd>

Specifica se disabilitare il reindirizzamento della stampante se il parametro *DeviceRedirectionType* è "2".

</dd> <dt>

*SerialPortsDisabled* \[ in\]
</dt> <dd>

Specifica se disabilitare il reindirizzamento della porta seriale se il parametro *DeviceRedirectionType* è "2".

</dd> <dt>

*ClipboardDisabled* \[ in\]
</dt> <dd>

Specifica se disabilitare il reindirizzamento degli Appunti se il parametro *DeviceRedirectionType* è "2".

</dd> <dt>

*PlugAndPlayDevicesDisabled* \[ in\]
</dt> <dd>

Specifica se disabilitare il reindirizzamento dei dispositivi Plug and Play se il parametro *DeviceRedirectionType* è "2".

</dd> <dt>

*IdleTimeout* \[ in\]
</dt> <dd>

Valore di timeout di inattività in minuti

</dd> <dt>

*SessionTimeout* \[ in\]
</dt> <dd>

Valore di timeout della sessione in minuti

</dd> <dt>

*SessionTimeoutAction* \[ in\]
</dt> <dd>

Azione di timeout della sessione in minuti

</dd> <dt>

*AllowOnlySDRServers* \[ in\]
</dt> <dd>

Indica se le connessioni sono consentite solo ai server TS SDR

</dd> <dt>

*CookieAuthentication* \[ in\]
</dt> <dd>

Indica se l'autenticazione del cookie può essere utilizzata per la connessione al server Gateway Servizi terminal

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

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

