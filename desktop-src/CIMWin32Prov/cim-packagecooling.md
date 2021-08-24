---
description: L'associazione CIM PackageCooling rappresenta la relazione in cui un dispositivo di raffreddamento viene installato in un pacchetto, ad esempio uno chassis o un rack, per facilitare il raffreddamento \_ del pacchetto.
ms.assetid: 0aaae8e1-6e70-4b26-8e56-dac5657e58c1
ms.tgt_platform: multiple
title: CIM_PackageCooling classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageCooling
- CIM_PackageCooling.Dependent
- CIM_PackageCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1dcb6727e909936e08ba8506c1a99855136c0a9725c746503dbf7fd7626515df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820631"
---
# <a name="cim_packagecooling-class"></a>Classe \_ CiM PackageCooling

**L'associazione CIM \_ PackageCooling** rappresenta la relazione in cui un dispositivo di raffreddamento viene installato in un pacchetto, ad esempio uno chassis o un rack, per facilitare il raffreddamento del pacchetto.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B8E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageCooling : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_CoolingDevice   REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ PackageCooling** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ PackageCooling** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ CoolingDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Oggetto [**CIM \_ CoolingDevice**](cim-coolingdevice.md) che descrive il dispositivo di raffreddamento per il pacchetto.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalPackage**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

[**CiM \_ PhysicalPackage che**](cim-physicalpackage.md) descrive il pacchetto fisico il cui ambiente è cooled.

</dd> </dl>

## <a name="remarks"></a>Commenti

**CIM \_ PackageCooling** deriva dalla [**dipendenza CIM. \_**](cim-dependency.md)

WMI non implementa questa classe.

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

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> </dl>

 

