---
description: Win32 \_ DCOMApplicationSetting&\# 8194; Classe WMI che rappresenta le impostazioni di un'applicazione DCOM.
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305274"
---
# <a name="win32_dcomapplicationsetting-class"></a>Win32 \_ DCOMApplicationSetting (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DCOMApplicationSetting Win32** rappresenta le impostazioni di un'applicazione DCOM. Contiene le opzioni di configurazione DCOM associate alla chiave **AppID** nel registro di sistema. Queste opzioni sono valide per i componenti raggruppati logicamente sotto la classe dell'applicazione specificata.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ DCOMApplicationSetting** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ DCOMApplicationSetting** presenta questi metodi.



| Metodo                                                                                                                        | Descrizione                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAccessSecurityDescriptor**](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Ottiene il descrittore di sicurezza che controlla gli utenti autorizzati ad accedere a un'applicazione DCOM.<br/>                                                                                                                              |
| [**GetConfigurationSecurityDescriptor**](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Ottiene il descrittore di sicurezza che controlla gli utenti autorizzati a configurare un'applicazione DCOM.<br/>                                                                                                                           |
| [**GetLaunchSecurityDescriptor**](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | Ottiene il descrittore di sicurezza che controlla gli utenti autorizzati ad avviare un'applicazione DCOM.<br/>                                                                                                                              |
| [**SetAccessSecurityDescriptor**](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Aggiorna il descrittore di sicurezza di accesso dell'applicazione DCOM con un nuovo descrittore di sicurezza definito da un'istanza della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/>        |
| [**SetConfigurationSecurityDescriptor**](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | Aggiorna il descrittore di sicurezza della configurazione dell'applicazione DCOM con un nuovo descrittore di sicurezza definito da un'istanza della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/> |
| [**SetLaunchSecurityDescriptor**](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | Aggiorna il descrittore di sicurezza di avvio dell'applicazione DCOM con un nuovo descrittore di sicurezza definito da un'istanza della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .<br/>        |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ DCOMApplicationSetting** dispone di queste proprietà.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ default \] ")
</dt> </dl>

Identificatore univoco globale (GUID) per l'applicazione DCOM.

</dd> <dt>

**AuthenticationLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] ")
</dt> </dl>

Livello di autenticazione client minimo richiesto da questo server COM. Se **null**, vengono utilizzati i valori predefiniti.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (1)


</dt> <dd>

Nessuno (nessuna autenticazione eseguita)

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Connetti** (2)


</dt> <dd>

Connetti (l'autenticazione viene eseguita solo quando il client stabilisce una relazione con l'applicazione)

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>**Chiamata** (3)


</dt> <dd>

Call (l'autenticazione viene eseguita solo all'inizio di ogni chiamata quando l'applicazione riceve la richiesta)

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Pacchetto** (4)


</dt> <dd>

Pacchetto (l'autenticazione viene eseguita su tutti i dati ricevuti dal client)

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)


</dt> <dd>

PacketIntegrity (tutti i dati trasferiti tra il client e l'applicazione vengono autenticati e verificati)

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)


</dt> <dd>

PacketPrivacy (vengono usate le proprietà degli altri livelli di autenticazione e tutti i dati sono crittografati)

</dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**CustomSurrogate**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")
</dt> </dl>

Nome del surrogato personalizzato in cui è attivata l'applicazione DCOM in-process. Se questo valore è **null** e la chiave **UseSurrogate** è **true**, il sistema fornisce un processo surrogato.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**EnableAtStorageActivation**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ ActivateAtStorage \] ")
</dt> </dl>

L'applicazione DCOM recupera lo stato salvato dell'applicazione o inizia dallo stato in cui l'applicazione viene inizializzata per la prima volta.

</dd> <dt>

**LocalService**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")
</dt> </dl>

Nome dei servizi forniti dall'applicazione DCOM.

</dd> <dt>

**RemoteServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ RemoteServerName \] ")
</dt> </dl>

Nome del server remoto in cui è attivata l'applicazione.

</dd> <dt>

**RunAsUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ RunAs \] ")
</dt> </dl>

Account utente specifico con cui l'applicazione deve essere eseguita all'attivazione.

</dd> <dt>

**ServiceParameters**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ ServiceParameters \] ")
</dt> </dl>

Parametri della riga di comando passati all'applicazione DCOM. Questa operazione è valida solo se l'applicazione viene scritta come servizio basato su Windows.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**UseSurrogate**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")
</dt> </dl>

L'applicazione DCOM può essere attivata come server out-of-process usando un file eseguibile surrogato.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ DCOMApplicationSetting** è derivata dalla [**\_ comimpostazione Win32**](win32-comsetting.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Comimpostazioni Win32 \_**](win32-comsetting.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Costanti Privilege**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Oggetti descrittore di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Modifica della sicurezza di accesso per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

