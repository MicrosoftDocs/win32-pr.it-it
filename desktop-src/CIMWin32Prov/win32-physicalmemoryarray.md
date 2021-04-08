---
description: Win32 \_ PhysicalMemoryArray&\# 160; Classe WMI rappresenta i dettagli sulla memoria fisica del sistema del computer. Sono inclusi il numero di dispositivi di memoria, la capacità di memoria disponibile e il tipo di memoria&\# 8212, ad esempio la memoria di sistema o video.
ms.assetid: 6b553230-e1fc-46e6-b13a-02fbbd34034d
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemoryArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryArray
- Win32_PhysicalMemoryArray.IsCompatible
- Win32_PhysicalMemoryArray.Caption
- Win32_PhysicalMemoryArray.CreationClassName
- Win32_PhysicalMemoryArray.Depth
- Win32_PhysicalMemoryArray.Description
- Win32_PhysicalMemoryArray.Height
- Win32_PhysicalMemoryArray.HotSwappable
- Win32_PhysicalMemoryArray.InstallDate
- Win32_PhysicalMemoryArray.Location
- Win32_PhysicalMemoryArray.Manufacturer
- Win32_PhysicalMemoryArray.MaxCapacity
- Win32_PhysicalMemoryArray.MaxCapacityEx
- Win32_PhysicalMemoryArray.MemoryDevices
- Win32_PhysicalMemoryArray.MemoryErrorCorrection
- Win32_PhysicalMemoryArray.Model
- Win32_PhysicalMemoryArray.Name
- Win32_PhysicalMemoryArray.OtherIdentifyingInfo
- Win32_PhysicalMemoryArray.PartNumber
- Win32_PhysicalMemoryArray.PoweredOn
- Win32_PhysicalMemoryArray.Removable
- Win32_PhysicalMemoryArray.Replaceable
- Win32_PhysicalMemoryArray.SerialNumber
- Win32_PhysicalMemoryArray.SKU
- Win32_PhysicalMemoryArray.Status
- Win32_PhysicalMemoryArray.Tag
- Win32_PhysicalMemoryArray.Use
- Win32_PhysicalMemoryArray.Version
- Win32_PhysicalMemoryArray.Weight
- Win32_PhysicalMemoryArray.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8a585b0399f7015113b02ff48dbeb85956c9e62b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966360"
---
# <a name="win32_physicalmemoryarray-class"></a>Win32 \_ PhysicalMemoryArray (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PhysicalMemoryArray Win32** rappresenta i dettagli sulla memoria fisica del sistema del computer. Sono inclusi il numero di dispositivi di memoria, la capacità di memoria disponibile e il tipo di memoria, ad esempio memoria di sistema o video.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B99-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemoryArray : CIM_PhysicalPackage
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   Location;
  string   Manufacturer;
  uint32   MaxCapacity;
  uint64   MaxCapacityEx;
  uint16   MemoryDevices;
  uint16   MemoryErrorCorrection;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  uint16   Use;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ PhysicalMemoryArray** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ PhysicalMemoryArray** presenta questi metodi.



| Metodo           | Descrizione                 |
|:-----------------|:----------------------------|
| **IsCompatible** | Non implementato.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PhysicalMemoryArray** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto, ovvero una stringa a una riga.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza. Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Livello nidificazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("pollici")
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

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Altezza**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("pollici")
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

