---
description: La \_ classe CIM PhysicalFrame è una classe padre di rack, chassis e altre enclosure di frame così come sono definiti nelle classi di estensione.
ms.assetid: 571c8ca2-1644-4060-8d89-d9625a591f86
ms.tgt_platform: multiple
title: Classe CIM_PhysicalFrame
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame
- CIM_PhysicalFrame.AudibleAlarm
- CIM_PhysicalFrame.BreachDescription
- CIM_PhysicalFrame.CableManagementStrategy
- CIM_PhysicalFrame.Caption
- CIM_PhysicalFrame.CreationClassName
- CIM_PhysicalFrame.Depth
- CIM_PhysicalFrame.Description
- CIM_PhysicalFrame.Height
- CIM_PhysicalFrame.HotSwappable
- CIM_PhysicalFrame.InstallDate
- CIM_PhysicalFrame.LockPresent
- CIM_PhysicalFrame.Manufacturer
- CIM_PhysicalFrame.Model
- CIM_PhysicalFrame.Name
- CIM_PhysicalFrame.OtherIdentifyingInfo
- CIM_PhysicalFrame.PartNumber
- CIM_PhysicalFrame.PoweredOn
- CIM_PhysicalFrame.Removable
- CIM_PhysicalFrame.Replaceable
- CIM_PhysicalFrame.SecurityBreach
- CIM_PhysicalFrame.SerialNumber
- CIM_PhysicalFrame.ServiceDescriptions
- CIM_PhysicalFrame.ServicePhilosophy
- CIM_PhysicalFrame.SKU
- CIM_PhysicalFrame.Status
- CIM_PhysicalFrame.Tag
- CIM_PhysicalFrame.Version
- CIM_PhysicalFrame.VisibleAlarm
- CIM_PhysicalFrame.Weight
- CIM_PhysicalFrame.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b445c928412bc475a3269ba59be48395b254efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127382"
---
# <a name="cim_physicalframe-class"></a>CIM \_ PhysicalFrame (classe)

La classe **CIM \_ PhysicalFrame** è una classe padre di rack, chassis e altre enclosure di frame così come sono definiti nelle classi di estensione. In questa classe padre sono incluse proprietà quali **VisibleAlarm** e **AudibleAlarm** e i dati relativi alle violazioni della sicurezza.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract, UUID("{FAF76B70-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalFrame : CIM_PhysicalPackage
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Members

La classe **CIM \_ PhysicalFrame** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **CIM \_ PhysicalFrame** presenta questi metodi.



| Metodo                                                                 | Descrizione                                                                                                                                      |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCompatible**](iscompatible-method-in-class-cim-physicalframe.md) | Verifica se l'elemento fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico. Non implementato da WMI.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **CIM \_ PhysicalFrame** dispone di queste proprietà.

<dl> <dt>

**AudibleAlarm**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il frame è dotato di un allarme acustico.

</dd> <dt>

**BreachDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**SecurityBreach**")
</dt> </dl>

Stringa in formato libero che fornisce ulteriori informazioni se la proprietà **SecurityBreach** indica che si è verificata una violazione o un altro evento correlato alla sicurezza.

</dd> <dt>

**CableManagementStrategy**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che contiene informazioni sul modo in cui i vari cavi sono connessi e in bundle per il frame. Con molti cavi di rete, correlati all'archiviazione e di alimentazione, la gestione dei cavi può essere un'attività complessa e impegnativa. Questa proprietà di stringa contiene informazioni per facilitare l'assembly e il servizio del frame.

</dd> <dt>

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

Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Livello nidificazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")
</dt> </dl>

Profondità del pacchetto fisico, in pollici.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

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

**Altezza**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")
</dt> </dl>

Altezza del pacchetto fisico, in pollici.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il pacchetto può essere scambiato a caldo. Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un oggetto fisicamente diverso (ma equivalente) uno mentre il pacchetto contenitore è attivato. Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo. Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LockPresent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il frame è protetto con un blocco.

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome dell'organizzazione responsabile della creazione dell'elemento fisico. Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Modello**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nome in base al quale l'elemento fisico è generalmente noto.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

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

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico. Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset. Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**NumeroArticolo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, l'elemento fisico è acceso; in caso contrario, è attualmente disattivato.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Rimovibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, questo elemento è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti. Un pacchetto viene considerato rimovibile anche se è necessario spegnere l'alimentazione per eseguire la rimozione. Se la potenza può essere accesa e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo. Ad esempio, un chip del processore aggiornabile è rimovibile.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**Sostituibili**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, è possibile sostituire l'elemento con uno fisicamente diverso. Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate. In questo caso, il processore viene definito sostituibile. Tutti i componenti rimovibili sono intrinsecamente sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**SecurityBreach**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| tabella globale del contenitore fisico \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**BreachDescription**")
</dt> </dl>

Indica se una violazione fisica del frame è stata tentata, ma non è stata completata, oppure se è stata tentata e riuscita.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

**Nessuna violazione** (3)


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

**Tentativo di violazione** (4)


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

**Violazione riuscita** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Numero allocato dal produttore utilizzato per identificare l'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**ServiceDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**ServicePhilosophy**")
</dt> </dl>

Stringhe in formato libero che forniscono spiegazioni dettagliate per le voci nella matrice **ServicePhilosophy** .

> [!Note]  
> Ogni voce di questa matrice è correlata alla voce nella matrice **ServicePhilosophy** che si trova nello stesso indice.

 

</dd> <dt>

**ServicePhilosophy**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**ServiceDescriptions**")
</dt> </dl>

Indica se il frame viene servito dalla parte superiore, anteriore, posteriore o laterale; e se sono presenti vassoi scorrevoli o lati rimovibili e se il frame è mobile (ad esempio, con i Roller).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

**Servizio dall'inizio** (2)


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

**Servizio dall'inizio** (3)


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

**Servizio da indietro** (4)


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

**Servizio dal lato** (5)


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

**Vassoi scorrevoli** (6)


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

**Lati rimovibili** (7)


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

**Mobile** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Numero di unità per l'elemento fisico che mantiene le scorte.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Stato corrente dell'oggetto.

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

**Tag**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Stringa arbitraria che identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento. Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie. La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via. Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato. L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito. La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Stringa che indica la versione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**VisibleAlarm**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, l'apparecchiatura include un allarme visibile.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("libbre")
</dt> </dl>

Peso del pacchetto fisico, in sterline.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**Larghezza**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")
</dt> </dl>

Larghezza del pacchetto fisico, in pollici.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ PhysicalFrame** è derivata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

WMI non implementa questa classe. Per le classi WMI derivate da **CIM \_ PhysicalFrame**, vedere [Win32 Classes](win32-provider.md).

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

[**\_PHYSICALPACKAGE CIM**](cim-physicalpackage.md)
</dt> </dl>

 

