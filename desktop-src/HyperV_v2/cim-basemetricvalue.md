---
description: Rappresenta il valore dell'istanza di una metrica.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: CIM_BaseMetricValue classe
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
ms.openlocfilehash: 107dc3721ee32ca7f51efd563cdd6af14af483a69a5990e0b107a153b79b9351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014699"
---
# <a name="cim_basemetricvalue-class"></a>Classe CiM \_ BaseMetricValue

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

La **classe CIM \_ BaseMetricValue** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ BaseMetricValue** ha queste proprietà.

<dl> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensione per cui questo set di valori della metrica viene suddiviso in base alla **proprietà BreakdownDimensions** dell'oggetto [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associato.

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore della proprietà **BreakdownDimension** definita per questo valore dell'istanza. Ad esempio, se **BreakdownDimension** contiene "TransactionName", questa proprietà potrebbe assegnare un nome alla transazione effettiva a cui si applica questo particolare valore della metrica.

</dd> <dt>

**Duration**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM \_ BaseMetricValue**.**TimeStamp**")
</dt> </dl>

Durata di validità del valore della metrica. Questa proprietà non deve esistere per i timestamp che si applicano solo a un punto nel tempo, ma deve essere definita per i valori considerati validi per un determinato periodo di tempo (ad esempio. campionamento). Se la **proprietà Duration** esiste ed è non Null, il **valore TimeStamp** deve essere la fine dell'intervallo.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe nell'ambito dello spazio dei nomi contenitore.

> [!IMPORTANT]
>
> Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalID*
>
> *OrgID* deve includere un nome protetto da copyright, con marchio o altrimenti univoco di proprietà dell'entità aziendale che definisce **InstanceID** o un ID registrato assegnato da un'autorità globale riconosciuta. Questo modello è simile alla struttura dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, i primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalID*. *L'OrgID non* deve pertanto contenere i due punti (':').
>
> *LocalID* viene scelto dall'entità aziendale e non deve essere usato nuovamente per identificare diversi elementi reali sottostanti.
>
> Se il modello precedente non viene usato, l'entità di definizione deve garantire che il valore **InstanceID** risultante non viene usato di nuovo in tutte le proprietà **InstanceID** prodotte da questo provider o da altri provider per questo spazio dei nomi.
>
> Per le istanze definite dalla dmtf (Distributed Management Task Force), il modello deve essere usato con *OrgID* impostato su CIM.

 

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome descrittivo dell'elemento misurato dalla metrica.

Questa proprietà è obbligatoria se la definizione della metrica non è associata a un [**oggetto CIM \_ ManagedElement**](cim-managedelement.md) e può essere usata in altri casi per fornire informazioni supplementari. In questo modo le metriche possono essere acquisite indipendentemente da **qualsiasi \_ oggetto CIM ManagedElement.**

Se sono presenti [**più oggetti \_ CIM ManagedElement**](cim-managedelement.md) associati al valore della metrica, è possibile scegliere uno degli elementi gestiti per creare le informazioni supplementari per la metrica. La proprietà non deve essere utilizzata come chiave esterna per eseguire query sull'elemento misurato. È invece consigliabile usare **l'associazione a \_ CIM ManagedElement.**

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Obbligatorio,**](/windows/desktop/WmiSdk/standard-qualifiers) [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**ID**")
</dt> </dl>

Chiave [**dell'istanza CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associata a questo valore dell'istanza.

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **obbligatori**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Rappresentazione di stringa del valore della metrica. Il tipo di dati originale del valore della metrica viene specificato [**nell'oggetto CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associato.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM \_ BaseMetricValue**.**Duration**")
</dt> </dl>

Ora in cui viene calcolato il valore di un'istanza della metrica. Questo valore è diverso dal momento in cui viene creata l'istanza di . Se la **proprietà Volatile** è true, questo valore cambia ogni volta che viene creato un nuovo snapshot di misurazione.

Un'applicazione di gestione può stabilire una serie temporale di dati delle metriche recuperando le istanze di **CIM \_ BaseMetricValue** e ordinandole in base al **relativo valore TimeStamp.**

</dd> <dt>

**Volatile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

True se il **valore TimeStamp** cambia ogni volta che cambia il valore dell'istanza della metrica. False se questo oggetto deve rimanere invariato e un nuovo oggetto creato per il nuovo **valore TimeStamp.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

