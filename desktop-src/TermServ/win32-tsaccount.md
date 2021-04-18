---
title: Classe Win32_TSAccount
description: Consente l'eliminazione di un account esistente nel terminale Win32 \_ e la modifica delle autorizzazioni esistenti.
ms.assetid: fd4d8a0f-685b-4619-84f1-faefbabd04ba
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSAccount Servizi Desktop remoto
- Classe Win32_TSAccount Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 10fed32943cf89728081e2443dfffe2e3762298d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302432"
---
# <a name="win32_tsaccount-class"></a>Win32 \_ TSAccount (classe)

La classe WMI **Win32 \_ TSAccount** consente l'eliminazione di un account esistente nel [**\_ terminale Win32**](win32-terminal.md) e la modifica delle autorizzazioni esistenti.

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

La classe **Win32 \_ TSAccount** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSAccount** presenta questi metodi.



| Metodo                                                                   | Descrizione                                                                                  |
|:-------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Eliminare**](win32-tsaccount-delete.md)                                 | Elimina l'account utente, gruppo o computer specificato.<br/>                           |
| [**ModifyAuditPermissions**](win32-tsaccount-modifyauditpermissions.md) | Modifica la granularità del set di autorizzazioni di controllo dell'account specificato.<br/> |
| [**ModifyPermissions**](win32-tsaccount-modifypermissions.md)           | Imposta un set di autorizzazioni più granulare per l'account specificato.<br/>                     |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSAccount** dispone di queste proprietà.

<dl> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome corrente dell'account. Il nome di dominio è incluso.

</dd> <dt>

**AuditFail**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le [autorizzazioni di host sessione Desktop remoto Services](terminal-services-permissions.md) controllate per una condizione di errore. Il valore di questa proprietà è una maschera di maschera, che può essere impostata su uno o più valori della proprietà **PermissionsAllowed** .

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

**WINSTATION \_ QUERY = 0x1** (0)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

**WINSTATION \_ SET = 0x2** (1)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

**WINSTATION \_ Disconnessione = 0x4** (2)


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

**WINSTATION \_ \| Diritti standard \_ virtuali \_ richiesti = 0xF008** (3)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

**WINSTATION \_ SHADOW = 0x10** (4)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

**WINSTATION \_ LOGON = 0x20** (5)


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

**WINSTATION \_ MESSAGGIO = 0x80** (6)


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

**WINSTATION \_ Connetti = 0x100** (7)


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

**WINSTATION \_ Disconnect = 0x200** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**AuditSuccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le autorizzazioni specifiche per il server Host sessione Desktop remoto controllate per una condizione di esito positivo. Il valore di questa proprietà è una maschera di maschera, che può essere impostata su uno o più valori della proprietà **PermissionsAllowed** .

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

**WINSTATION \_ QUERY = 0x1** (0)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

**WINSTATION \_ SET = 0x2** (1)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_logoff_0x4winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_LOGOFF_0X4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

**WINSTATION \_ Disconnessione = 0x4WINSTATION \_ virtual \| standard \_ Rights \_ required = 0xF008** (2)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

**WINSTATION \_ SHADOW = 0x10** (3)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

**WINSTATION \_ LOGON = 0x20** (4)


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

**WINSTATION \_ MESSAGGIO = 0x80** (5)


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

**WINSTATION \_ Connetti = 0x100** (6)


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

**WINSTATION \_ Disconnect = 0x200** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione (stringa a una riga) dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Data di installazione dell'oggetto. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PermissionsAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le [autorizzazioni servizi desktop remoto](terminal-services-permissions.md) consentite per l'account. Il valore di questa proprietà è una maschera di maschera, che può essere impostata su uno o più dei valori seguenti.

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION \_ QUERY = 0x1** (1)


</dt> <dd>

Autorizzazione per eseguire query sulle informazioni relative a una sessione.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ IMPOSTA** (2)


</dt> <dd>

Autorizzazione per la modifica dei parametri di connessione.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ Reimposta** (64)


</dt> <dd>

Autorizzazione per reimpostare o terminare una sessione o una connessione.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ \| Diritti standard \_ virtuali \_ richiesti** (983048)


</dt> <dd>

Autorizzazione per l'utilizzo di canali virtuali. I canali virtuali forniscono l'accesso da un programma server ai dispositivi client.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ OMBREGGIAtura** (16)


</dt> <dd>

Autorizzazione per nascondere o controllare in modalità remota la sessione di un altro utente.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ ACCESSO** (32)


</dt> <dd>

Autorizzazione per accedere a una sessione nel server.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ Disconnessione** (4)


</dt> <dd>

Autorizzazione per disconnettere un utente da una sessione.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MESSAGGIO** (128)


</dt> <dd>

Autorizzazione per l'invio di un messaggio alla sessione di un altro utente.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ Connetti** (256)


</dt> <dd>

Autorizzazione per la connessione a un'altra sessione.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ Disconnetti** (512)


</dt> <dd>

Autorizzazione per disconnettere una sessione.

</dd> </dl>

</dd> <dt>

**PermissionsDenied**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le autorizzazioni specifiche per il server Host sessione Desktop remoto non consentite per l'account. Il valore di questa proprietà è una maschera di maschera, che può essere impostata su uno o più valori della proprietà **PermissionsAllowed** .

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

**WINSTATION \_ QUERY = 0x1** (0)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

**WINSTATION \_ SET = 0x2** (1)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

**WINSTATION \_ Disconnessione = 0x4** (2)


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

**WINSTATION \_ \| Diritti standard \_ virtuali \_ richiesti = 0xF008** (3)


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

**WINSTATION \_ SHADOW = 0x10** (4)


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

**WINSTATION \_ LOGON = 0x20** (5)


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

**WINSTATION \_ MESSAGGIO = 0x80** (6)


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

**WINSTATION \_ Connetti = 0x100** (7)


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

**WINSTATION \_ Disconnect = 0x200** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica gli [ID di sicurezza](/windows/desktop/SecAuthZ/security-identifiers) dell'account.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire diversi stati operativi e non operativi. Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro). Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service". Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Errore")


</dt> <dd></dd> <dt>



 ("Danneggiato")


</dt> <dd></dd> <dt>



 ("Sconosciuto")


</dt> <dd></dd> <dt>



 ("Errore di predazione")


</dt> <dd></dd> <dt>



 ("Avvio")


</dt> <dd></dd> <dt>



 ("Arresto")


</dt> <dd></dd> <dt>



 ("Servizio")


</dt> <dd></dd> </dl>

</dd> <dt>

**Terminale**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del terminale.

Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6. Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> </dl>

 

