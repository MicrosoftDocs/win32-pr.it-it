---
description: Usato nel metodo GetSummaryInformation nella \_ classe MSVM VirtualSystemManagementService per recuperare rapidamente informazioni comuni correlate a un sistema virtuale o a uno snapshot.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Classe Msvm_SummaryInformationBase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65c20239673f279babba2581c4300f373f1392bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308909"
---
# <a name="msvm_summaryinformationbase-class"></a>\_Classe MSVM SummaryInformationBase

Usato nel metodo [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) nella classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) per recuperare rapidamente informazioni comuni correlate a un sistema virtuale o a uno snapshot.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a>Members

La **classe \_ SummaryInformationBase di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SummaryInformationBase di MSVM** dispone di queste proprietà.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora in cui è stato creato il sistema virtuale o lo snapshot.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ managed. ElementName")
</dt> </dl>

Nome descrittivo per il sistema virtuale o lo snapshot.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente del sistema virtuale o dello snapshot.

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se le connessioni in modalità avanzata sono consentite dall'host e se sono consentite, indipendentemente dal fatto che siano disponibili o meno per la macchina virtuale.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Consentito e disponibile** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**Non consentito** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Consentito ma non disponibile** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato di integrità corrente per il sistema virtuale. Questa proprietà non è valida per le istanze di [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) che rappresentano uno snapshot del sistema virtuale.

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer che ospita la macchina virtuale.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ managed. InstanceId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID è una proprietà facoltativa che può essere utilizzata per identificare in modo opaco e univoco un'istanza di questa classe nell'ambito dello spazio dei nomi di creazione di istanze. Varie sottoclassi di questa classe possono eseguire l'override di questa proprietà per renderla obbligatoria o una chiave. Tali sottoclassi possono anche modificare gli algoritmi preferiti per garantire l'univocità definita di seguito.

Per garantire l'univocità all'interno dello spazio dei nomi, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente:

<OrgID>:<LocalID>

Dove <OrgID> e <LocalID> sono separati da due punti (:) e dove <OrgID> devono includere un nome con copyright, un marchio o in altro modo univoco di proprietà dell'entità di business che crea o definisce InstanceID o che è un ID registrato assegnato all'entità business da un'autorità globale riconosciuta. (Questo requisito è simile al <Schema Name> \_ <Class Name> struttura dei nomi delle classi dello schema. Per garantire l'univocità, inoltre, <OrgID> non deve contenere i due punti (:). Quando si utilizza questo algoritmo, i primi due punti da visualizzare in InstanceID devono essere compresi tra <OrgID> e <LocalID> .

<LocalID> viene scelto dall'entità business e non deve essere riutilizzato per identificare elementi diversi (reali) sottostanti. Se non è null e l'algoritmo "preferito" precedente non viene utilizzato, l'entità di definizione deve garantire che l'ID istanza risultante non venga riutilizzato tra le InstanceID prodotte da questo o da altri provider per lo spazio dei nomi di questa istanza.

Se non è impostato su null per le istanze definite da DMTF, è necessario usare l'algoritmo "preferito" con <OrgID> impostato su CIM.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome univoco per il sistema virtuale o lo snapshot.

</dd> <dt>

**Note**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Note associate al sistema virtuale o allo snapshot.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di processori virtuali allocati al sistema virtuale o allo snapshot.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Stato corrente dell'elemento.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro"). Questa proprietà deve essere impostata su null quando **EnabledState** è un valore diverso da 1.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Stringhe che descrivono i vari valori della matrice **OperationalStatus** .

</dd> <dt>

**Tempo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Quantità di tempo trascorsa dall'ultimo avvio del sistema virtuale. Questa proprietà non è valida per le istanze di [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) che rappresentano uno snapshot del sistema virtuale.

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del sistema virtuale in formato "Major. minor"; ad esempio, "2,0".

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Stringhe che elencano i nomi descrittivi dei commutatori virtuali a cui è connessa la macchina virtuale.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Sottotipo del sistema virtuale.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft: Hyper-v: sottotipo: 1** ("Microsoft: Hyper-v: sottotipo: 1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft: Hyper-v: sottotipo: 2** ("Microsoft: Hyper-v: sottotipo: 2")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Visualizzazione CIM**](cim-view.md)
</dt> </dl>

 

