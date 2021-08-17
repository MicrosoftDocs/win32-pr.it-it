---
description: La classe ClusterShare Win32 \_ rappresenta una risorsa condivisa in un cluster.
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Win32_ClusterShare classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare
- Win32_ClusterShare.Caption
- Win32_ClusterShare.Description
- Win32_ClusterShare.InstallDate
- Win32_ClusterShare.Status
- Win32_ClusterShare.AccessMask
- Win32_ClusterShare.AllowMaximum
- Win32_ClusterShare.MaximumAllowed
- Win32_ClusterShare.Name
- Win32_ClusterShare.Path
- Win32_ClusterShare.Type
- Win32_ClusterShare.ServerName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 66be06bf3a8433a7dba1eb28e6123adb03d622803745838158aa80bda0e8e594
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417992"
---
# <a name="win32_clustershare-class"></a>Classe ClusterShare Win32 \_

\[La **classe \_ ClusterShare Win32** è deprecata. Usare invece le [**classi MSFT \_ FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) e [**\_ MSFT SMFileShare.**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare)\]

La classe ClusterShare Win32 \_ rappresenta una risorsa condivisa in un cluster.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_ClusterShare : Win32_Share
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
  string   ServerName;
};
```

## <a name="members"></a>Members

La **classe \_ ClusterShare Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ ClusterShare Win32** include questi metodi.



| Metodo                                                    | Descrizione                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [**Creare**](create-win32-clustershare.md)               | Crea una nuova **istanza di \_ ClusterShare Win32.**<br/>       |
| [**Elimina**](delete-win32-clustershare.md)               | Elimina **un'istanza di \_ ClusterShare Win32.**<br/>           |
| [**GetAccessMask**](getaccessmask-win32-clustershare.md) | Restituisce una bitmap con i diritti di accesso alla condivisione.<br/> |
| [**SetShareInfo**](setshareinfo-win32-clustershare.md)   | Imposta i parametri della risorsa condivisa.<br/>           |



 

### <a name="properties"></a>Proprietà

La **classe \_ ClusterShare Win32** ha queste proprietà.

<dl> <dt>

**Accessmask**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **DEPRECATO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Questa proprietà è obsoleta e non viene più usata. Usare invece [**il metodo Win32 \_ Share.GetAccessMask.**](getaccessmask-method-in-class-win32-share.md) Il valore della **proprietà AccessMask** è impostato su **Null** da WMI. Per altre informazioni sull'impostazione dell'accesso quando viene creata una condivisione, vedere il [**metodo Create.**](create-method-in-class-win32-share.md)

Questa proprietà viene ereditata da [**Win32 \_ Share.**](win32-share.md)

</dd> <dt>

**AllowMaximum**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ uses")
</dt> </dl>

Il numero di utenti simultanei per questa risorsa è stato limitato. Se **True,** il valore nella **proprietà MaximumAllowed** viene ignorato.

Questa proprietà viene ereditata da [**Win32 \_ Share.**](win32-share.md)

</dd> <dt>

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

**MaximumAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ max \_ uses")
</dt> </dl>

Limite al numero massimo di utenti autorizzati a usare questa risorsa contemporaneamente. Il valore è valido solo se la **proprietà AllowMaximum** è impostata su **FALSE.**

Questa proprietà viene ereditata da [**Win32 \_ Share.**](win32-share.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ netname")
</dt> </dl>

Alias assegnato a un percorso configurato come condivisione in un computer che esegue Windows.

Windows 2008: \\ "SERVER01 \\ public" - Windows Server 2008 richiede di inserire il nome UNC.

Questa proprietà viene ereditata da [**Win32 \_ Share.**](win32-share.md)

</dd> <dt>

**Percorso**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")
</dt> </dl>

Percorso locale della condivisione Windows locale.

Esempio: "C: \\ Programmi"

Questa proprietà viene ereditata da [**Win32 \_ Share.**](win32-share.md)

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| shi503 \_ servername")
</dt> </dl>

Server del cluster in cui è ospitata la condivisione.

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

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SHARE INFO \| [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ type")
</dt> </dl>

Tipo di risorsa condivisa. I tipi includono: unità disco, code di stampa, comunicazioni interprocesso (IPC) e dispositivi generali.

Questa proprietà viene ereditata da [**Win32 \_ Share.**](win32-share.md)

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Unità disco** (0)


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**Coda di** stampa (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Dispositivo** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Amministratore unità disco** (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Amministratore coda di** stampa (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Amministratore del** dispositivo (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**Amministratore IPC** (2147483651)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Condivisione \_ Win32**](win32-share.md)
</dt> </dl>

 

