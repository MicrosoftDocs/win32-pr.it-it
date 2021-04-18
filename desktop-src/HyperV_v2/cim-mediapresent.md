---
description: Rappresenta una relazione in cui è necessario accedere a un extent di archiviazione tramite un dispositivo di accesso multimediale.
ms.assetid: 436a7e2d-2c14-4058-aca0-669373b8004a
title: Classe CIM_MediaPresent (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Antecedent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e26c36231edaf3ca4b8accf844a3c58b3d70bc7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320467"
---
# <a name="cim_mediapresent-class-hyper-v-management"></a>Classe CIM_MediaPresent (gestione Hyper-V)

Rappresenta una relazione in cui è necessario accedere a un extent di archiviazione tramite un dispositivo di accesso multimediale.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageExtents"), MappingStrings("MIF.DMTF|Storage Devices|001.8"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a>Members

La classe **CIM \_ MediaPresent** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ MediaPresent** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ MediaAccessDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Il dispositivo di accesso multimediale.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ StorageExtent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

L'extent di archiviazione a cui si accede quando si usa il dispositivo di accesso multimediale.

</dd> <dt>

**FixedMedia**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se l'extent di archiviazione è fisso nel dispositivo di accesso multimediale e non può essere espulso; in caso contrario, **false**.

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

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> </dl>

 

