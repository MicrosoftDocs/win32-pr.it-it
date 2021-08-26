---
description: La classe SLOT CIM \_ rappresenta i connettori in cui vengono inseriti i pacchetti.
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: CIM_Slot classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 910fb4a3dcd5d3d95ef524d838781bad8331d33d71fc0af8ebd358ac9dd9588e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919461"
---
# <a name="cim_slot-class"></a>Classe slot CIM \_

La **classe \_ SLOT CIM** rappresenta i connettori in cui vengono inseriti i pacchetti. Ad esempio, un pacchetto fisico che è un'unità disco può essere inserito in uno slot SCA oppure una scheda (una sottoclasse [di CIM \_ PhysicalPackage](cim-physicalpackage.md)) può essere inserita in uno slot di espansione a 16, 32 o 64 bit in una scheda di hosting. Gli slot PCI o PCMCIA di tipo III sono esempi di questi ultimi.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a>Members

La **classe \_ SLOT CIM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ slot CIM** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ConnectorPinout**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che descrive la configurazione del pin e l'uso del segnale di un connettore fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).

</dd> <dt>

**Connectortype**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DmTF \| System Slot \| 004.2")
</dt> </dl>

Tipo di connettore fisico. Viene specificata una matrice per consentire la descrizione delle combinazioni di informazioni sul connettore. Ad esempio, una voce di matrice può specificare RS-232, un'altra DB-25 e una terza può definire il connettore come "Male".

Questa proprietà viene ereditata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).

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

Male

</dd> <dt>

3
</dt> <dd>

Female

</dd> <dt>

4
</dt> <dd>

Schermato

</dd> <dt>

5
</dt> <dd>

Unshielded

</dd> <dt>

6
</dt> <dd>

SCSI (A) Ad alta densità (50 pin)

</dd> <dt>

7
</dt> <dd>

SCSI (A) Bassa densità (50 pin)

</dd> <dt>

8
</dt> <dd>

SCSI (P) Ad alta densità (68 pin)

</dd> <dt>

9
</dt> <dd>

SCSI SCA-I (80 pin)

</dd> <dt>

10
</dt> <dd>

SCSI SCA-II (80 pin)

</dd> <dt>

11
</dt> <dd>

ScSI Fibre Channel (DB-9, Rame)

</dd> <dt>

12
</dt> <dd>

SCSI Fibre Channel (Fibre)

</dd> <dt>

13
</dt> <dd>

SCSI Fibre Channel SCA-II (40 pin)

</dd> <dt>

14
</dt> <dd>

SCSI Fibre Channel SCA-II (20 pin)

</dd> <dt>

15
</dt> <dd>

SCSI Fibre Channel BNC

</dd> <dt>

16
</dt> <dd>

ATA 3-1/2 pollici (40 pin)

</dd> <dt>

17
</dt> <dd>

ATA 2-1/2 pollice (44 pin)

</dd> <dt>

18
</dt> <dd>

ATA-2

</dd> <dt>

19
</dt> <dd>

ATA-3

</dd> <dt>

20
</dt> <dd>

ATA/66

</dd> <dt>

21
</dt> <dd>

DB-9

</dd> <dt>

22
</dt> <dd>

DB-15

</dd> <dt>

23
</dt> <dd>

DB-25

</dd> <dt>

24
</dt> <dd>

DB-36

</dd> <dt>

25
</dt> <dd>

RS-232C

</dd> <dt>

26
</dt> <dd>

RS-422

</dd> <dt>

27
</dt> <dd>

RS-423

</dd> <dt>

28
</dt> <dd>

RS-485

</dd> <dt>

29
</dt> <dd>

RS-449

</dd> <dt>

30
</dt> <dd>

V.35

</dd> <dt>

31
</dt> <dd>

X.21

</dd> <dt>

32
</dt> <dd>

IEEE-488

</dd> <dt>

33
</dt> <dd>

Aui

</dd> <dt>

34
</dt> <dd>

UTP Categoria 3

</dd> <dt>

35
</dt> <dd>

UTP Categoria 4

</dd> <dt>

36
</dt> <dd>

UTP Categoria 5

</dd> <dt>

37
</dt> <dd>

Bnc

</dd> <dt>

38
</dt> <dd>

RJ11

</dd> <dt>

39
</dt> <dd>

RJ45

</dd> <dt>

40
</dt> <dd>

Fiber MIC

</dd> <dt>

41
</dt> <dd>

Apple AUI

</dd> <dt>

42
</dt> <dd>

Apple GeoPort

</dd> <dt>

43
</dt> <dd>

PCI

</dd> <dt>

44
</dt> <dd>

ISA

