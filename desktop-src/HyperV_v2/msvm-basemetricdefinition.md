---
description: Rappresenta gli aspetti della definizione di una metrica.
ms.assetid: 861a69f6-a3bf-4e18-a9c2-931632e3cccc
title: Msvm_BaseMetricDefinition classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricDefinition
- Msvm_BaseMetricDefinition.InstanceID
- Msvm_BaseMetricDefinition.Caption
- Msvm_BaseMetricDefinition.Description
- Msvm_BaseMetricDefinition.ElementName
- Msvm_BaseMetricDefinition.Id
- Msvm_BaseMetricDefinition.Name
- Msvm_BaseMetricDefinition.DataType
- Msvm_BaseMetricDefinition.Calculable
- Msvm_BaseMetricDefinition.Units
- Msvm_BaseMetricDefinition.BreakdownDimensions
- Msvm_BaseMetricDefinition.IsContinuous
- Msvm_BaseMetricDefinition.ChangeType
- Msvm_BaseMetricDefinition.TimeScope
- Msvm_BaseMetricDefinition.GatheringType
- Msvm_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4193f934dd17224091974a705288831e28253876d05ca1b5fc4b99c9c70424e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790241"
---
# <a name="msvm_basemetricdefinition-class"></a>Classe Msvm \_ BaseMetricDefinition

