---
description: Rappresenta una scheda di base, nota anche come scheda madre o scheda di sistema.
ms.assetid: 04ac7522-8b99-4ffc-9f7d-d1225f55a862
ms.tgt_platform: multiple
title: Win32_BaseBoard classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseBoard
- Win32_BaseBoard.IsCompatible
- Win32_BaseBoard.Caption
- Win32_BaseBoard.ConfigOptions
- Win32_BaseBoard.CreationClassName
- Win32_BaseBoard.Depth
- Win32_BaseBoard.Description
- Win32_BaseBoard.Height
- Win32_BaseBoard.HostingBoard
- Win32_BaseBoard.HotSwappable
- Win32_BaseBoard.InstallDate
- Win32_BaseBoard.Manufacturer
- Win32_BaseBoard.Model
- Win32_BaseBoard.Name
- Win32_BaseBoard.OtherIdentifyingInfo
- Win32_BaseBoard.PartNumber
- Win32_BaseBoard.PoweredOn
- Win32_BaseBoard.Product
- Win32_BaseBoard.Removable
- Win32_BaseBoard.Replaceable
- Win32_BaseBoard.RequirementsDescription
- Win32_BaseBoard.RequiresDaughterBoard
- Win32_BaseBoard.SerialNumber
- Win32_BaseBoard.SKU
- Win32_BaseBoard.SlotLayout
- Win32_BaseBoard.SpecialRequirements
- Win32_BaseBoard.Status
- Win32_BaseBoard.Tag
- Win32_BaseBoard.Version
- Win32_BaseBoard.Weight
- Win32_BaseBoard.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac22dc01864d74902c666529bd40344f65eacfb1ad2515552e1cd46fbf65b9e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546517"
---
# <a name="win32_baseboard-class"></a>Classe BaseBoard Win32 \_

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ Win32 BaseBoard** rappresenta una scheda di base, nota anche come scheda madre o scheda di sistema.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B95-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_BaseBoard : CIM_Card
{
  string   Caption;
  string   ConfigOptions[];
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HostingBoard;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   Product;
  boolean  Removable;
  boolean  Replaceable;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SerialNumber;
  string   SKU;
  string   SlotLayout;
  boolean  SpecialRequirements;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Members

La **classe \_ BaseBoard Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ BaseBoard Win32** include questi metodi.



| Metodo           | Descrizione                 |
|:-----------------|:----------------------------|
| **IsCompatible** | Non implementato.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ BaseBoard Win32** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto una stringa di una riga.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Opzioni di configurazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stringhe delle opzioni di configurazione di tipo SMBIOS \| 12") \|
</dt> </dl>

Matrice che rappresenta la configurazione dei ponticelli e dei commutatori posizionati sulla baseboard.

Esempio: "JP2: 1-2 Cache Size is 256K, 2-3 Cache Size is 512K, SW1-1: Close to Disable On Board Video"

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata nella creazione di un'istanza di . Se usata con le altre proprietà chiave della classe , la proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Livello nidificazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")
</dt> </dl>

Profondità del pacchetto fisico in pollici.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Altezza**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")
</dt> </dl>

Altezza del pacchetto fisico in pollici.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> <dt>

**HostingBoard**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** la scheda è una scheda madre o una scheda base in uno chassis.

Questa proprietà viene ereditata dalla [**scheda CIM \_**](cim-card.md).

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** il pacchetto può essere scambiato a caldo. Un pacchetto fisico può essere scambiato a caldo se è possibile sostituire l'elemento con un elemento fisicamente diverso ma equivalente, mentre il pacchetto contenitore ha alimentazione applicata, mentre è on. Ad esempio, un pacchetto di unità disco inserito usando connettori SCA è rimovibile e può essere scambiato a caldo. Tutti i pacchetti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

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

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome dell'organizzazione responsabile della produzione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Modello**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nome con cui è noto l'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. In caso di sottoclasse, la proprietà può essere sottoposta a override per essere una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Acquisisce dati aggiuntivi, oltre alle informazioni sui tag di asset, che possono essere usati per identificare un elemento fisico. Un esempio sono i dati del codice a barre associati a un elemento che include anche un tag di asset. Si noti che se sono disponibili solo i dati del codice a barre e univoci o possono essere usati come chiave dell'elemento, il valore della proprietà sarà **NULL** e i dati del codice a barre verranno usati come chiave di classe, nella proprietà tag .

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

Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.

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

**Prodotto**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 2 \| Product")
</dt> </dl>

Numero della parte della scheda di base definita dal produttore.

</dd> <dt>

**Rimovibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** un pacchetto è rimovibile. Un pacchetto fisico è rimovibile se è progettato per essere prelevato e estratto dal contenitore fisico in cui si trova normalmente senza compromettere la funzione della creazione complessiva dei pacchetti. Un pacchetto può comunque essere rimovibile se l'alimentazione deve essere disattivata per eseguire la rimozione. Se l'alimentazione può essere impostata su ON e il pacchetto è stato rimosso, l'elemento è rimovibile e può essere scambiato a caldo. Ad esempio, una batteria aggiuntiva in un portatile è rimovibile, così come un pacchetto di unità disco inserito usando connettori SCA. Tuttavia, quest'ultimo può anche essere scambiato a caldo. Il display di un portatile non è rimovibile, né è un alimentatore non rimovibile. La rimozione di questi componenti influisce sulla funzione del pacchetto complessivo o è impossibile a causa della stretta integrazione del pacchetto.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> <dt>

**Sostituibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** un pacchetto è sostituibile. Un pacchetto fisico è sostituibile se è possibile sostituire (FRU o aggiornare) l'elemento con uno fisicamente diverso. Ad esempio, alcuni sistemi di computer consentono l'aggiornamento del chip del processore principale a una classificazione di clock superiore. In questo caso, il processore è detto sostituibile. Un altro esempio è un pacchetto di alimentazione montato su guide scorrevoli. Tutti i pacchetti rimovibili sono intrinsecamente sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> <dt>

**RequirementsDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**SCHEDA CIM \_**](cim-card.md).**SpecialRequirements**")
</dt> </dl>

