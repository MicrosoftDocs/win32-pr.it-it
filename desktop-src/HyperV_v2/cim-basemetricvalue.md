---
description: Rappresenta il valore dell'istanza di una metrica.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: Classe CIM_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ca6c90a4b6b3ef3e690c13612f69480ec5f008be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968109"
---
# <a name="cim_basemetricvalue-class"></a>CIM \_ BaseMetricValue (classe)

Rappresenta il valore dell'istanza di una metrica.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a>Members

La classe **CIM \_ BaseMetricValue** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ BaseMetricValue** dispone di queste proprietà.

<dl> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensione per la quale questo set di valori di metrica viene suddiviso in base alla proprietà **BreakdownDimensions** dell' [**oggetto \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) associato.

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore della proprietà **BreakdownDimension** definita per questo valore dell'istanza. Se, ad esempio, **BreakdownDimension** contiene "transactionName", questa proprietà potrebbe assegnare un nome alla transazione effettiva a cui si applica questo particolare valore della metrica.

</dd> <dt>

**Duration**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**CIM \_ BaseMetricValue**.**TimeStamp**")
</dt> </dl>

Durata del periodo di validità del valore della metrica. Questa proprietà non deve esistere per gli indicatori temporali che si applicano solo a un punto nel tempo, ma deve essere definito per i valori considerati validi per un determinato periodo di tempo (ad esempio, campionamento). Se la proprietà **Duration** esiste e è diversa da null, il valore di **timestamp** deve essere la fine dell'intervallo.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe nell'ambito dello spazio dei nomi che lo contiene.

> [!IMPORTANT]
>
> Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalId*
>
> *OrgID* deve includere un nome con copyright, marchio o in altro modo univoco, di proprietà dell'entità di business che definisce **InstanceID**, oppure essere un ID registrato assegnato da un'autorità globale riconosciuta. Questo modello è simile alla struttura dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, i primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalId*. Pertanto *OrgID* non deve contenere i due punti (':').
>
> Il *localizzato* viene scelto dall'entità di business e non deve essere riutilizzato per identificare diversi elementi reali sottostanti.
>
> Se il criterio precedente non viene utilizzato, l'entità di definizione deve assicurare che il valore **InstanceID** risultante non venga riutilizzato nelle proprietà **InstanceID** generate dal provider o da altri provider per questo spazio dei nomi.
>
> Per le istanze definite DMTF (Distributed Management Task Force), il modello deve essere usato con *OrgID* impostato su CIM.

 

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome descrittivo per l'elemento misurato dalla metrica.

Questa proprietà è obbligatoria se la definizione della metrica non è associata a un oggetto [**\_ gestito CIM**](cim-managedelement.md) e può essere usata in altri casi per fornire informazioni aggiuntive. Ciò consente di acquisire le metriche indipendentemente da qualsiasi oggetto **CIM \_ gestito** .

Se sono presenti più oggetti [**CIM \_ gestitielement**](cim-managedelement.md) associati al valore della metrica, è possibile scegliere uno degli elementi gestiti per creare le informazioni aggiuntive per la metrica. La proprietà non deve essere utilizzata come chiave esterna per eseguire una query sull'elemento misurato. È invece consigliabile usare l'associazione a **CIM \_ Managed** .

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**ID**")
</dt> </dl>

Chiave dell'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associata a questo valore dell'istanza.

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Rappresentazione di stringa del valore della metrica. Il tipo di dati originale del valore della metrica viene specificato nell'oggetto [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) associato.

</dd> <dt>

**TimeStamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**CIM \_ BaseMetricValue**.**Durata**")
</dt> </dl>

Data e ora in cui viene calcolato il valore di un'istanza della metrica. Questa operazione è diversa dal momento in cui viene creata l'istanza. Se la proprietà **volatile** è true, questo valore cambia ogni volta che viene eseguito un nuovo snapshot di misurazione.

Un'applicazione di gestione può stabilire una serie temporale di dati di metrica recuperando le istanze di **CIM \_ BaseMetricValue** e ordinando le istanze in base al relativo valore di **timestamp** .

</dd> <dt>

**Volatile**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

True se il valore di **timestamp** cambia ogni volta che viene modificato il valore dell'istanza della metrica. False se l'oggetto deve rimanere invariato e viene creato un nuovo oggetto per il nuovo valore di **timestamp** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ManagementName CIM**](cim-managedelement.md)
</dt> </dl>

 

