---
description: Rappresenta un'impostazione dell'ambiente o dell'ambiente di sistema in un Windows computer.
ms.assetid: da7ee891-c759-4046-a9d8-d3caf66ab5a9
ms.tgt_platform: multiple
title: Win32_Environment classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Environment
- Win32_Environment.Caption
- Win32_Environment.Description
- Win32_Environment.InstallDate
- Win32_Environment.Status
- Win32_Environment.Name
- Win32_Environment.SystemVariable
- Win32_Environment.UserName
- Win32_Environment.VariableValue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 18a85af664a4be8ef96b1882477e2fadec0f0b1a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882274"
---
# <a name="win32_environment-class"></a>Classe Ambiente Win32 \_

La **classe \_ WMI Ambiente Win32** rappresenta un ambiente o un'impostazione dell'ambiente di sistema in un Windows computer. [](/windows/desktop/WmiSdk/retrieving-a-class) L'esecuzione di query su questa classe restituisce le variabili di ambiente disponibili in:

**HKEY \_ Ambiente \_** \\  \\ sessionmanager **del controllo CurrentControlSet** \\  \\ **del sistema** \\  LOCAL MACHINE

e

**HKEY \_ Utenti** \\ **< *-* >** \\ **Ambiente utente**

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4D2-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_Environment : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  boolean  SystemVariable;
  string   UserName;
  string   VariableValue;
};
```

## <a name="members"></a>Members

La **classe \_ Ambiente Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Ambiente Win32** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto .

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto .

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")
</dt> </dl>

Indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet Control Session Manager \\ \\ \\ \\ \\ \\ Environment")
</dt> </dl>

Stringa di caratteri che specifica il nome di una variabile Windows di ambiente basata su criteri. Specificando il nome di una variabile che non esiste ancora, un'applicazione crea una nuova variabile di ambiente.

Esempio: "Path"

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Stringa che indica lo stato corrente dell'oggetto . È possibile definire lo stato operativo e non operativo. Lo stato operativo può includere "OK", "Degraded" e "Pred Fail". "Pred Fail" indica che un elemento funziona correttamente, ma sta stimando un errore (ad esempio, un disco rigido abilitato per SMART).

Lo stato non operativo può includere "Error", "Starting", "Stopping" e "Service". "Servizio" può essere applicato durante il ridimensionamento del mirror del disco, il ricaricamento di un elenco di autorizzazioni utente o altre operazioni amministrative. Non tutte queste operazioni sono online, ma l'elemento gestito non è né "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradato** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** ("Avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** ("Arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("Servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("Nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemVariable**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control Session Manager \\ \\ \\ \\ Environment")
</dt> </dl>

Indica se la variabile è una variabile di sistema. Una variabile di sistema viene impostata dal sistema operativo ed è indipendente dalle impostazioni dell'ambiente utente.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet Control Session Manager \\ \\ \\ \\ \\ \\ Environment")
</dt> </dl>

Nome del proprietario dell'impostazione dell'ambiente. È impostato su SYSTEM per le impostazioni specifiche del sistema basato su Windows (anziché su un utente specifico) e su DEFAULT per le &lt; &gt; impostazioni utente &lt; &gt; predefinite.

Esempio: "JSmith"

</dd> <dt>

**Variablevalue**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control Session Manager \\ \\ \\ \\ Environment")
</dt> </dl>

Variabile segnaposto di una Windows di ambiente basata su valori. Informazioni come la file system directory possono cambiare da computer a computer. Il sistema operativo sostituisce i segnaposto.

Esempio: "%SystemRoot%"

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ Environment Win32** è derivata da [**CIM \_ SystemResource**](cim-systemresource.md). È possibile usare questa classe per trovare i percorsi di cartelle speciali, ad esempio la cartella Di sistema o i file di programma in un computer remoto. Alcuni esempi sono: windir, systemroot, programfiles e userprofile. **Win32 \_ L'ambiente** restituisce fondamentalmente ciò che è possibile trovare in:

**HKEY \_ Ambiente \_** \\  \\ sessionmanager **del controllo CurrentControlSet** \\  \\ **del sistema** \\  LOCAL MACHINE

e

**HKEY \_ Utenti** \\ **< *-* >** \\ **Ambiente utente**

Il processo chiamante che usa questa classe deve **disporre del edizione Standard RESTORE \_ \_ NAME** nel computer in cui si trova il Registro di sistema. Ad esempio, se si enumera questa classe nel computer locale, l'account con cui viene eseguita l'applicazione deve avere questo privilegio. Per altre informazioni, vedere [Esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Esempio

[L'esempio List Environment Variables on a Computer](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl usa WMI per restituire informazioni su tutte le variabili di ambiente in un computer.

Nell'esempio di codice VBScript seguente vengono enumerate le variabili di ambiente nel computer locale.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colVar = objWMIService.ExecQuery("Select * from Win32_Environment")
For Each objVar in colVar
    Wscript.Echo "Description: " & objVar.Description & VBNewLine _
               & "Name: " & objVar.Name & VBNewLine _
               & "System Variable: " & objVar.SystemVariable & VBNewLine _
               & "User Name: " & objVar.UserName & VBNewLine _
               & "Variable Value: " & objVar.VariableValue 
Next
```



Nell'esempio di codice VBScript seguente viene modificata una variabile di ambiente denominata BUILD \_ TYPE in un input di valore da parte dell'utente. Lo script presuppone che la variabile BUILD \_ TYPE esista già. Se non esiste, lo script termina. Il valore di input viene controllato: deve essere "Build1", "Build2" o "Build3" e non vengono accettati altri valori. La funzione [VBScript UCase](https://msdn.microsoft.com/library/aa902519.aspx) rende l'input senza distinzione tra maiuscole e minuscole. Se ciò che viene digitato non è uno dei tre valori accettabili, lo script termina.


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_Environment")
Found = False
For Each objItem in colItems
    If objItem.Name = "BUILD_TYPE" Then
    Found = True
    Change = UCase(InputBox("BUILD_TYPE currently = " & objItem.VariableValue & VBNewLine _
                          & "Change options are Build1, Build2, Build3 "))
        If UCase(Change) = "BUILD1" OR Change = "BUILD2" OR Change = "BUILD3" Then
            objItem.VariableValue = Change
            objItem.Put_
        WScript.Echo "BUILD_TYPE changed to " & objItem.VariableValue
        Else 
        WScript.Echo "No input or unacceptable input." & " No change to BUILD_TYPE"
        End If
    End If
Next
If Found = False Then
    WScript.Echo "User-defined environment variable BUILD_TYPE not found."
End If
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SystemResource**](cim-systemresource.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

