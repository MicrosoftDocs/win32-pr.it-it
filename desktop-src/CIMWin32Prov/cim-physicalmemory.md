---
description: La classe CIM PhysicalMemory rappresenta dispositivi di memoria di basso livello, ad esempio SIMMS, DIMM, chip di memoria non elaborata \_ e così via.
ms.assetid: a25c5f00-cd85-42e6-9b26-8e9380b3c73b
ms.tgt_platform: multiple
title: CIM_PhysicalMemory classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMemory
- CIM_PhysicalMemory.BankLabel
- CIM_PhysicalMemory.Capacity
- CIM_PhysicalMemory.Caption
- CIM_PhysicalMemory.CreationClassName
- CIM_PhysicalMemory.DataWidth
- CIM_PhysicalMemory.Description
- CIM_PhysicalMemory.FormFactor
- CIM_PhysicalMemory.HotSwappable
- CIM_PhysicalMemory.InstallDate
- CIM_PhysicalMemory.InterleavePosition
- CIM_PhysicalMemory.Manufacturer
- CIM_PhysicalMemory.MemoryType
- CIM_PhysicalMemory.Model
- CIM_PhysicalMemory.Name
- CIM_PhysicalMemory.OtherIdentifyingInfo
- CIM_PhysicalMemory.PartNumber
- CIM_PhysicalMemory.PositionInRow
- CIM_PhysicalMemory.PoweredOn
- CIM_PhysicalMemory.Removable
- CIM_PhysicalMemory.Replaceable
- CIM_PhysicalMemory.SerialNumber
- CIM_PhysicalMemory.SKU
- CIM_PhysicalMemory.Speed
- CIM_PhysicalMemory.Status
- CIM_PhysicalMemory.Tag
- CIM_PhysicalMemory.TotalWidth
- CIM_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b85a4e80588b98625f166f76c09aff9d52b114adcee4507eb7b81957746d88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080485"
---
# <a name="cim_physicalmemory-class"></a>Classe \_ CiM PhysicalMemory