Rappresenta gli aspetti della definizione di una metrica. La **classe Msvm \_ BaseMetricDefinition** deve essere associata agli [**\_ elementi gestiti CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) a cui si applica.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricDefinition : CIM_BaseMetricDefinition
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
};
```

## <a name="members"></a>Members

La **classe Msvm \_ BaseMetricDefinition** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ BaseMetricDefinition** ha queste proprietà.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Definisce una o più stringhe che possono essere usate per affinare (suddividere) le query sui valori delle metriche lungo una determinata dimensione. Un esempio è un nome di transazione, che consente di suddividere il valore totale per tutte le transazioni in un set di valori, uno per ogni nome di transazione. Altri esempi possono essere il nome del sistema dell'applicazione o del gruppo di utenti. Le stringhe sono in formato libero e devono essere significative per gli utenti finali dei dati delle metriche. Le stringhe indicano le dimensioni di scomposimento supportate per questa definizione di metrica dalla strumentazione sottostante. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition.**

</dd> <dt>

**Calcolabile**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive le caratteristiche della metrica ai fini dell'esecuzione dei calcoli. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition.** Può essere **Null** o uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <dt>**Non calcolo**</dt> <dt>1</dt> </dl> | Il valore non può essere calcolato. Ad esempio, una stringa.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <dt>**Sommabile**</dt> <dt>2</dt> </dl>                         | Il valore può essere sommato su molte istanze. Ad esempio, se ogni processo di backup è un'unità di lavoro e ogni processo backup di 27.000 file in media, 100 processi di backup hanno elaborato 2.700.000 file.<br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <dt> **Non sommabile**</dt> <dt>3</dt> </dl>    | Questo valore non può essere sommato in molte istanze. Un esempio è una metrica che misura la lunghezza della coda quando un processo arriva a un server. Se ogni processo è un'unità di lavoro e la lunghezza media della coda all'arrivo di ogni processo è 33, non ha senso dire che la lunghezza della coda per 100 processi è 3300. È opportuno dire che la media è 33.<br/> |



 

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il modo in cui cambia il valore della metrica, sotto forma di combinazioni tipiche di attributi di granularità più fine, ad esempio modifica della direzione, valori minimi e massimi e semantica di wrapping. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition.**



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                                 | La finestra di progettazione delle metriche non ha qualificato **ChangeType.**.<br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <dt>**N/D**</dt> <dt>2</dt> </dl>                                                                                       | Se la **proprietà IsContinuous** è "false", **ChangeType** non ha senso e deve essere impostato su "N/D".<br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <dt>**Contatore**</dt> <dt>3</dt> </dl>                                                 | La metrica è una metrica contatore. Questi hanno valori interi non negativi che aumentano fino a raggiungere il numero massimo rappresentabile e quindi vengono incapsulati e iniziano ad aumentare da 0.<br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <dt>**Misuratore**</dt> <dt>4</dt> </dl>                                                         | La metrica è una metrica del misuratore. Hanno valori interi o float che possono aumentare e diminuire in modo arbitrario.<br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF riservato**</dt> <dt>5..32767</dt> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Fornitore riservato**</dt> <dt>32768..65535</dt> </dl> | I fornitori possono estendere la **proprietà ChangeType** nell'intervallo riservato del fornitore.<br/>                                                                                                          |



 

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di dati della metrica. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition.**

<dl> <dt>

<span id="boolean"></span><span id="BOOLEAN"></span>**booleano** (1)
</dt> <dt>

<span id="char16"></span><span id="CHAR16"></span>**char16** (2)
</dt> <dt>

<span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)
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

<span id="string"></span><span id="STRING"></span>**string** (10)
</dt> <dt>

<span id="uint16"></span><span id="UINT16"></span>**uint16** (11)
</dt> <dt>

<span id="uint32"></span><span id="UINT32"></span>**uint32** (12)
</dt> <dt>

<span id="uint64"></span><span id="UINT64"></span>**uint64** (13)
</dt> <dt>

<span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )
</dt> </dl>

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica come i valori delle metriche vengono raccolti dalla strumentazione sottostante. In questo modo l'applicazione client può scegliere la metrica giusta per lo scopo. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition.** Può essere **Null** o uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                                 | Il tipo di raccolta non è noto.<br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <dt>**OnChange**</dt> <dt>2</dt> </dl>                                             | I valori delle metriche vengono aggiornati immediatamente quando i valori all'interno della risorsa misurata cambiano.<br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <dt>**Periodico**</dt> <dt>3</dt> </dl>                                             | I valori delle metriche vengono aggiornati periodicamente. Ad esempio, per un'applicazione client, un valore della metrica che si applica all'ora corrente apparirà costante durante ogni intervallo di raccolta e quindi passa al nuovo valore alla fine di ogni intervallo di raccolta.<br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <dt>**OnRequest**</dt> <dt>4</dt> </dl>                                         | Il valore della metrica viene determinato ogni volta che viene letto da un'applicazione client.<br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reserved**</dt> <dt>5..32767</dt> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Fornitore riservato**</dt> <dt>32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Stringa che identifica in modo univoco la definizione della metrica. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition.**

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Stringa che identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il valore della metrica è continuo o scalare. Le metriche delle prestazioni sono un esempio di metrica continua. Esempi di metriche scalari includono codici di errore o stati operativi. Le metriche continue possono essere confrontate usando la relazione "maggiore di". Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition.**

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della metrica. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition.**

</dd> <dt>

**Unità programmatiche**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica le unità specifiche di un valore. Il valore di questa proprietà sarà un valore valido del qualificatore di unità programmatiche, come definito nell'Appendice C.1 di [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) o versione successiva. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition.**

</dd> <dt>

**Ambito temporale**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica l'ambito temporale a cui si applica il valore della metrica. Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition.**



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                                 | L'ambito temporale non è stato qualificato dalla finestra di progettazione delle metriche o è sconosciuto al provider.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Punto**</dt> <dt>2</dt> </dl>                                                         | La metrica si applica a un punto nel tempo. Nelle istanze [**di \_ Msvm BaseMetricValue**](msvm-basemetricvalue.md) corrispondenti, la **proprietà TimeStamp** specifica il punto nel tempo e la proprietà **Duration** è sempre 0.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <dt>**Intervallo**</dt> <dt>3</dt> </dl>                                             | La metrica si applica a un intervallo di tempo. Nelle istanze [**di \_ Msvm BaseMetricValue**](msvm-basemetricvalue.md) corrispondenti, la proprietà **TimeStamp** specifica la fine dell'intervallo di tempo e la **proprietà Duration** ne specifica la durata.<br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <dt>**StartupInterval**</dt> <dt>4</dt> </dl>                 | La metrica si applica a un intervallo di tempo iniziato all'avvio della risorsa misurata, ovvero l'elemento ManagedElement associato da MetricDefForMe. Nelle istanze [**Di \_ BaseMetricValue msvm**](msvm-basemetricvalue.md) corrispondenti, la proprietà **TimeStamp** specifica la fine dell'intervallo di tempo. Se la **proprietà Duration** è 0, significa che il tempo di avvio della risorsa misurata è sconosciuto. In caso **contrario, Durata** specifica la durata tra l'avvio della risorsa e **TimeStamp.**<br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reserved**</dt> <dt>5..32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Fornitore riservato**</dt> <dt>32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Unità**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica le unità specifiche di un valore, ad esempio "megabyte". Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