Stringa in formato libero che descrive il modo in cui questa scheda è fisicamente univoca rispetto ad altre schede. La proprietà ha significato solo quando la proprietà booleana **corrispondente SpecialRequirements** è impostata su **TRUE.**

Questa proprietà viene ereditata dalla [**scheda CIM. \_**](cim-card.md)

</dd> <dt>

**RequiresDaughterBoard**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** è necessario almeno una scheda ausiliaria o una scheda ausiliaria per funzionare correttamente.

Questa proprietà viene ereditata dalla [**scheda CIM. \_**](cim-card.md)

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

**SlotLayout**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che descrive la posizione dello slot, l'utilizzo tipico, le restrizioni, la spaziatura dei singoli slot o qualsiasi altra informazione pertinente per gli slot in una scheda.

Questa proprietà viene ereditata dalla [**scheda CIM. \_**](cim-card.md)

</dd> <dt>

**SpecialRequirements**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**SCHEDA CIM \_**](cim-card.md).**RequirementsDescription**")
</dt> </dl>

Se **TRUE,** questa scheda è fisicamente univoca da altre schede dello stesso tipo e pertanto richiede uno slot speciale. Ad esempio, una scheda a larghezza doppia richiede due slot. Un altro esempio è quello in cui una determinata scheda può essere usata per la stessa funzione generale di altre schede, ma richiede uno slot speciale (ad esempio, molto lungo), mentre le altre schede possono essere inserite in qualsiasi slot disponibile. Se impostato su **TRUE,** la proprietà corrispondente **RequirementsDescription** deve specificare la natura dell'univocità o dello scopo della scheda.

Questa proprietà viene ereditata dalla [**scheda CIM. \_**](cim-card.md)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati nonoperational includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono online, ma l'elemento gestito non è "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

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

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Identificatore univoco della baseboard del sistema.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

Esempio: "Base Board"

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

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("libbre")
</dt> </dl>

Peso del pacchetto fisico in libbre.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage.**](cim-physicalelement.md)

</dd> <dt>

**Larghezza**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")
</dt> </dl>

Larghezza del pacchetto fisico in pollici.

Questa proprietà viene ereditata da [**CIM \_ PhysicalPackage.**](cim-physicalelement.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ BaseBoard Win32** deriva dalla [**scheda CIM \_**](cim-card.md) che deriva da [**CIM \_ PhysicalPackage.**](cim-physicalelement.md)

## <a name="examples"></a>Esempio

[L'esempio List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) Perl restituisce informazioni sulla baseboard del computer.

L'esempio di PowerShell [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) restituisce informazioni sulla baseboard del computer.

Nell'esempio di VBScript seguente vengono restituite anche informazioni sulla baseboard del computer.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BaseBoard") 
 
For Each objItem in colItems 
    For Each strOption in objItem.ConfigOptions 
        Wscript.Echo "Configuration Option: " & strOption 
    Next 
    Wscript.Echo "Depth: " & objItem.Depth 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Height: " & objItem.Height 
    Wscript.Echo "Hosting Board: " & objItem.HostingBoard 
    Wscript.Echo "Hot Swappable: " & objItem.HotSwappable 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "Model: " & objItem.Model 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Other Identifying Information: " & _ 
        objItem.OtherIdentifyingInfo 
    Wscript.Echo "Part Number: " & objItem.PartNumber 
    Wscript.Echo "Powered-On: " & objItem.PoweredOn 
    Wscript.Echo "Product: " & objItem.Product 
    Wscript.Echo "Removable: " & objItem.Removable 
    Wscript.Echo "Replaceable: " & objItem.Replaceable 
    Wscript.Echo "Requirements Description: " & objItem.RequirementsDescription 
    Wscript.Echo "Requires Daughterboard: " & objItem.RequiresDaughterBoard 
    Wscript.Echo "Serial Number: " & objItem.SerialNumber 
    Wscript.Echo "SKU: " & objItem.SKU 
    Wscript.Echo "Slot Layout: " & objItem.SlotLayout 
    Wscript.Echo "Special Requirements: " & objItem.SpecialRequirements 
    Wscript.Echo "Tag: " & objItem.Tag 
    Wscript.Echo "Version: " & objItem.Version 
    Wscript.Echo "Weight: " & objItem.Weight 
    Wscript.Echo "Width: " & objItem.Width 
Next 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Scheda \_ CIM**](cim-card.md)
</dt> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

