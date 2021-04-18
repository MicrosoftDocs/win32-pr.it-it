---
description: La \_ classe CIM StorageRedundancyGroup rappresenta informazioni di ridondanza relative all'archiviazione di massa.
ms.assetid: 6bc81680-672a-4872-8951-11d7f10acbc7
ms.tgt_platform: multiple
title: Classe CIM_StorageRedundancyGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageRedundancyGroup
- CIM_StorageRedundancyGroup.Caption
- CIM_StorageRedundancyGroup.Description
- CIM_StorageRedundancyGroup.InstallDate
- CIM_StorageRedundancyGroup.Name
- CIM_StorageRedundancyGroup.Status
- CIM_StorageRedundancyGroup.CreationClassName
- CIM_StorageRedundancyGroup.RedundancyStatus
- CIM_StorageRedundancyGroup.TypeOfAlgorithm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bef8cb8029c62957446ee5d7aefcf67fe5d7acb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304484"
---
# <a name="cim_storageredundancygroup-class"></a>CIM \_ StorageRedundancyGroup (classe)

La classe **CIM \_ StorageRedundancyGroup** rappresenta informazioni di ridondanza relative all'archiviazione di massa. I gruppi di ridondanza di archiviazione vengono usati per proteggere i dati utente. Sono costituiti da uno o più extent fisici o da uno o più extent fisici aggregati. I gruppi di ridondanza dell'archiviazione possono sovrapporsi; Tuttavia, gli extent sottostanti all'interno della sovrapposizione non devono contenere dati di controllo.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{6D477DBC-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_StorageRedundancyGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint16   TypeOfAlgorithm;
};
```

## <a name="members"></a>Members

La classe **CIM \_ StorageRedundancyGroup** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ StorageRedundancyGroup** dispone di queste proprietà.

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

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).

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

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**RedundancyStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Informazioni sullo stato del gruppo di ridondanza.

Questa proprietà viene ereditata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

Sconosciuto.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

Altro.

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Completamente ridondante** (2)


</dt> <dd>

È disponibile tutta la ridondanza configurata.

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Ridondanza danneggiata** (3)


</dt> <dd>

È disponibile una minore quantità di ridondanza a causa di alcuni errori.

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Ridondanza persa** (4)


</dt> <dd>

La ridondanza non è disponibile a causa di un numero sufficiente di errori. L'errore successivo provocherà un errore generale.

</dd> </dl>

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

</dd> <dt>

**TypeOfAlgorithm**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Gruppo di ridondanza DMTF \| 001,2 ")
</dt> </dl>

Algoritmo utilizzato per la ridondanza e la ricostruzione dei dati. Il valore 0 non è valido nello schema CIM perché rappresenta che non esiste alcuna ridondanza in DMI. In tal caso, non è necessario creare un'istanza dell'oggetto.

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Non definito** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

**Copia** (3)


</dt> <dd></dd> <dt>

<span id="XOR"></span><span id="xor"></span>

**Xor** (4)


</dt> <dd></dd> <dt>

<span id="P_Q"></span><span id="p_q"></span>

**P + Q** (5)


</dt> <dd></dd> <dt>

<span id="S"></span><span id="s"></span>

**S** (6)


</dt> <dd></dd> <dt>

<span id="P_S"></span><span id="p_s"></span>

**P + S** (7)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ StorageRedundancyGroup** è derivata da [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

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

[**\_REDUNDANCYGROUP CIM**](cim-redundancygroup.md)
</dt> </dl>

 

