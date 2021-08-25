---
description: La classe \_ WMI Win32 OnBoardDevice rappresenta i dispositivi adattatore comuni incorporati nella scheda madre (scheda di sistema).
ms.assetid: 6fac38b4-7c04-4f64-997d-40bcbf767959
ms.tgt_platform: multiple
title: Win32_OnBoardDevice classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OnBoardDevice
- Win32_OnBoardDevice.Caption
- Win32_OnBoardDevice.CreationClassName
- Win32_OnBoardDevice.Description
- Win32_OnBoardDevice.DeviceType
- Win32_OnBoardDevice.Enabled
- Win32_OnBoardDevice.HotSwappable
- Win32_OnBoardDevice.InstallDate
- Win32_OnBoardDevice.Manufacturer
- Win32_OnBoardDevice.Model
- Win32_OnBoardDevice.Name
- Win32_OnBoardDevice.OtherIdentifyingInfo
- Win32_OnBoardDevice.PartNumber
- Win32_OnBoardDevice.PoweredOn
- Win32_OnBoardDevice.Removable
- Win32_OnBoardDevice.Replaceable
- Win32_OnBoardDevice.SerialNumber
- Win32_OnBoardDevice.SKU
- Win32_OnBoardDevice.Status
- Win32_OnBoardDevice.Tag
- Win32_OnBoardDevice.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a6ce10494c44f6eecd78e44d4bcf97d5e46da7d6281a5ef614a9e737acae68c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972591"
---
# <a name="win32_onboarddevice-class"></a>Classe OnBoardDevice Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) **\_ Win32 OnBoardDevice** rappresenta i dispositivi adattatore comuni incorporati nella scheda madre (scheda di sistema).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{AEECF151-D0EA-11d2-ABFC-00805F538618}"), AMENDMENT]
class Win32_OnBoardDevice : CIM_PhysicalComponent
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  uint16   DeviceType;
  boolean  Enabled;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
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
  string   Version;
};
```

## <a name="members"></a>Members

La **classe \_ OnBoardDevice Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ OnBoardDevice Win32** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata nella creazione di un'istanza di . Se usata con le altre proprietà chiave della classe , la proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 10 \| Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 10 \| Device Type n")
</dt> </dl>

Tipo di dispositivo rappresentato.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

**Video** (3)


</dt> <dd></dd> <dt>

<span id="SCSI_Controller"></span><span id="scsi_controller"></span><span id="SCSI_CONTROLLER"></span>

**Controller SCSI** (4)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (5)


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Token ring** (6)


</dt> <dd></dd> <dt>

<span id="Sound"></span><span id="sound"></span><span id="SOUND"></span>

**Audio** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 10 \| Device Status n")
</dt> </dl>

Se **TRUE,** il dispositivo su scheda è disponibile per l'uso.

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** un pacchetto fisico può essere scambiato a caldo (se è possibile sostituire l'elemento con un elemento fisicamente diverso ma equivalente mentre al pacchetto contenitore è applicata la potenza). Ad esempio, un pacchetto di unità disco inserito usando connettori SCA è rimovibile e può essere scambiato a caldo. Tutti i pacchetti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome dell'organizzazione responsabile della produzione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Modello**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
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

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. In caso di sottoclasse, è possibile eseguire l'override della proprietà come proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati aggiuntivi, oltre alle informazioni sui tag degli asset, che possono essere usati per identificare un elemento fisico. Un esempio è dato da dati di codice a barre associati a un elemento che ha anche un tag di asset. Si noti che se sono disponibili solo i dati del codice a barre e sono univoci o possono essere usati come chiave dell'elemento, questa proprietà sarà **NULL** e i dati del codice a barre verranno usati come chiave di classe nella proprietà tag.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
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

**Rimovibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** un pacchetto fisico è rimovibile (se è progettato per essere prelevato e estratto dal contenitore fisico in cui viene normalmente trovato, senza compromettere la funzione della creazione complessiva dei pacchetti). Un pacchetto può comunque essere rimovibile se l'alimentazione deve essere disattivata per eseguire la rimozione. Se l'alimentazione può essere "on" e il pacchetto è stato rimosso, l'elemento è rimovibile e può essere scambiato a caldo. Ad esempio, una batteria aggiuntiva in un portatile è rimovibile, così come un pacchetto di unità disco inserito usando connettori SCA. Tuttavia, quest'ultimo può essere scambiato a caldo. Il display di un portatile non è rimovibile, né è un alimentatore non rimovibile. La rimozione di questi componenti influisce sulla funzione del pacchetto complessivo o è impossibile a causa della stretta integrazione del pacchetto.

Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**Sostituibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** un pacchetto fisico è sostituibile (se è possibile sostituire, FRU o aggiornare, l'elemento con un elemento fisicamente diverso). Ad esempio, alcuni sistemi di computer consentono l'aggiornamento del chip del processore principale a una classificazione di clock superiore. In questo caso, il processore è detto sostituibile. Un altro esempio è un pacchetto di alimentazione montato su guide scorrevoli. Tutti i pacchetti rimovibili sono intrinsecamente sostituibili.

Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
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

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Numero di unità di mantenimento delle scorte per l'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
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

Qualificatori: [**Key,**](../wmisdk/key-qualifier.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Identificatore univoco del dispositivo di scheda connesso al sistema.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

Esempio: "On Board Device 1"

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Versione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ OnBoardDevice Win32** è derivata da [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

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

[**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)
</dt> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
