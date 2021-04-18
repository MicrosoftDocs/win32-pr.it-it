---
description: La \_ classe CIM PhysicalLink rappresenta il cablaggio di elementi fisici.
ms.assetid: 0d96cb7f-ca50-4eb2-b8d4-e749bbe67ad7
ms.tgt_platform: multiple
title: Classe CIM_PhysicalLink
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalLink
- CIM_PhysicalLink.Caption
- CIM_PhysicalLink.CreationClassName
- CIM_PhysicalLink.Description
- CIM_PhysicalLink.InstallDate
- CIM_PhysicalLink.Length
- CIM_PhysicalLink.Manufacturer
- CIM_PhysicalLink.MaxLength
- CIM_PhysicalLink.MediaType
- CIM_PhysicalLink.Model
- CIM_PhysicalLink.Name
- CIM_PhysicalLink.OtherIdentifyingInfo
- CIM_PhysicalLink.PartNumber
- CIM_PhysicalLink.PoweredOn
- CIM_PhysicalLink.SerialNumber
- CIM_PhysicalLink.SKU
- CIM_PhysicalLink.Status
- CIM_PhysicalLink.Tag
- CIM_PhysicalLink.Version
- CIM_PhysicalLink.Wired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 659e73d9f5331d5c6648af00e147797dc6424130
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524010"
---
# <a name="cim_physicallink-class"></a>CIM \_ PhysicalLink (classe)

La classe **CIM \_ PhysicalLink** rappresenta il cablaggio di elementi fisici. Ad esempio, i cavi seriale o Ethernet e i collegamenti infrarossi sarebbero sottoclassi (se sono definite proprietà o associazioni aggiuntive) o istanze di **CIM \_ PhysicalLink**. In genere, i numerosi cavi fisici in un pacchetto fisico o in una rete non sono modellati. Tuttavia, quando i cavi o i collegamenti sono componenti critici o asset con tag della società, è possibile creare un'istanza degli oggetti utilizzando questa classe o una delle relative classi discendenti.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B82-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalLink : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  real64   Length;
  string   Manufacturer;
  real64   MaxLength;
  uint16   MediaType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  Wired;
};
```

## <a name="members"></a>Members

La classe **CIM \_ PhysicalLink** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ PhysicalLink** dispone di queste proprietà.

<dl> <dt>

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

**Length**
</dt> <dd> <dl> <dt>

Tipo di dati: **real64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("piedi")
</dt> </dl>

Lunghezza corrente del collegamento fisico, in metri. Per alcune connessioni, soprattutto per le tecnologie wireless, questa proprietà potrebbe non essere applicabile e deve essere lasciata non inizializzata.

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

**MaxLength**
</dt> <dd> <dl> <dt>

Tipo di dati: **real64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("piedi")
</dt> </dl>

Lunghezza massima del collegamento fisico in piedi.

</dd> <dt>

**MediaType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di supporti attraverso i quali passano i segnali di trasmissione. I supporti di rete comuni includono cavi bidirezionali, coassiali e a fibra ottica.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Cat1"></span><span id="cat1"></span><span id="CAT1"></span>

**CAT1** (2)


</dt> <dd></dd> <dt>

<span id="Cat2"></span><span id="cat2"></span><span id="CAT2"></span>

**CAT2** (3)


</dt> <dd></dd> <dt>

<span id="Cat3"></span><span id="cat3"></span><span id="CAT3"></span>

**Cat3** (4)


</dt> <dd></dd> <dt>

<span id="Cat4"></span><span id="cat4"></span><span id="CAT4"></span>

**Cat4** (5)


</dt> <dd></dd> <dt>

<span id="Cat5"></span><span id="cat5"></span><span id="CAT5"></span>

**CAT5** (6)


</dt> <dd></dd> <dt>

<span id="50-ohm_Coaxial"></span><span id="50-ohm_coaxial"></span><span id="50-OHM_COAXIAL"></span>

**50-ohm coassiale** (7)


</dt> <dd></dd> <dt>

<span id="75-ohm_Coaxial"></span><span id="75-ohm_coaxial"></span><span id="75-OHM_COAXIAL"></span>

**75-ohm coassiale** (8)


</dt> <dd></dd> <dt>

<span id="100-ohm_Coaxial"></span><span id="100-ohm_coaxial"></span><span id="100-OHM_COAXIAL"></span>

**100-ohm coassiale** (9)


</dt> <dd></dd> <dt>

<span id="Fiber-optic"></span><span id="fiber-optic"></span><span id="FIBER-OPTIC"></span>

**Fibra ottica** (10)


</dt> <dd></dd> <dt>

<span id="UTP"></span><span id="utp"></span>

**UTP** (11)


</dt> <dd></dd> <dt>

<span id="STP"></span><span id="stp"></span>

**STP** (12)


</dt> <dd></dd> <dt>

<span id="Ribbon_Cable"></span><span id="ribbon_cable"></span><span id="RIBBON_CABLE"></span>

**Cavo barra multifunzione** (13)


</dt> <dd></dd> <dt>

<span id="Twinaxial"></span><span id="twinaxial"></span><span id="TWINAXIAL"></span>

**Twinaxial** (14)


</dt> <dd></dd> <dt>

<span id="Optical_9um"></span><span id="optical_9um"></span><span id="OPTICAL_9UM"></span>

**9Um ottico** (15)


</dt> <dd></dd> <dt>

<span id="Optical_50um"></span><span id="optical_50um"></span><span id="OPTICAL_50UM"></span>

**50um ottico** (16)


</dt> <dd></dd> <dt>

<span id="Optical_62.5um"></span><span id="optical_62.5um"></span><span id="OPTICAL_62.5UM"></span>

**62,5 ottico um** (17)


</dt> <dd></dd> </dl>

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

Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico. Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset. Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** . Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

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

Se **true**, l'elemento fisico è acceso.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

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

Versione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Cablate**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, il collegamento fisico è un cavo. In caso contrario, si tratta di una connessione wireless.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ PhysicalLink** è derivata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

WMI non implementa questa classe.

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

[**\_PhysicalElement CIM**](cim-physicalelement.md)
</dt> </dl>

 

