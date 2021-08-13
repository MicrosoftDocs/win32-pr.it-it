---
description: Rappresenta un set di componenti che funzionano come singola entità di alto livello.
ms.assetid: 784cee32-e0ae-4632-8dac-e5110513f5c9
title: CIM_System classe (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerName
- CIM_System.PrimaryOwnerContact
- CIM_System.Roles
- CIM_System.OtherIdentifyingInfo
- CIM_System.IdentifyingDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 143e2514ae22528c695542ad67024a4ef9a75532c0e734b69f3c9e6772777a70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646795"
---
# <a name="cim_system-class-hyper-v-management"></a>CIM_System classe (gestione Hyper-V)

Rappresenta un set di componenti che funzionano come singola entità di alto livello.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_System : CIM_EnabledLogicalElement
{
  string CreationClassName;
  string Name;
  string NameFormat;
  string PrimaryOwnerName;
  string PrimaryOwnerContact;
  string Roles[];
  string OtherIdentifyingInfo[];
  string IdentifyingDescriptions[];
};
```

## <a name="members"></a>Members

La **classe CIM \_ System** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ System** ha queste proprietà.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome della classe utilizzato per creare un'istanza di questa classe. **CreationClassName viene** combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ System**.**OtherIdentifyingInfo**")
</dt> </dl>

Matrice contenente le descrizioni dei valori nella **proprietà OtherIdentifyingInfo.** Gli elementi della matrice in **IdentifyingDescriptions** corrispondono agli elementi nella **proprietà IdentifyingDescriptions.**

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Chiave di questa istanza in un ambiente aziendale.

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Convenzione di denominazione usata dalla proprietà Name per garantire che i **valori Name** siano univoci.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ System**.**IdentifyingDescriptions**")
</dt> </dl>

Matrice contenente un set di dati aggiuntivi, oltre alle informazioni sul nome del sistema, che possono essere usati per identificare un sistema informatico.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. INFORMAZIONI \| GENERALI DMTF \| 001.4")
</dt> </dl>

Stringa che fornisce informazioni su come è possibile raggiungere il proprietario del sistema primario, ad esempio il numero di telefono, l'indirizzo di posta elettronica e così via.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DmTF \| General Information \| 001.3")
</dt> </dl>

Nome dell'utente primario del sistema.

</dd> <dt>

**Ruoli**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Matrice contenente i ruoli eseguiti dal sistema in un ambiente aziendale.

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

[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)
</dt> </dl>

 

