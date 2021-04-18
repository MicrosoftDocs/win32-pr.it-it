---
description: Un'associazione tra un'istanza di CIM \_ VirtualSystemSettingData e l' \_ istanza CIM VirtualSystemSettingData che rappresenta lo snapshot più recente su cui si basa questo oggetto.
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: Classe CIM_ParentChildSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 9b2b866c3d5ae15d3f5a97c971e8efec75e9164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329649"
---
# <a name="cim_parentchildsettingdata-class"></a>CIM \_ ParentChildSettingData (classe)

Un'associazione tra un'istanza di [**CIM \_ VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) e l'istanza **CIM \_ VirtualSystemSettingData** che rappresenta lo snapshot più recente su cui si basa questo oggetto.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ParentChildSettingData** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ParentChildSettingData** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'oggetto indipendente in questa associazione.

Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Figlio**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati di impostazione per il sistema virtuale che rappresenta l'elemento figlio dell'elemento padre.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'oggetto che dipende dalla proprietà **precedente** .

Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

I dati di impostazione dello snapshot su cui si basano i dati delle impostazioni figlio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------|
| Spazio dei nomi<br/> | \\CIMV2 radice<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

