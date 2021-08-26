---
title: Win32_TSAccount classe
description: Consente l'eliminazione di un account esistente nel terminale Win32 \_ e la modifica delle autorizzazioni esistenti.
ms.assetid: fd4d8a0f-685b-4619-84f1-faefbabd04ba
ms.tgt_platform: multiple
keywords:
- Win32_TSAccount classe Servizi Desktop remoto
- Win32_TSAccount classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSAccount
- Win32_TSAccount.Caption
- Win32_TSAccount.Description
- Win32_TSAccount.InstallDate
- Win32_TSAccount.Name
- Win32_TSAccount.Status
- Win32_TSAccount.TerminalName
- Win32_TSAccount.AccountName
- Win32_TSAccount.AuditFail
- Win32_TSAccount.AuditSuccess
- Win32_TSAccount.PermissionsAllowed
- Win32_TSAccount.PermissionsDenied
- Win32_TSAccount.SID
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51dd20046f24f8dbe27d884b04d688b70629fd06509d7a7b5e5a492eb97087a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008530"
---
# <a name="win32_tsaccount-class"></a>Classe TSAccount Win32 \_

La classe WMI **\_ Win32 TSAccount** consente l'eliminazione di un account esistente nel [**\_ terminale Win32**](win32-terminal.md) e la modifica delle autorizzazioni esistenti.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico. Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSACCOUNT_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSAccount : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   AccountName;
  uint32   AuditFail;
  uint32   AuditSuccess;
  uint32   PermissionsAllowed;
  uint32   PermissionsDenied;
  string   SID;
};
```

## <a name="members"></a>Members

La **classe \_ TSAccount Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ TSAccount Win32** dispone di questi metodi.



| Metodo                                                                   | Descrizione                                                                                  |
|:-------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Elimina**](win32-tsaccount-delete.md)                                 | Elimina l'account utente, gruppo o computer specificato.<br/>                           |
| [**ModifyAuditPermissions**](win32-tsaccount-modifyauditpermissions.md) | Modifica la granularità del set di autorizzazioni di controllo dell'account specificato.<br/> |
| [**Autorizzazioni di modifica**](win32-tsaccount-modifypermissions.md)           | Imposta un set di autorizzazioni più granulare sull'account specificato.<br/>                     |



 

### <a name="properties"></a>Proprietà

La **classe \_ Win32 TSAccount** ha queste proprietà.

<dl> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome corrente dell'account. Il nome di dominio è incluso.

</dd> <dt>

**AuditFail**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le autorizzazioni [Desktop remoto servizi host sessione](terminal-services-permissions.md) che vengono controllati per una condizione di errore. Il valore di questa proprietà è una maschera di bit, che può essere impostata su uno o più valori della **proprietà PermissionsAllowed.**

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

**WINSTATION \_ QUERY=0x1** (0)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

**WINSTATION \_ SET=0x2** (1)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

**WINSTATION \_ LOGOFF=0x4** (2)


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

**WINSTATION \_ VIRTUAL \| STANDARD RIGHTS REQUIRED = \_ \_ 0xF008** (3)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

**WINSTATION \_ SHADOW=0x10** (4)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

**WINSTATION \_ LOGON=0x20** (5)


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

**WINSTATION \_ MSG=0x80** (6)


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

**WINSTATION \_ CONNECT=0x100** (7)


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

**WINSTATION \_ DISCONNECT=0x200** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**AuditSuccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le autorizzazioni specifiche del server Host sessione Desktop remoto che vengono verificate per una condizione di esito positivo. Il valore di questa proprietà è una maschera di bit, che può essere impostata su uno o più valori della **proprietà PermissionsAllowed.**

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

**WINSTATION \_ QUERY=0x1** (0)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

**WINSTATION \_ SET=0x2** (1)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_logoff_0x4winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_LOGOFF_0X4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

**WINSTATION \_ LOGOFF=0x4WINSTATION \_ VIRTUAL STANDARD RIGHTS REQUIRED = \| \_ \_ 0xF008** (2)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

**WINSTATION \_ SHADOW=0x10** (3)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

**WINSTATION \_ LOGON=0x20** (4)


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

**WINSTATION \_ MSG=0x80** (5)


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

**WINSTATION \_ CONNECT=0x100** (6)


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

**WINSTATION \_ DISCONNECT=0x200** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione (stringa di una riga) dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**mappingstring**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Data di installazione dell'oggetto. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Autorizzazioni consentite**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le autorizzazioni [Servizi Desktop remoto consentite](terminal-services-permissions.md) per l'account. Il valore di questa proprietà è una maschera di bit, che può essere impostata su uno o più dei valori seguenti.

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION \_ QUERY=0x1** (1)


</dt> <dd>

Autorizzazione per eseguire query sulle informazioni su una sessione.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ SET** (2)


</dt> <dd>

Autorizzazione per la modifica dei parametri di connessione.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ RESET** (64)


</dt> <dd>

Autorizzazione per reimpostare o terminare una sessione o una connessione.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ DIRITTI \| STANDARD \_ VIRTUALI \_ NECESSARI** (983048)


</dt> <dd>

Autorizzazione per l'uso di canali virtuali. I canali virtuali forniscono l'accesso da un programma server ai dispositivi client.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ SHADOW** (16)


</dt> <dd>

Autorizzazione per lo shadow o il controllo remoto della sessione di un altro utente.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ LOGON** (32)


</dt> <dd>

Autorizzazione per accedere a una sessione nel server.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ LOGOFF** (4)


</dt> <dd>

Autorizzazione per disconnettere un utente da una sessione.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MSG** (128)


</dt> <dd>

Autorizzazione per inviare un messaggio a una sessione di un altro utente.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ CONNECT** (256)


</dt> <dd>

Autorizzazione per la connessione a un'altra sessione.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ DISCONNECT** (512)


</dt> <dd>

Autorizzazione per disconnettere una sessione.

</dd> </dl>

</dd> <dt>

**Autorizzazioni negate**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le autorizzazioni specifiche del server Host sessione Desktop remoto non consentite per l'account. Il valore di questa proprietà è una maschera di bit, che può essere impostata su uno o più valori della **proprietà PermissionsAllowed.**

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

**WINSTATION \_ QUERY=0x1** (0)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

**WINSTATION \_ SET=0x2** (1)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

**WINSTATION \_ LOGOFF=0x4** (2)


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

**WINSTATION \_ VIRTUAL \| STANDARD RIGHTS REQUIRED = \_ \_ 0xF008** (3)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

**WINSTATION \_ SHADOW=0x10** (4)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

**WINSTATION \_ LOGON=0x20** (5)


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

**WINSTATION \_ MSG=0x80** (6)


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

**WINSTATION \_ CONNECT=0x100** (7)


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

**WINSTATION \_ DISCONNECT=0x200** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica gli [ID di sicurezza dell'account.](/windows/desktop/SecAuthZ/security-identifiers)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati nonoperational includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono in linea, ma l'elemento gestito non è né "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Danneggiato")


</dt> <dd></dd> <dt>



 ("Sconosciuto")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Starting")


</dt> <dd></dd> <dt>



 ("Arresto")


</dt> <dd></dd> <dt>



 ("Servizio")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del terminale.

Questa proprietà viene ereditata da [**\_ TerminalSetting Win32.**](win32-terminalsetting.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Per connettersi allo spazio \\ dei \\ nomi CIMV2 \\ TerminalServices radice, il livello di autenticazione deve includere la privacy dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione di **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valore di 6. Nell'esempio Visual Basic Scripting Edition (VBScript) seguente viene illustrato come connettersi a un computer remoto con privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> </dl>

 