Se è **true**, un pacchetto fisico può essere scambiato a caldo (se è possibile sostituire l'elemento con un oggetto fisicamente diverso ma equivalente mentre al pacchetto che lo contiene è stata applicata la potenza, è "on"). Ad esempio, un pacchetto di unità disco inserito usando i connettori SCA è rimovibile e può essere scambiato a caldo. Tutti i pacchetti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Posizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 16 \| location")
</dt> </dl>

Posizione fisica della matrice di memoria.

Questo valore deriva dal membro **location** della struttura della **matrice di memoria fisica** nelle informazioni SMBIOS.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Riservato** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="System_board_or_motherboard"></span><span id="system_board_or_motherboard"></span><span id="SYSTEM_BOARD_OR_MOTHERBOARD"></span>

Scheda di **sistema o scheda madre** (3)


</dt> <dd></dd> <dt>

<span id="ISA_add-on_card"></span><span id="isa_add-on_card"></span><span id="ISA_ADD-ON_CARD"></span>

**Scheda componente aggiuntivo ISA** (4)


</dt> <dd></dd> <dt>

<span id="EISA_add-on_card"></span><span id="eisa_add-on_card"></span><span id="EISA_ADD-ON_CARD"></span>

**Scheda componente aggiuntivo EISA** (5)


</dt> <dd></dd> <dt>

<span id="PCI_add-on_card"></span><span id="pci_add-on_card"></span><span id="PCI_ADD-ON_CARD"></span>

**Scheda componente aggiuntivo PCI** (6)


</dt> <dd></dd> <dt>

<span id="MCA_add-on_card"></span><span id="mca_add-on_card"></span><span id="MCA_ADD-ON_CARD"></span>

**Scheda componente aggiuntivo MCA** (7)


</dt> <dd></dd> <dt>

<span id="PCMCIA_add-on_card"></span><span id="pcmcia_add-on_card"></span><span id="PCMCIA_ADD-ON_CARD"></span>

**Scheda componente aggiuntivo PCMCIA** (8)


</dt> <dd></dd> <dt>

<span id="Proprietary_add-on_card"></span><span id="proprietary_add-on_card"></span><span id="PROPRIETARY_ADD-ON_CARD"></span>

**Scheda componente aggiuntivo proprietaria** (9)


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

**Nubus** (10)


</dt> <dd></dd> <dt>

<span id="PC-98_C20_add-on_card"></span><span id="pc-98_c20_add-on_card"></span><span id="PC-98_C20_ADD-ON_CARD"></span>

**Scheda componente aggiuntivo PC-98/C20** (11)


</dt> <dd></dd> <dt>

<span id="PC-98_C24_add-on_card"></span><span id="pc-98_c24_add-on_card"></span><span id="PC-98_C24_ADD-ON_CARD"></span>

**Scheda componente aggiuntivo PC-98/C24** (12)


</dt> <dd></dd> <dt>

<span id="PC-98_E_add-on_card"></span><span id="pc-98_e_add-on_card"></span><span id="PC-98_E_ADD-ON_CARD"></span>

**Scheda componente aggiuntivo PC-98/E** (13)


</dt> <dd></dd> <dt>

<span id="PC-98_Local_bus_add-on_card"></span><span id="pc-98_local_bus_add-on_card"></span><span id="PC-98_LOCAL_BUS_ADD-ON_CARD"></span>

**Scheda aggiuntivo PC-98/bus locale** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome dell'organizzazione responsabile della creazione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**MaxCapacity**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 16 \| capacità massima")
</dt> </dl>

In alternativa, usare la proprietà **MaxCapacityEx** .

Questo valore deriva dal membro di **capacità massima** della struttura della **matrice di memoria fisica** nelle informazioni SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Dimensione massima della memoria (in byte) installabile per questa particolare matrice di memoria. Se la dimensione è sconosciuta, alla proprietà viene assegnato un valore pari a 0 (zero).

</dd> <dt>

**MaxCapacityEx**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 16 \| Extended maximum capacity"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Dimensione massima della memoria (in kilobyte) installabile per la matrice di memoria specifica. Se la dimensione è sconosciuta, alla proprietà viene assegnato un valore pari a 0 (zero).

Questo valore deriva dal membro di **capacità massima estesa** della struttura della **matrice di memoria fisica** nelle informazioni SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata.

</dd> <dt>

**MemoryDevices**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 16 \| numero di dispositivi di memoria")
</dt> </dl>

Numero di slot o socket fisici disponibili in questa matrice di memoria.

Questo valore deriva dal **numero di dispositivi di memoria** membro della struttura della **matrice di memoria fisica** nelle informazioni SMBIOS.

</dd> <dt>

**MemoryErrorCorrection**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 16 \| Memory Error Correction")
</dt> </dl>

Tipo di correzione di errore utilizzata dalla matrice di memoria.

Questo valore deriva dal membro di **correzione degli errori di memoria** della struttura della matrice di **memoria fisica** nelle informazioni SMBIOS.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Riservato** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (3)


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

**Parità** (4)


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

**Ecc a bit singolo** (5)


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

**Ecc a più bit** (6)


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

**CRC** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Modello**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
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

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico. Un esempio è costituito dai dati del codice a barre associati a un elemento che dispone anche di un tag asset. Si noti che se sono disponibili solo i dati del codice a barre ed è univoco o in grado di essere utilizzati come chiave di elemento, questa proprietà sarà **null** e i dati del codice a barre utilizzati come chiave della classe nella proprietà Tag.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**NumeroArticolo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
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

Se **true**, l'elemento fisico è acceso.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Rimovibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se il valore è **true**, un pacchetto fisico è rimovibile (se è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti). Un pacchetto può ancora essere rimovibile se l'alimentazione deve essere "off" per eseguire la rimozione. Se Power può essere "on" e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo. Ad esempio, una batteria aggiuntiva in un portatile è rimovibile, così come un pacchetto di unità disco inserito usando i connettori SCA. Tuttavia, quest'ultimo può essere scambiato a caldo. La visualizzazione di un computer portatile non è rimovibile, né è un alimentatore non ridondante. La rimozione di questi componenti influirà sulla funzione della creazione complessiva dei pacchetti o non è possibile grazie alla stretta integrazione del pacchetto.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**Sostituibili**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, questo componente multimediale fisico può essere sostituito con uno fisicamente diverso. Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate. In questo caso, il processore viene definito sostituibile. Un altro esempio è un pacchetto di alimentazione montato sulle guide scorrevoli. Tutti i pacchetti rimovibili sono intrinsecamente sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Numero allocato dal produttore utilizzato per identificare l'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Numero di unità di stockkeeping per l'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire diversi stati operativi e non operativi. Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro). Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service". Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

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

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Identificatore univoco della matrice di memoria fisica.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

Esempio: "matrice di memoria fisica 1"

</dd> <dt>

**Uso**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 16 \| use")
</dt> </dl>

Modalità di utilizzo della memoria nel computer.

Questo valore deriva dal membro **use** della struttura della **matrice di memoria fisica** nelle informazioni SMBIOS.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>

<span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**Memoria di sistema** (3)


</dt> <dd></dd> <dt>

<span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>

<span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Memoria video** (4)


</dt> <dd></dd> <dt>

<span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>

<span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Memoria flash** (5)


</dt> <dd></dd> <dt>

<span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>

<span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**RAM non volatile** (6)


</dt> <dd>

RAM non volatile

</dd> <dt>

<span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>

<span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Memoria cache** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Versione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("libbre")
</dt> </dl>

Peso del pacchetto fisico in sterline.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**Larghezza**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("pollici")
</dt> </dl>

Larghezza del pacchetto fisico in pollici.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ PhysicalMemoryArray** è derivata da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

## <a name="examples"></a>Esempio

L'esempio di PowerShell seguente recupera il numero di slot di memoria e la quantità di memoria installata in un computer di destinazione.


```PowerShell
$strComputer = Read-Host "Enter Computer Name"
 $colSlots = Get-WmiObject -Class "win32_PhysicalMemoryArray" -namespace "root\CIMV2" `
 -computerName $strComputer
 $colRAM = Get-WmiObject -Class "win32_PhysicalMemory" -namespace "root\CIMV2" `
 -computerName $strComputer

Foreach ($objSlot In $colSlots){
      "Total Number of DIMM Slots: " + $objSlot.MemoryDevices
 }
 Foreach ($objRAM In $colRAM) {
      "Memory Installed: " + $objRAM.DeviceLocator
      "Memory Size: " + ($objRAM.Capacity / 1GB) + " GB"
 }
```



Nell'esempio di codice VBScript seguente vengono restituite informazioni sulla memoria fisica installata in un computer.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_PhysicalMemoryArray") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Maximum Capacity: " & objItem.MaxCapacity 
    Wscript.Echo "Memory Devices: " & objItem.MemoryDevices 
    Wscript.Echo "Memory Error Correction: " & objItem.MemoryErrorCorrection 
Next 
```



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
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> <dt>

[**\_MemoryArrayLocation Win32**](win32-memoryarraylocation.md)
</dt> </dl>

 

 
