---
description: La \_ classe della condivisione Win32 rappresenta una risorsa condivisa in un sistema di computer che esegue Windows. Potrebbe trattarsi di un'unità disco, di una stampante, di una comunicazione interprocesso o di un altro dispositivo condivisibile. Per ulteriori informazioni sul recupero delle classi WMI, vedere Recupero di una classe.
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127319"
---
# <a name="win32_share-class"></a>\_Classe condivisione Win32

La classe della **\_ condivisione Win32** rappresenta una risorsa condivisa in un sistema di computer che esegue Windows. Potrebbe trattarsi di un'unità disco, di una stampante, di una comunicazione interprocesso o di un altro dispositivo condivisibile. Per ulteriori informazioni sul recupero delle classi WMI, vedere [recupero di una classe](../wmisdk/retrieving-a-class.md).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
};
```

## <a name="members"></a>Members

La classe della **\_ condivisione Win32** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe della **\_ condivisione Win32** presenta questi metodi.



| Metodo                                                             | Descrizione                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Creare**](create-method-in-class-win32-share.md)               | Metodo della classe che avvia la condivisione per una risorsa server.<br/>                                                                                                                                               |
| [**Delete**](delete-method-in-class-win32-share.md)               | Metodo della classe che elimina un nome di condivisione dall'elenco di risorse condivise di un server, disconnettendo le connessioni alla risorsa condivisa.<br/>                                                                       |
| [**GetAccessMask**](getaccessmask-method-in-class-win32-share.md) | Restituisce i diritti di accesso alla condivisione utilizzata dall'utente o dal gruppo per conto del quale viene restituita l'istanza. È consigliabile usare questo metodo al posto della proprietà **accessMask** , che è sempre **null**.<br/> |
| [**SetShareInfo**](setshareinfo-method-in-class-win32-share.md)   | Metodo della classe che imposta i parametri di una risorsa condivisa.<br/>                                                                                                                                              |



 

### <a name="properties"></a>Proprietà

La classe della **\_ condivisione Win32** dispone di queste proprietà.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Questa proprietà è obsoleta e non viene più utilizzata. Usare invece il metodo [**Win32 \_ share. GetAccessMask**](getaccessmask-method-in-class-win32-share.md) . Il valore della proprietà **accessMask** è impostato su **null** da WMI. Per ulteriori informazioni sull'impostazione dell'accesso quando viene creata una condivisione, vedere il metodo [**create**](create-method-in-class-win32-share.md) .

</dd> <dt>

**AllowMaximum**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ USA")
</dt> </dl>

Il numero di utenti simultanei per questa risorsa è stato limitato. Se **true**, il valore nella proprietà **MaximumAllowed** viene ignorato.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
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

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")
</dt> </dl>

Indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**MaximumAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ USA")
</dt> </dl>

Limite per il numero massimo di utenti che possono usare questa risorsa contemporaneamente. Il valore è valido solo se la proprietà **AllowMaximum** è impostata su **false**.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ info \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")
</dt> </dl>

Alias assegnato a un percorso configurato come una condivisione in un computer in cui è in esecuzione Windows.

Esempio di Windows 2008: " \\ Server01 \\ public"-per windows Server 2008 è necessario inserire l'UNC nel nome.

</dd> <dt>

**Percorso**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**share \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")
</dt> </dl>

Percorso locale della condivisione di Windows.

Esempio: "C: \\ Program Files"

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
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

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**Condividi \_ informazioni \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| \_ tipo shi502")
</dt> </dl>

Tipo di risorsa condivisa. I tipi includono le unità disco, le code di stampa, le comunicazioni interprocesso (IPC) e i dispositivi generali.

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Unità disco** (0)


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**Coda di stampa** (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Dispositivo** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Amministrazione unità disco** (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Amministrazione coda di stampa** (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Amministratore del dispositivo** (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**Amministratore IPC** (2147483651)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe della **\_ condivisione Win32** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).

Il metodo create in questa classe è un metodo statico. I metodi **Delete**, **GetAccessMask** e **SetShareInfo** sono tutti metodi di istanza.

A seconda delle autorizzazioni di sicurezza, potrebbe non essere possibile recuperare tutte le proprietà di questa classe. Ad esempio, le proprietà **AllowMaximum**, **MaximumAllowed**, **path** e **Type** possono restituire null. In generale, gli utenti avanzati e gli amministratori potranno recuperare tutti i valori delle proprietà.

## <a name="examples"></a>Esempio

Il seguente esempio di[codice](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) di script Center elenca tutte le condivisioni in un computer ed elenca tutte le autorizzazioni di condivisione per ogni condivisione.

L'esempio [Get Share Information simile a Win32 \_ share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell esegue una query su condivisione Win32 \_ e fornisce i risultati.

Nell'esempio di PowerShell seguente vengono visualizzate le condivisioni nel sistema locale.


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



In alternativa, se si vuole filtrare più precisamente, è possibile usare il frammento di codice di PowerShell seguente:


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



Nell'esempio VBScript seguente vengono visualizzate le condivisioni nel sistema locale.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
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

[**\_LogicalElement CIM**](cim-logicalelement.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Attività WMI: file e cartelle](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 