La **classe \_ CIM PhysicalMemory** rappresenta dispositivi di memoria di basso livello, ad esempio SIMMS, DIMM, chip di memoria non elaborata e così via.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract, UUID("{FAF76B7B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMemory : CIM_Chip
{
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint16   MemoryType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  string   Version;
};
```

## <a name="members"></a>Members

La **classe \_ CIM PhysicalMemory** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CIM PhysicalMemory** ha queste proprietà.

<dl> <dt>

**BankLabel**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.4")
</dt> </dl>

Banca con etichetta in cui si trova la memoria. Ad esempio, "Bank 0" o "Bank A".

</dd> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Capacità totale della memoria fisica, in byte.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome della classe o sottoclasse utilizzata nella creazione di un'istanza di . Se usata con altre proprietà chiave della classe , questa proprietà consente l'identificazione univoca di tutte le istanze della classe e delle relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**DataWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Larghezza dei dati della memoria fisica, in bit. Una larghezza dei dati pari a 0 (zero) e una larghezza totale di 8 indica che la memoria viene utilizzata esclusivamente per fornire bit di correzione degli errori.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**FormFactor**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.6")
</dt> </dl>

Fattore di forma dell'implementazione per il chip. Ad esempio, è possibile specificare valori come SIMM, TSOP o PGA.

Questa proprietà viene ereditata dal [**\_ chip CIM.**](cim-chip.md)

<dt>

0
</dt> <dd>

Sconosciuto

</dd> <dt>

1
</dt> <dd>

Altro

</dd> <dt>

2
</dt> <dd>

Sip

</dd> <dt>

3
</dt> <dd>

DIP

</dd> <dt>

4
</dt> <dd>

ZIP

</dd> <dt>

5
</dt> <dd>

SOJ

</dd> <dt>

6
</dt> <dd>

Proprietario

</dd> <dt>

7
</dt> <dd>

Simm

</dd> <dt>

8
</dt> <dd>

Dimm

</dd> <dt>

9
</dt> <dd>

Tsop

</dd> <dt>

10
</dt> <dd>

Pga

</dd> <dt>

11
</dt> <dd>

Rimm

</dd> <dt>

12
</dt> <dd>

Sodimm

</dd> <dt>

13
</dt> <dd>

SRIMM

</dd> <dt>

14
</dt> <dd>

Smd

</dd> <dt>

15
</dt> <dd>

SSMP

</dd> <dt>

16
</dt> <dd>

QFP

</dd> <dt>

17
</dt> <dd>

TQFP

</dd> <dt>

18
</dt> <dd>

Soic

</dd> <dt>

19
</dt> <dd>

Lcc

</dd> <dt>

20
</dt> <dd>

Plcc

</dd> <dt>

21
</dt> <dd>

Bga

</dd> <dt>

22
</dt> <dd>

FPBGA

</dd> <dt>

23
</dt> <dd>

LGA

</dd> </dl>

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** il pacchetto può essere scambiato a caldo. Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un pacchetto fisicamente diverso (ma equivalente) mentre il pacchetto contenitore è attivato. Ad esempio, un componente ventola può essere progettato per lo scambio a caldo. Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

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

**InterleavePosition**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device Mapped Addresses \| 001.7")
</dt> </dl>

Posizione della memoria fisica in un interleave. Il valore 0 indica che non è interleaved, 1 indica la prima posizione, 2 indica la seconda posizione e così via. Ad esempio, in un interleave 2:1, il valore 1 indica che la memoria si trova nella posizione pari.

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome dell'organizzazione responsabile della produzione dell'elemento fisico. Per altre informazioni, vedere la **proprietà Vendor** di [**CIM \_ Product.**](cim-product.md)

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**MemoryType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.9")
</dt> </dl>

Tipo di memoria fisica.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

**DRAM** (2)


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

**DRAM sincrona** (3)


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

**DRAM cache** (4)


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

**EDO** (5)


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

**EDRAM** (6)


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

**VRAM** (7)


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

**SRAM** (8)


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

**RAM** (9)


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

**ROM** (10)


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

**Flash** (11)


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

**EEPROM** (12)


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

**FEPROM** (13)


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

**EPROM** (14)


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

**CDRAM** (15)


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

**3DRAM** (16)


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

**SDRAM** (17)


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

**SGRAM** (18)


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

**RDRAM** (19)


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

**DDR** (20)


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

**DDR2** (21)


</dt> <dd></dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

**DDR2 FB-DIMM** (22)


</dt> <dd></dd> </dl>

</dd> <dt>

**Modello**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nome con cui l'elemento fisico è noto a livello generale.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, questa proprietà può essere sottoposta a override come proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati aggiuntivi, oltre alle informazioni sui tag degli asset, che possono essere usati per identificare un elemento fisico. Un esempio è dato da dati di codice a barre associati a un elemento, che ha anche un tag di asset. Si noti che se sono disponibili solo dati di codice a barre e sono univoci e possono essere usati come chiave dell'elemento, questa proprietà sarà Null e i dati del codice a barre verrebbero usati come chiave di classe nella **proprietà Tag.** Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Numero di parte assegnato dall'organizzazione che ha prodotto o prodotto l'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**PositionInRow**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device Mapped Addresses \| 001.6")
</dt> </dl>

Posizione della memoria fisica in una riga. Ad esempio, se sono necessari due dispositivi di memoria a 8 bit per formare una riga a 16 bit, il valore 2 indica che la memoria è il secondo dispositivo. Il valore 0 non è valido per questa proprietà.

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** l'elemento fisico è acceso.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Rimovibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** questo elemento è progettato per essere prelevato e estratto dal contenitore fisico in cui viene normalmente trovato, senza compromettere la funzione del pacchetto complessivo. Un pacchetto viene considerato rimovibile anche se l'alimentazione deve essere spenta per eseguire la rimozione. Se l'alimentazione può essere accensione e il pacchetto è stato rimosso, l'elemento è rimovibile e può essere scambiato a caldo. Ad esempio, un chip del processore non aggiornabile è rimovibile.

Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**Sostituibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** è possibile sostituire l'elemento con un elemento fisicamente diverso. Ad esempio, alcuni sistemi di computer consentono l'aggiornamento del chip del processore principale a una classificazione di clock superiore. In questo caso, il processore è detto sostituibile. Tutti i componenti rimovibili sono intrinsecamente sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Numero allocato dal produttore usato per identificare l'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Numero di unità di mantenimento delle scorte per l'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Velocità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanosecondi")
</dt> </dl>

Velocità della memoria fisica, in nanosecondi.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Stato corrente dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

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

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Stringa arbitraria che identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento. Questa proprietà può contenere informazioni, ad esempio il tag asset o i dati del numero di serie. La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata molto in alto nella gerarchia di oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dal posizionamento fisico in (o in) archivi, schede e così via. Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere prelevato dal pacchetto contenitore (ambito) e temporaneamente inutilizzato. L'oggetto continua a esistere e può anche essere inserito in un contenitore di ambito diverso. La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dalla gerarchia di posizionamento o orientata alla posizione.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**TotalWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Larghezza totale, in bit, della memoria fisica, inclusi i bit di controllo o di correzione degli errori. Se non sono presenti bit di correzione degli errori, il valore di questa proprietà deve corrispondere a quello specificato per la **proprietà DataWidth.**

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Versione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ CIM PhysicalMemory** è derivata dal [**\_ chip CIM**](cim-chip.md).

WMI non implementa questa classe. Per le classi WMI derivate **da CIM \_ PhysicalMemory,** vedere [Classi Win32.](win32-provider.md)

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[**CIM \_ Chip**](cim-chip.md)
</dt> </dl>

 

