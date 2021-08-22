---
description: Usato nel metodo GetSummaryInformation nella classe Msvm VirtualSystemManagementService per recuperare rapidamente le informazioni comuni correlate a un sistema virtuale \_ o a uno snapshot.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Msvm_SummaryInformationBase classe
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
ms.openlocfilehash: d131a2630c0c64e4b4b6bcec371eb901665c989948a1db510b47a41d9159f06d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950100"
---
# <a name="msvm_summaryinformationbase-class"></a>Classe Msvm \_ SummaryInformationBase

Usato nel [**metodo GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) nella classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) per recuperare rapidamente le informazioni comuni correlate a un sistema virtuale o a uno snapshot.

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

La **classe Msvm \_ SummaryInformationBase** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SummaryInformationBase** ha queste proprietà.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di creazione del sistema virtuale o dello snapshot.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement.ElementName")
</dt> </dl>

Nome descrittivo del sistema virtuale o dello snapshot.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente del sistema virtuale o dello snapshot.

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se le connessioni in modalità avanzata sono consentite dall'host e, se consentite, se sono disponibili o meno per la macchina virtuale.

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

**Stato di integrità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato di integrità corrente per il sistema virtuale. Questa proprietà non è valida per le istanze di [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) che rappresentano uno snapshot del sistema virtuale.

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer che ospita la macchina virtuale.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID è una proprietà facoltativa che può essere usata per identificare in modo opaco e univoco un'istanza di questa classe nell'ambito dello spazio dei nomi di creazione dell'istanza. Diverse sottoclassi di questa classe possono eseguire l'override di questa proprietà per renderla obbligatoria o una chiave. Tali sottoclassi possono anche modificare gli algoritmi preferiti per garantire l'univocità definita di seguito.

Per garantire l'univocità all'interno di NameSpace, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente:

<OrgID>:<LocalID>

Dove e sono separati da due punti (:) e dove devono includere un nome protetto da copyright, marchio o altrimenti univoco di proprietà dell'entità aziendale che crea o definisce InstanceID o che è un ID registrato assegnato all'entità aziendale da un'autorità globale <OrgID> <LocalID> <OrgID> riconosciuta. Questo requisito è simile al seguente: <Schema Name> \_ <Class Name> struttura dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, <OrgID> non deve contenere i due punti (:). Quando si usa questo algoritmo, i primi due punti da visualizzare in InstanceID devono essere compresi tra <OrgID> e <LocalID> .

<LocalID> viene scelto dall'entità business e non deve essere riutilizzato per identificare diversi elementi sottostanti (reali). Se non è Null e l'algoritmo "preferito" precedente non viene usato, l'entità di definizione deve garantire che l'InstanceID risultante non viene riutilizzato in alcun InstanceID prodotto da questo o da altri provider per lo spazio dei nomi di questa istanza.

Se non è impostato su Null per le istanze definite da DMTF, l'algoritmo "preferito" deve essere usato con <OrgID> impostato su CIM.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome univoco per il sistema virtuale o lo snapshot.

</dd> <dt>

**Note**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Note associate al sistema virtuale o allo snapshot.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di processori virtuali allocati al sistema virtuale o allo snapshot.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Stato corrente dell'elemento.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la **proprietà EnabledState** è impostata su 1 ("Other"). Questa proprietà deve essere impostata su Null quando **EnabledState** è un valore diverso da 1.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Stringhe che descrivono i vari **valori della matrice OperationalStatus.**

</dd> <dt>

**Uptime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Periodo di tempo dall'ultimo avvio del sistema virtuale. Questa proprietà non è valida per le istanze di [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) che rappresentano uno snapshot del sistema virtuale.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del sistema virtuale nel formato "major.minor"; ad esempio "2.0".

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Stringhe che elencano i nomi descrittivi dei commutatori virtuali a cui è connessa la macchina virtuale.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Sottotipo del sistema virtuale.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Visualizzazione \_ CIM**](cim-view.md)
</dt> </dl>

 

