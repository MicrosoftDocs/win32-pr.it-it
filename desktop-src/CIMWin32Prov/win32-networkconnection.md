---
description: Rappresenta una connessione di rete attiva in un Windows basato su rete.
ms.assetid: e16e5f13-ea28-4d75-9978-4ff2ef5e5506
ms.tgt_platform: multiple
title: Win32_NetworkConnection classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkConnection
- Win32_NetworkConnection.Caption
- Win32_NetworkConnection.Description
- Win32_NetworkConnection.InstallDate
- Win32_NetworkConnection.Status
- Win32_NetworkConnection.AccessMask
- Win32_NetworkConnection.Comment
- Win32_NetworkConnection.ConnectionState
- Win32_NetworkConnection.ConnectionType
- Win32_NetworkConnection.DisplayType
- Win32_NetworkConnection.LocalName
- Win32_NetworkConnection.Name
- Win32_NetworkConnection.Persistent
- Win32_NetworkConnection.ProviderName
- Win32_NetworkConnection.RemoteName
- Win32_NetworkConnection.RemotePath
- Win32_NetworkConnection.ResourceType
- Win32_NetworkConnection.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b4a8c712e8eb373730d24841133264e312694d79b593e83e89a1fc7387e7a77a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972631"
---
# <a name="win32_networkconnection-class"></a>Classe NetworkConnection Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) **\_ Win32 NetworkConnection** rappresenta una connessione di rete attiva in un Windows basato su rete.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkConnection : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  string   Comment;
  string   ConnectionState;
  string   ConnectionType;
  string   DisplayType;
  string   LocalName;
  string   Name;
  boolean  Persistent;
  string   ProviderName;
  string   RemoteName;
  string   RemotePath;
  string   ResourceType;
  string   UserName;
};
```

## <a name="members"></a>Members

La **classe \_ NetworkConnection Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ NetworkConnection Win32** ha queste proprietà.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Elenco dei diritti di accesso per il file o la directory specificata in cui l'utente o il gruppo ha la proprietà per conto del quale viene restituita l'istanza. Nei volumi FAT viene invece restituito il valore **FULL \_ ACCESS,** che indica che non è stata impostata alcuna sicurezza per l'oggetto.

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE \_ READ \_ DATA (file) o FILE \_ LIST DIRECTORY \_ (directory)** (1)


</dt> <dd>

Concede il diritto di leggere i dati dal file. Per una directory, questo valore concede il diritto di elencare il contenuto della directory.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE \_ WRITE \_ DATA (file) o FILE \_ ADD FILE \_ (directory)** (2)


</dt> <dd>

Concede il diritto di scrivere dati nel file. Per una directory, questo valore concede il diritto di creare un file nella directory.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE \_ APPEND \_ DATA (file) o FILE \_ ADD \_ SUBDIRECTORY** (4)


</dt> <dd>

Concede il diritto di aggiungere dati al file. Per una directory, questo valore concede il diritto di creare una sottodirectory.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE \_ READ \_ EA** (8)


</dt> <dd>

Concede il diritto di leggere gli attributi estesi.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE \_ WRITE \_ EA** (16)


</dt> <dd>

Concede il diritto di scrivere attributi estesi.

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE \_ EXECUTE (file) o FILE \_ TRAVERSE (directory)** (32)


</dt> <dd>

Concede il diritto di eseguire un file. Per una directory, la directory può essere attraversata.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE \_ DELETE \_ CHILD (directory)** (64)


</dt> <dd>

Concede il diritto di eliminare una directory e tutti i file in essa contenuti (relativi elementi figlio), anche se i file sono di sola lettura.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE \_ ATTRIBUTI \_ DI** LETTURA (128)


</dt> <dd>

Concede il diritto di leggere gli attributi del file.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE \_ ATTRIBUTI \_ DI** SCRITTURA (256)


</dt> <dd>

Concede il diritto di modificare gli attributi del file.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)


</dt> <dd>

Concede l'accesso per l'eliminazione.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**READ \_ CONTROL** (131072)


</dt> <dd>

Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE \_ Applicazione livello** dati (262144)


</dt> <dd>

Concede l'accesso in scrittura all'elenco di controllo di accesso discrezionale (DACL).

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE \_ OWNER** (524288)


</dt> <dd>

Assegna il proprietario della scrittura.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)


</dt> <dd>

Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.

</dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Commento**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows strutture di rete \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| *lpComment*")
</dt> </dl>

Commento fornito dal provider di rete.

</dd> <dt>

**ConnectionState**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures USE INFO \| [**\_ \_ 1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1) \| **ui1 \_ status**")
</dt> </dl>

Stato corrente della connessione di rete.

<dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

**Connesso** ("Connesso")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Error")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Paused** ("Paused")


</dt> <dd></dd> <dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

**Disconnesso** ("Disconnesso")


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

**Connessione** ("Connessione")


</dt> <dd></dd> <dt>

<span id="Reconnecting"></span><span id="reconnecting"></span><span id="RECONNECTING"></span>

**Riconnessione** ("Riconnessione")


</dt> <dd></dd> </dl>

</dd> <dt>

**ConnectionType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows strutture di rete \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwScope**")
</dt> </dl>

Tipo di persistenza della connessione utilizzata per la connessione alla rete.

<dt>

<span id="Current_Connection"></span><span id="current_connection"></span><span id="CURRENT_CONNECTION"></span>

**Connessione corrente** ("Connessione corrente")


</dt> <dd></dd> <dt>

<span id="Persistent_Connection"></span><span id="persistent_connection"></span><span id="PERSISTENT_CONNECTION"></span>

**Connessione permanente** ("Connessione permanente")


</dt> <dd></dd> </dl>

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto .

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DisplayType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows strutture di rete \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwDisplayType**")
</dt> </dl>

L'oggetto di rete deve essere visualizzato in un'interfaccia utente di esplorazione di rete.

<dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>

**Dominio** ("Dominio")


</dt> <dd></dd> <dt>

<span id="Generic"></span><span id="generic"></span><span id="GENERIC"></span>

**Generico** ("Generico")


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

**Server** ("Server")


</dt> <dd></dd> <dt>

<span id="Share"></span><span id="share"></span><span id="SHARE"></span>

**Condivisione** ("Condividi")


</dt> <dd></dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")
</dt> </dl>

Indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Localname**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows strutture di rete \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpLocalName**")
</dt> </dl>

Nome locale del dispositivo di rete connesso.

Esempio: "c: \\ public"

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")
</dt> </dl>

Nome della connessione di rete corrente. È la combinazione dei valori in **RemoteName** e **LocalName**.

Esempio: " \\ \\ NTRELEASE (c: \\ public)"

</dd> <dt>

**Persistente**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Functions \| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")
</dt> </dl>

La connessione verrà riconnessa automaticamente dal sistema operativo all'accesso successivo.

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows strutture di rete \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpProvider**")
</dt> </dl>

Nome del provider proprietario della risorsa. Questa proprietà può essere **NULL se** il nome del provider è sconosciuto.

</dd> <dt>

**RemoteName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API Windows strutture di rete \| \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")
</dt> </dl>

Nome della risorsa di rete remota per una risorsa di rete. Per una connessione corrente o persistente, **RemoteName** contiene il nome di rete associato al nome del valore nella **proprietà LocalName.** Il nome in **RemoteName** deve seguire le convenzioni di denominazione del provider di rete.

Esempio: \\ \\ "NTRELEASE"

</dd> <dt>

**RemotePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API Windows strutture di rete \| \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")
</dt> </dl>

Percorso completo della risorsa di rete.

Esempio: " \\ \\ infosrv1 \\ public"

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows strutture di rete \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwType**")
</dt> </dl>

Tipo di risorsa a cui enumerare o connettersi.

<dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>

**Disco** ("Disco")


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

**Stampa** ("Stampa")


</dt> <dd></dd> <dt>

<span id="Any"></span><span id="any"></span><span id="ANY"></span>

**Qualsiasi** ("Qualsiasi")


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Stringa che indica lo stato corrente dell'oggetto . È possibile definire lo stato operativo e non operativo. Lo stato operativo può includere "OK", "Danneggiato" e "Pred Fail". "Pred Fail" indica che un elemento funziona correttamente, ma prevede un errore , ad esempio un'unità disco rigido abilitata per SMART.

Lo stato non operativo può includere "Error", "Starting", "Stopping" e "Service". Il "servizio" può essere applicato durante il ridimensionamento del mirror del disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono online, ma l'elemento gestito non è "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degraded** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


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

**UserName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Functions \| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")
</dt> </dl>

Nome utente o nome utente predefinito utilizzato per stabilire una connessione di rete.

Esempio: "SYSTEM"

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ NetworkConnection Win32** è derivata da [**CIM \_ LogicalElement.**](cim-logicalelement.md)

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente vengono recuperate informazioni sulla connessione di rete locale.


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\Root\CIMv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_NetworkConnection",,48)
For Each objItem in colItems
    Wscript.Echo "AccessMask: " & objItem.AccessMask
    Wscript.Echo "Caption: " & objItem.Caption
    Wscript.Echo "Comment: " & objItem.Comment
    Wscript.Echo "ConnectionState: " & objItem.ConnectionState
    Wscript.Echo "ConnectionType: " & objItem.ConnectionType
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "DisplayType: " & objItem.DisplayType
    Wscript.Echo "InstallDate: " & objItem.InstallDate
    Wscript.Echo "LocalName: " & objItem.LocalName
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Persistent: " & objItem.Persistent
    Wscript.Echo "ProviderName: " & objItem.ProviderName
    Wscript.Echo "RemoteName: " & objItem.RemoteName
    Wscript.Echo "RemotePath: " & objItem.RemotePath
    Wscript.Echo "ResourceType: " & objItem.ResourceType
    Wscript.Echo "Status: " & objItem.Status
    Wscript.Echo "UserName: " & objItem.UserName
Next
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

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
