---
description: Rappresenta il software di basso livello caricato nell'archiviazione non volatile e usato per avviare e configurare un computer system (CIM \_ ComputerSystem).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: CIM_BIOSElement classe (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c443e212913eef60bd3b4c6db8145f454e7de027b5445268c7abb7b2ee8457fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813402"
---
# <a name="cim_bioselement-class-hyper-v-management"></a>CIM_BIOSElement classe (gestione Hyper-V)

Rappresenta il software di basso livello caricato nell'archiviazione non volatile e usato per avviare e configurare un sistema informatico ([**CIM \_ ComputerSystem**](cim-computersystem.md)).

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a>Members

La **classe \_ CIM BIOSElement** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CIM BIOSElement** ha queste proprietà.

<dl> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSElement**.**ListOfLanguages**")
</dt> </dl>

Lingua attualmente selezionata per il BIOS. Queste informazioni possono essere ottenute dal BIOS di Gestione sistema (SMBIOS) usando l'attributo Current Language della struttura Type 13 per indicizzare nell'elenco di stringhe che segue la struttura. Questa proprietà viene formattata usando il nome della lingua ISO 639 e può essere seguita dal nome del territorio ISO 3166 e dal metodo di codifica.

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di lingue installabili per il BIOS. Queste informazioni possono essere ottenute da SMBIOS, dall'elenco di stringhe che segue la struttura di tipo 13. È necessario usare un nome di lingua ISO 639 per specificare le lingue installabili del BIOS. È anche possibile specificare il nome del territorio ISO 3166 e il metodo di codifica, seguendo il nome della lingua.

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. BIOS di sistema DMTF \| \| 001.6")
</dt> </dl>

Indirizzo finale della memoria occupata dal BIOS.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. BIOS di sistema DMTF \| \| 001.5")
</dt> </dl>

Indirizzo iniziale della memoria occupata dal BIOS.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.7")
</dt> </dl>

Stringa in formato libero che descrive l'utilità flash/load del BIOS necessaria per aggiornare **l'oggetto \_ CIM BIOSElement.** La versione e altre informazioni possono essere indicate in questa proprietà.

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. BIOS di sistema DMTF \| \| 001.2")
</dt> </dl>

Produttore dell'elemento software.

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. BIOS di sistema DMTF \| \| 001.9")
</dt> </dl>

True se si tratta del BIOS primario del sistema informatico; in caso contrario, false.

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di pubblicazione dei registri degli attributi BIOS a cui è conforme l'implementazione del BIOS.

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. BIOS di sistema DMTF \| \| 001.8")
</dt> </dl>

Data di rilascio del BIOS.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. BIOS di sistema DMTF \| \| 001.3")
</dt> </dl>

Versione dell'operazione. La versione dell'operazione deve essere in uno dei formati seguenti:

-   *<major>*.*<minor>*.*<revision>*
-   *<major>*.*<minor><letter><revision>*

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

[**CIM \_ SoftwareElement**](cim-softwareelement.md)
</dt> </dl>

 

