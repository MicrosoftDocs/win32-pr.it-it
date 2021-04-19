---
description: Rappresenta il software di basso livello caricato nell'archiviazione non volatile e utilizzato per avviare e configurare un sistema di computer (CIM \_ ComputerSystem).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: Classe CIM_BIOSElement (gestione Hyper-V)
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
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319527"
---
# <a name="cim_bioselement-class-hyper-v-management"></a>Classe CIM_BIOSElement (gestione Hyper-V)

Rappresenta il software di basso livello caricato nell'archiviazione non volatile e utilizzato per avviare e configurare un sistema di computer ([**CIM \_ ComputerSystem**](cim-computersystem.md)).

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

La classe **CIM \_ bioselement** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ bioselement** dispone di queste proprietà.

<dl> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ bioselement**.**ListOfLanguages**")
</dt> </dl>

Lingua attualmente selezionata per il BIOS. Queste informazioni possono essere ottenute da System Management BIOS (SMBIOS) utilizzando l'attributo della lingua corrente della struttura di tipo 13 da indicizzare nell'elenco di stringhe che segue la struttura. Questa proprietà viene formattata con il nome della lingua ISO 639 e può essere seguita dal nome del territorio ISO 3166 e dal metodo di codifica.

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di lingue installabili per il BIOS. Queste informazioni possono essere ottenute da SMBIOS, dall'elenco di stringhe che segue la struttura di tipo 13. Per specificare le lingue installabili del BIOS, è necessario usare un nome di lingua ISO 639. È possibile specificare anche il nome del territorio ISO 3166 e il metodo di codifica, dopo il nome della lingua.

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,6 ")
</dt> </dl>

Indirizzo finale della memoria occupata dal BIOS.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,5 ")
</dt> </dl>

Indirizzo iniziale della memoria occupata dal BIOS.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,7 ")
</dt> </dl>

Stringa in formato libero che descrive l'utilità Flash/Load BIOS necessaria per aggiornare l'oggetto **CIM \_ bioselement** . La versione e altre informazioni possono essere indicate in questa proprietà.

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,2 ")
</dt> </dl>

Produttore dell'elemento software.

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,9 ")
</dt> </dl>

True se si tratta del BIOS principale del computer. in caso contrario, false.

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il percorso di pubblicazione dei registri degli attributi BIOS a cui è conforme l'implementazione del BIOS.

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,8 ")
</dt> </dl>

Data in cui è stato rilasciato il BIOS.

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,3 ")
</dt> </dl>

Versione dell'operazione. La versione dell'operazione deve essere in uno dei seguenti formati:

-   *<major>*.*<minor>*.*<revision>*
-   *<major>*.*<minor><letter><revision>*

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Software CIM**](cim-softwareelement.md)
</dt> </dl>

 

