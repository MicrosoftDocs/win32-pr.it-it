---
description: Registro di sistema Win32 \_&\# 8194; La classe WMI rappresenta il Registro di sistema in un computer che esegue Windows.
ms.assetid: 4a6cd7d7-2845-434d-b024-d6dbb77371ea
ms.tgt_platform: multiple
title: Win32_Registry classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Registry
- Win32_Registry.Caption
- Win32_Registry.Description
- Win32_Registry.InstallDate
- Win32_Registry.Status
- Win32_Registry.CurrentSize
- Win32_Registry.MaximumSize
- Win32_Registry.Name
- Win32_Registry.ProposedSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 64611f35e08d9b816d990602b43c62330431e8afb65874cee284fac5778a898d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971576"
---
# <a name="win32_registry-class"></a>Classe Registry \_ Win32

La classe  [WMI](../wmisdk/retrieving-a-class.md) Registro di sistema **Win32 \_** rappresenta il Registro di sistema in un computer che esegue Windows.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Registry : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   CurrentSize;
  uint32   MaximumSize;
  string   Name;
  uint32   ProposedSize;
};
```

## <a name="members"></a>Members

La **classe \_ Registro di sistema Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Registro di sistema Win32** ha queste proprietà.

<dl> <dt>

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

**CurrentSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemRegistryQuotaInformation"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Dimensioni fisiche correnti del Registro Windows sistema.

Esempio: 10

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

**MaximumSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Dimensioni massime del registro Windows dati. Se il sistema usa correttamente la **proprietà ProposedSize,** **MaximumSize** deve contenere lo stesso valore.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")
</dt> </dl>

Nome del registro Windows dati. La lunghezza massima è 256 caratteri.

</dd> <dt>

**ProposedSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Dimensioni proposte del registro Windows dati. È l'unica impostazione del Registro di sistema che può essere modificata e la proposta viene tentata al successivo avvio del sistema.

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

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ Registry di Win32** è derivata da [**CIM \_ LogicalElement.**](cim-logicalelement.md)

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

 

 
