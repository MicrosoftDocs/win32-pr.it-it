---
description: Rappresenta gli aspetti della definizione di una metrica derivata da un altro valore della metrica.
ms.assetid: 642f53fe-e51c-4c73-babf-19adb2cf55f4
title: Classe Msvm_AggregationMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricDefinition
- Msvm_AggregationMetricDefinition.InstanceID
- Msvm_AggregationMetricDefinition.Caption
- Msvm_AggregationMetricDefinition.Description
- Msvm_AggregationMetricDefinition.ElementName
- Msvm_AggregationMetricDefinition.Id
- Msvm_AggregationMetricDefinition.Name
- Msvm_AggregationMetricDefinition.DataType
- Msvm_AggregationMetricDefinition.Calculable
- Msvm_AggregationMetricDefinition.Units
- Msvm_AggregationMetricDefinition.BreakdownDimensions
- Msvm_AggregationMetricDefinition.IsContinuous
- Msvm_AggregationMetricDefinition.ChangeType
- Msvm_AggregationMetricDefinition.TimeScope
- Msvm_AggregationMetricDefinition.GatheringType
- Msvm_AggregationMetricDefinition.ProgrammaticUnits
- Msvm_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: da52c154c90b58fc147a52268025887d2dfa8f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232687"
---
# <a name="msvm_aggregationmetricdefinition-class"></a>\_Classe MSVM AggregationMetricDefinition