</dd> <dt>

45
</dt> <dd>

Eisa

</dd> <dt>

46
</dt> <dd>

Vesa

</dd> <dt>

47
</dt> <dd>

Pcmcia

</dd> <dt>

48
</dt> <dd>

PCMCIA Di tipo I

</dd> <dt>

49
</dt> <dd>

PCMCIA Di tipo II

</dd> <dt>

50
</dt> <dd>

PCMCIA Di tipo III

</dd> <dt>

51
</dt> <dd>

Porta ZV

</dd> <dt>

52
</dt> <dd>

Cardbus

</dd> <dt>

53
</dt> <dd>

USB

</dd> <dt>

54
</dt> <dd>

IEEE 1394

</dd> <dt>

55
</dt> <dd>

HIPPI

</dd> <dt>

56
</dt> <dd>

HSSDC (6 pin)

</dd> <dt>

57
</dt> <dd>

Gbic

</dd> <dt>

58
</dt> <dd>

DIN

</dd> <dt>

59
</dt> <dd>

Mini-DIN

</dd> <dt>

60
</dt> <dd>

Micro-DIN

</dd> <dt>

61
</dt> <dd>

PS/2

</dd> <dt>

62
</dt> <dd>

Infrarossi

</dd> <dt>

63
</dt> <dd>

HP-PF

</dd> <dt>

64
</dt> <dd>

Access.bus

</dd> <dt>

65
</dt> <dd>

NuBus

</dd> <dt>

66
</dt> <dd>

Centronics

</dd> <dt>

67
</dt> <dd>

Mini-Centronics

</dd> <dt>

68
</dt> <dd>

Mini-Centronics Di tipo 14

</dd> <dt>

69
</dt> <dd>

Mini-Centronics tipo 20

</dd> <dt>

70
</dt> <dd>

Mini-Centronics tipo 26

</dd> <dt>

71
</dt> <dd>

Bus Mouse

</dd> <dt>

72
</dt> <dd>

Adb

</dd> <dt>

73
</dt> <dd>

Agp

</dd> <dt>

74
</dt> <dd>

VME Bus

</dd> <dt>

75
</dt> <dd>

VME64

</dd> <dt>

76
</dt> <dd>

Proprietario

</dd> <dt>

77
</dt> <dd>

Slot della scheda processore proprietario

</dd> <dt>

78
</dt> <dd>

Slot di schede di memoria proprietarie

</dd> <dt>

79
</dt> <dd>

Slot del riser di I/O proprietario

</dd> <dt>

80
</dt> <dd>

PCI-66MHZ

</dd> <dt>

81
</dt> <dd>

AGP2X

</dd> <dt>

82
</dt> <dd>

AGP4X

</dd> <dt>

83
</dt> <dd>

PC-98

</dd> <dt>

84
</dt> <dd>

PC-98-Hireso

</dd> <dt>

85
</dt> <dd>

PC-H98

</dd> <dt>

86
</dt> <dd>

PC-98Nota

</dd> <dt>

87
</dt> <dd>

PC-98Full

</dd> <dt>

88
</dt> <dd>

SSA SCSI

</dd> <dt>

89
</dt> <dd>

Circolare

</dd> <dt>

90
</dt> <dd>

On Board IDE Connector

</dd> <dt>

91
</dt> <dd>

Connettore Floppy su scheda

</dd> <dt>

92
</dt> <dd>

9 Pin Dual Inline

</dd> <dt>

93
</dt> <dd>

Doppio inline a 25 pin

</dd> <dt>

94
</dt> <dd>

Doppio inline a 50 pin

</dd> <dt>

95
</dt> <dd>

Doppio inline a 68 pin

</dd> <dt>

96
</dt> <dd>

On Board Sound Connector

</dd> <dt>

97
</dt> <dd>

Mini-jack

</dd> <dt>

98
</dt> <dd>

PCI-X

</dd> <dt>

99
</dt> <dd>

Sbus IEEE 1396-1993 a 32 bit

</dd> <dt>

100
</dt> <dd>

Sbus IEEE 1396-1993 a 64 bit

</dd> <dt>

101
</dt> <dd>

Contratto del cliente Microsoft

</dd> <dt>

102
</dt> <dd>

GIO

</dd> <dt>

103
</dt> <dd>

XIO

</dd> <dt>

104
</dt> <dd>

Hio

</dd> <dt>

105
</dt> <dd>

NGIO

</dd> <dt>

106
</dt> <dd>

PMC

</dd> <dt>

107
</dt> <dd>

MTRJ

</dd> <dt>

108
</dt> <dd>

VF-45

</dd> <dt>

109
</dt> <dd>

