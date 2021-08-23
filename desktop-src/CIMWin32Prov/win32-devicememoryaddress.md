---
description: La classe WMI Win32 DeviceMemoryAddress rappresenta un indirizzo di memoria del dispositivo \_ in un computer che esegue Windows.
ms.assetid: f0a70724-5ced-47fe-b17e-e153e65b80df
ms.tgt_platform: multiple
title: Win32_DeviceMemoryAddress classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d49baca4e11ce1908ba1d057819f216153f49353415c8b5465e70e3a607e00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020249"
---
# <a name="win32_devicememoryaddress-class"></a>Classe \_ DeviceMemoryAddress Win32

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ Win32 DeviceMemoryAddress** rappresenta un indirizzo di memoria del dispositivo in un computer che esegue Windows.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceMemoryAddress : Win32_SystemMemoryResource
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   MemoryType;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a>Members

La **classe \_ DeviceMemoryAddress Win32** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ DeviceMemoryAddress Win32** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto, una stringa di una riga.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**chiave \_ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata nella creazione di un'istanza di . Se usata con le altre proprietà chiave della classe , la proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO.**](cim-memorymappedio.md)

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome della classe di creazione del computer di ambito.

Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO.**](cim-memorymappedio.md)

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome del computer di ambito.

Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO.**](cim-memorymappedio.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Mapped I/O \| 001.2")
</dt> </dl>

Indirizzo finale dell'I/O mappato alla memoria.

Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO.**](cim-memorymappedio.md)

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**MemoryType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| SystemStructures \| CM PARTIAL RESOURCE \_ \_ \_ DESCRIPTOR \| Flags")
</dt> </dl>

Caratteristiche della risorsa di memoria nel computer che esegue Windows. I valori sono i seguenti.

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")


</dt> <dd>

La memoria può essere sia letta che scritta.

</dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")


</dt> <dd>

La memoria è di sola lettura.

</dd> <dt>

<span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>

<span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")


</dt> <dd>

La memoria può essere scritta solo.

</dd> <dt>

<span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>

<span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Preletturabile** ("Preletturabile")


</dt> <dd>

Un blocco di memoria viene copiato dalla memoria principale in un piccolo buffer gestito dal chipset di memoria. Le operazioni di lettura ripetute dalla stessa parte della memoria sono più veloci con la memoria prelettura.

</dd> <dt>

<span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>

<span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")


</dt> <dd>

DA DEFINIRE

</dd> <dt>

<span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>

<span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")


</dt> <dd>

DA DEFINIRE

</dd> <dt>

<span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>

<span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Memorizzabile nella** cache ("memorizzabile nella cache")


</dt> <dd>

DA DEFINIRE

</dd> <dt>

<span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>

<span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")


</dt> <dd>

DA DEFINIRE

</dd> <dt>

<span id="Bar"></span><span id="bar"></span><span id="BAR"></span>

<span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Bar** ("Bar")


</dt> <dd>

DA DEFINIRE

</dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. In caso di sottoclasse, è possibile eseguire l'override della proprietà come proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Indirizzo iniziale**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Mapped I/O \| 001.1")
</dt> </dl>

Indirizzo iniziale dell'I/O mappato alla memoria. La proprietà dell'identificatore di risorsa hardware deve essere impostata su questo valore per costruire la chiave della risorsa di I/O mappata.

Questa proprietà viene ereditata da [**CIM \_ MemoryMappedIO.**](cim-memorymappedio.md)

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un disco rigido abilitato per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati non di operazione includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono online, ma l'elemento gestito non è né "OK" né in uno degli altri stati.

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

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ DeviceMemoryAddress Win32** è derivata da [**\_ SystemMemoryResource Win32.**](win32-systemmemoryresource.md)

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

[**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md)
</dt> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

