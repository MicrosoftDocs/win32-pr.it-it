---
description: Rappresenta i dati relativi a un account di gruppo.
ms.assetid: a53d1276-3dc9-419a-bbb8-5dd07794a971
ms.tgt_platform: multiple
title: Classe Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group
- Win32_Group.Caption
- Win32_Group.Description
- Win32_Group.InstallDate
- Win32_Group.Status
- Win32_Group.LocalAccount
- Win32_Group.SID
- Win32_Group.SIDType
- Win32_Group.Domain
- Win32_Group.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8849ba149e0de570150682d3afbad3a4ee33f36
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127330"
---
# <a name="win32_group-class"></a>\_Classe gruppo Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) del **\_ gruppo Win32** rappresenta i dati relativi a un account di gruppo. Un account di gruppo consente la modifica dei privilegi di accesso per un elenco di utenti. Esempio: Marketing2.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Group : Win32_Account
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  LocalAccount;
  string   SID;
  uint8    SIDType;
  string   Domain;
  string   Name;
};
```

## <a name="members"></a>Members

La classe del **\_ gruppo Win32** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe del **\_ gruppo Win32** presenta questi metodi.



| Metodo                                               | Descrizione                        |
|:-----------------------------------------------------|:-----------------------------------|
| [**Rinominare**](rename-method-in-class-win32-group.md) | Modifica il nome del gruppo.<br/> |



 

### <a name="properties"></a>Proprietà

La classe del **\_ gruppo Win32** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Dominio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Functions \| NomeDominio")
</dt> </dl>

Nome del dominio Windows a cui appartiene l'account di gruppo.

Esempio: "NA-SALES"

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")
</dt> </dl>

Indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LocalAccount**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Se **true**, l'account viene definito nel computer locale. Per recuperare solo gli account definiti nel computer locale, progettare una query che includa la condizione "LocalAccount =**true**".

Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| Name")
</dt> </dl>

Nome dell'account di gruppo di Windows nel dominio specificato dalla proprietà del **dominio** di questa classe.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Security Identifier (SID)")
</dt> </dl>

ID di sicurezza (SID) per l'account. Un SID è un valore stringa di lunghezza variabile usato per identificare un trustee. Ogni account dispone di un SID univoco emesso da un'autorità, ad esempio un dominio di Windows, archiviato in un database di sicurezza. Quando un utente esegue l'accesso, il sistema Recupera il SID dell'utente dal database e lo inserisce nel token di accesso dell'utente. Il sistema usa il SID nel token di accesso dell'utente per identificare l'utente in tutte le interazioni successive con la sicurezza di Windows. Quando un SID è stato usato come identificatore univoco per un utente o un gruppo, non può essere usato di nuovo per identificare un altro utente o gruppo.

Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).

</dd> <dt>

**SIDType**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API di \| controllo di accesso tipi di enumerazione \| SID \_ nome \_ utilizzo")
</dt> </dl>

Valori enumerati che specificano il tipo di ID di sicurezza (SID).

Questa proprietà viene ereditata [**dall' \_ account Win32**](win32-account.md).

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

**SidTypeUser** (1)


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

**SidTypeGroup** (2)


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

**SidTypeDomain** (3)


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

**SidTypeAlias** (4)


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

**SidTypeWellKnownGroup** (5)


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

**SidTypeDeletedAccount** (6)


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

**SidTypeInvalid** (7)


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

**SidTypeUnknown** (8)


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

**SidTypeComputer** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Stringa che indica lo stato corrente dell'oggetto. È possibile definire lo stato operativo e non operativo. Lo stato operativo può includere "OK", "danneggiato" e "errore predazione". "Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.

Lo stato non operativo può includere "Error", "starting", "stoping" e "Service". Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Ridotto **("danneggiato"** )


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Errore di predazione** ("Predator fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** di ("avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** in corso ("arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sottolineato** (sottolineato)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Noncover** ("noncover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicazione persa** ("comunicazione persa")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe del **\_ gruppo Win32** è derivata [**dall' \_ account Win32**](win32-account.md).

## <a name="examples"></a>Esempio

Il codice seguente, tratto dall' [elenco dei gruppi locali utilizzando](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) l'esempio di codice VBScript WMI nella raccolta TechNet, utilizza il **\_ gruppo Win32** per restituire informazioni sui gruppi locali presenti in un computer.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_Group  Where LocalAccount = True") 
 
For Each objItem in colItems 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Domain: " & objItem.Domain 
    Wscript.Echo "Local Account: " & objItem.LocalAccount 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "SID: " & objItem.SID 
    Wscript.Echo "SID Type: " & objItem.SIDType 
    Wscript.Echo "Status: " & objItem.Status 
    Wscript.Echo 
Next 
```



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

[**\_Account Win32**](win32-account.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