I/O futuro

</dd> <dt>

110
</dt> <dd>

SC

</dd> <dt>

111
</dt> <dd>

SG

</dd> <dt>

112
</dt> <dd>

Electrical

</dd> <dt>

113
</dt> <dd>

Ottico

</dd> <dt>

114
</dt> <dd>

Barra multifunzione

</dd> <dt>

115
</dt> <dd>

Glm

</dd> <dt>

116
</dt> <dd>

1x9

</dd> <dt>

117
</dt> <dd>

Mini SG

</dd> <dt>

118
</dt> <dd>

LC

</dd> <dt>

119
</dt> <dd>

HSSC

</dd> <dt>

120
</dt> <dd>

VHDCI schermato (68 pin)

</dd> <dt>

121
</dt> <dd>

InfiniBand

</dd> </dl>

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

**HeightAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")
</dt> </dl>

Altezza massima, in pollici, di una scheda adattatore che può essere inserita nello slot.

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

**LengthAllowed**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")
</dt> </dl>

Lunghezza massima, in pollici, di una scheda di scheda che può essere inserita nello slot.

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Organizzazione che ha prodotto l'elemento fisico. Per altre informazioni, vedere la **proprietà Vendor** di [**CIM \_ Product.**](cim-product.md)

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**MaxDataWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Slot \| 004.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Larghezza massima del bus, in bit, delle schede di scheda che possono essere inserite nello slot.

<dt>

<span id="8"></span>

**8** (0)


</dt> <dd></dd> <dt>

<span id="16"></span>

**16** (1)


</dt> <dd></dd> <dt>

<span id="32"></span>

**32** (2)


</dt> <dd></dd> <dt>

<span id="64"></span>

**64** (3)


</dt> <dd></dd> <dt>

<span id="128"></span>

**128** (4)


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

**Number**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di slot fisico, che può essere utilizzato come indice in una tabella di slot di sistema, per determinare se lo slot è occupato fisicamente.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati aggiuntivi, oltre alle informazioni sui tag degli asset, che possono essere usati per identificare un elemento fisico. Un esempio è dato da dati di codice a barre associati a un elemento, che ha anche un tag di asset. Si noti che se sono disponibili solo dati di codice a barre e sono univoci e possono essere usati come chiave dell'elemento, questa proprietà sarà Null e i dati del codice a barre verrebbero usati come chiave di classe nella **proprietà Tag.**

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

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

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** l'elemento fisico è acceso.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**PurposeDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Slot CIM \_**.**SpecialPurpose**")
</dt> </dl>

Stringa in formato libero che descrive come questo slot è fisicamente univoco e che può contenere tipi speciali di hardware. Questa proprietà ha significato solo quando la proprietà **Boolean SpecialPurpose** corrispondente è impostata su **TRUE.**

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

**SpecialPurpose**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Slot CIM \_**.**PurposeDescription**")
</dt> </dl>

Se **TRUE,** lo slot è fisicamente univoco e può contenere tipi speciali di hardware, ad esempio uno slot del processore di grafica. Se **TRUE,** la **proprietà PurposeDescription** deve specificare il modo in cui lo slot è univoco o lo scopo dello slot.

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

**SupportsHotPlug**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** lo slot supporta il collegamento a caldo delle schede di scheda.

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Stringa arbitraria che identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento. Questa proprietà può contenere informazioni, ad esempio i dati relativi al tag di asset o al numero di serie. La chiave [**per CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata molto in alto nella gerarchia di oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dal posizionamento fisico in (o in) archivi, adattatori e così via. Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere prelevato dal pacchetto contenitore (ambito) e temporaneamente inutilizzato. L'oggetto continua a esistere e può anche essere inserito in un contenitore di ambito diverso. La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dalla gerarchia di posizionamento o orientata alla posizione.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**ThermalRating**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DmTF \| System Slot \| 004.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")
</dt> </dl>

Dissipazione termica massima dello slot, in milliwatt.

</dd> <dt>

**VccMixedVoltageSupport**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DmTF \| System Slot \| 004.9")
</dt> </dl>

Tensione Vcc supportata dallo slot.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3.3V** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5V** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Versione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**VppMixedVoltageSupport**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DmTF \| System Slot \| 004.10")
</dt> </dl>

Tensione Vpp supportata dallo slot.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3.3V** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5V** (3)


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

**12V** (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ slot CIM** è derivata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).

WMI non implementa questa classe. Per le classi WMI derivate **dallo \_ slot CIM,** vedere [Classi Win32](win32-provider.md).

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[**CIM \_ PhysicalConnector**](cim-physicalconnector.md)
</dt> </dl>

 