Rappresenta gli aspetti della definizione di una metrica derivata da un altro valore della metrica. L' **oggetto \_ AggregationMetricDefinition di MSVM** deve essere associato agli elementi gestiti a cui si applica.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricDefinition : CIM_AggregationMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
  uint16  SimpleFunction;
};
```

## <a name="members"></a>Members

La **classe \_ AggregationMetricDefinition di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ AggregationMetricDefinition di MSVM** dispone di queste proprietà.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Definisce una o più stringhe che possono essere utilizzate per perfezionare (suddividere) query sui valori della metrica lungo una determinata dimensione. Un esempio è un nome di transazione, che consente l'interruzione del valore totale di tutte le transazioni in un set di valori, uno per ogni nome di transazione. Altri esempi possono essere il nome del sistema dell'applicazione o del gruppo di utenti. Le stringhe sono di formato libero e dovrebbero essere significative per gli utenti finali dei dati della metrica. Le stringhe indicano quali dimensioni di suddivisione sono supportate per questa definizione di metrica dalla strumentazione sottostante. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.

</dd> <dt>

**Calcolabile**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive le caratteristiche della metrica a scopo di esecuzione dei calcoli. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**. Può essere **null** o uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <dt>**Non calcolabile**</dt> <dt>1</dt> </dl> | Non è possibile calcolare il valore. Ad esempio, una stringa.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <dt>**Sommabile**</dt> <dt>2</dt> </dl>                         | Il valore può essere sommato in molte istanze. Ad esempio, se ogni processo di backup è un'unità di lavoro e ogni processo esegue il backup di 27.000 file in media, 100 processi di backup elaborati 2,7 milioni file.<br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <dt> **Non sommabile**</dt> <dt>3</dt> </dl>    | Questo valore non può essere sommato in molte istanze. Un esempio è una metrica che misura la lunghezza della coda quando un processo arriva a un server. Se ogni processo è un'unità di lavoro e la lunghezza media della coda quando ogni processo arriva è 33, non è sensato dire che la lunghezza della coda per i processi 100 è 3300. È sensato dire che la media è 33.<br/> |



 

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il modo in cui viene modificato il valore della metrica, sotto forma di combinazioni tipiche di attributi di granularità più sottili, ad esempio la modifica della direzione, i valori minimo e massimo e la semantica di wrapping. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                                 | La finestra di progettazione metrica non ha qualificato l'oggetto **ChangeType**.<br/>                                                                                                                               |
| <span id="N_A"></span><span id="n_a"></span><dl> <dt>**N/A**</dt> <dt>2</dt> </dl>                                                                                       | Se la proprietà di **discontinuità** è "false", **ChangeType** non ha senso e deve essere impostato su "N/A".<br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <dt>**Contatore**</dt> <dt>3</dt> </dl>                                                 | La metrica è una metrica del contatore. Questi includono valori interi non negativi che aumentano fino a raggiungere il numero massimo rappresentabile, quindi eseguire il wrapping e iniziare ad aumentare da 0.<br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <dt>**Misuratore**</dt> <dt>4</dt> </dl>                                                         | La metrica è una metrica del misuratore. Hanno valori integer o float che possono aumentare e diminuire in modo arbitrario.<br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF riservato**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> 32768 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt> </dl> | I fornitori possono estendere la proprietà **ChangeType** nell'intervallo riservato del fornitore.<br/>                                                                                                          |



 

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di dati della metrica. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.

<dl> <dt>

<span id="boolean"></span><span id="BOOLEAN"></span>**valore booleano** (1)
</dt> <dt>

<span id="char16"></span><span id="CHAR16"></span>**Char16** (2)
</dt> <dt>

<span id="datetime"></span><span id="DATETIME"></span>**DateTime** (3)
</dt> <dt>

<span id="real32"></span><span id="REAL32"></span>**real32** (4)
</dt> <dt>

<span id="real64"></span><span id="REAL64"></span>**real64** (5)
</dt> <dt>

<span id="sint16"></span><span id="SINT16"></span>**sint16** (6)
</dt> <dt>

<span id="sint32"></span><span id="SINT32"></span>**sint32** (7)
</dt> <dt>

<span id="sint64"></span><span id="SINT64"></span>**sint64** (8)
</dt> <dt>

<span id="sint8"></span><span id="SINT8"></span>**sint8** (9)
</dt> <dt>

<span id="string"></span><span id="STRING"></span>**stringa** (10)
</dt> <dt>

<span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)
</dt> <dt>

<span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)
</dt> <dt>

<span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)
</dt> <dt>

<span id="uint8_"></span><span id="UINT8_"></span>**Uint8** (14)
</dt> </dl>

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il modo in cui i valori delle metriche vengono raccolti dalla strumentazione sottostante. Ciò consente all'applicazione client di scegliere la metrica corretta per lo scopo. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**. Può essere **null** o uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                                 | Il tipo di raccolta non è noto.<br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <dt>**OnChange**</dt> <dt>2</dt> </dl>                                             | I valori delle metriche vengono aggiornati immediatamente quando i valori all'interno della risorsa misurata cambiano.<br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <dt>3</dt> <dt>**periodici**</dt> </dl>                                             | I valori delle metriche vengono aggiornati periodicamente. Ad esempio, per un'applicazione client, un valore della metrica che si applica all'ora corrente apparirà costante durante ogni intervallo di raccolta, quindi passa al nuovo valore alla fine di ogni intervallo di raccolta.<br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <dt>**OnRequest**</dt> <dt>4</dt> </dl>                                         | Il valore della metrica viene determinato ogni volta che viene letto da un'applicazione client.<br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF riservato**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> 32768 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Stringa che identifica in modo univoco la definizione della metrica. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Stringa che identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il valore della metrica è continuo o scalare. Le metriche delle prestazioni sono un esempio di metrica continua. Esempi di metriche scalari includono codici di errore o stati operativi. È possibile confrontare le metriche continue usando la relazione "maggiore di". Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della metrica. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica le unità specifiche di un valore. Il valore di questa proprietà sarà un valore valido del qualificatore unità programmatiche come definito nell'Appendice C. 1 di [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) o versione successiva. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.

</dd> <dt>

**SimpleFunction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Identifica il calcolo di base eseguito su una metrica sottostante per giungere al valore di questa metrica derivata. Questa proprietà viene ereditata da **CIM \_ AggregationMetricDefinition** e sarà uno dei valori seguenti.

<dl> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimo** (2)
</dt> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Massimo** (3)
</dt> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Media** (4)
</dt> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Mediana** (5)
</dt> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modalità** (6)
</dt> </dl>

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica l'ambito temporale a cui si applica il valore della metrica. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                                 | L'ambito temporale non è stato qualificato dalla finestra di progettazione della metrica o è sconosciuto al provider.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Punto**</dt> <dt>2</dt> </dl>                                                         | La metrica si applica a un punto nel tempo. Nelle istanze [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) corrispondenti la proprietà **timestamp** specifica il punto nel tempo e la proprietà **Duration** è sempre 0.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <dt>**Intervallo**</dt> <dt>3</dt> </dl>                                             | La metrica si applica a un intervallo di tempo. Nelle istanze [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) corrispondenti la proprietà **timestamp** specifica la fine dell'intervallo di tempo e la proprietà **Duration** ne specifica la durata.<br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <dt>**StartupInterval**</dt> <dt>4</dt> </dl>                 | La metrica si applica a un intervallo di tempo che inizia all'avvio della risorsa misurata (ovvero l'oggetto gestito associato da MetricDefForMe). Nelle istanze [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) corrispondenti la proprietà **timestamp** specifica la fine dell'intervallo di tempo. Se la proprietà **Duration** è 0, indica che il tempo di avvio della risorsa misurata è sconosciuto. In caso contrario, **Duration** specifica la durata tra l'avvio della risorsa e il **timestamp**.<br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF riservato**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> 32768 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Unità**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica le unità di un valore, ad esempio "megabyte". Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

