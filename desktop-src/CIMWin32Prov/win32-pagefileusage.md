---
description: PageFileUsage Win32 \_&\# 8194; La classe WMI rappresenta il file utilizzato per la gestione dello scambio di file di memoria virtuale in un sistema Win32. Le informazioni contenute negli oggetti di cui è stata creata un'istanza da questa classe specificano lo stato di esecuzione del file di pagina.
ms.assetid: 635d7bd0-3738-4092-8b76-5e9583e079a9
ms.tgt_platform: multiple
title: Win32_PageFileUsage classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileUsage
- Win32_PageFileUsage.Caption
- Win32_PageFileUsage.Description
- Win32_PageFileUsage.InstallDate
- Win32_PageFileUsage.Status
- Win32_PageFileUsage.AllocatedBaseSize
- Win32_PageFileUsage.CurrentUsage
- Win32_PageFileUsage.Name
- Win32_PageFileUsage.PeakUsage
- Win32_PageFileUsage.TempPageFile
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d5d901c771fb71dbda141f6166348d1601317eae7bcda3ea5a059f5836975014
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972271"
---
# <a name="win32_pagefileusage-class"></a>Classe \_ PageFileUsage Win32

La classe  [WMI](../wmisdk/retrieving-a-class.md) **\_ PageFileUsage win32** rappresenta il file utilizzato per la gestione dello scambio di file di memoria virtuale in un sistema Win32. Le informazioni contenute negli oggetti di cui è stata creata un'istanza da questa classe specificano lo stato di esecuzione del file di pagina.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{9B3AC16A-EEE5-11d2-B13B-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileUsage : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AllocatedBaseSize;
  uint32   CurrentUsage;
  string   Name;
  uint32   PeakUsage;
  boolean  TempPageFile;
};
```

## <a name="members"></a>Members

La **classe \_ PageFileUsage win32** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ PageFileUsage win32** ha queste proprietà.

<dl> <dt>

**AllocatedBaseSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")
</dt> </dl>

Quantità effettiva di spazio su disco allocato per l'uso con questo file di pagine. Questo valore corrisponde all'intervallo stabilito in [**\_ PageFileSetting Win32**](win32-pagefilesetting.md) nelle **proprietà InitialSize** **e MaximumSize,** impostato all'avvio del sistema.

Esempio: 178

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

**CurrentUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")
</dt> </dl>

Quantità di spazio su disco attualmente utilizzata dal file di pagina.

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

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Nome del file di pagina.

Esempio: "C: \\PAGEFILE.SYS"

</dd> <dt>

**PeakUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")
</dt> </dl>

File di pagina di uso più elevato.

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

**TempPageFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control Session Manager Memory \\ \\ \\ \\ Management \| TempPageFile")
</dt> </dl>

Se **true,** è stato creato un file di pagine temporaneo, in genere perché non esiste alcun file di pagina permanente nel computer corrente.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ PageFileUsage Win32** è derivata da [**CIM \_ LogicalElement.**](cim-logicalelement.md)

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

 

 
