---
description: La \_ classe CIM ApplicationSystemSoftwareFeature rappresenta un'associazione che identifica le funzionalità software che costituiscono un particolare sistema applicativo. Le funzionalità software possono essere incluse in prodotti diversi.
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: Classe CIM_ApplicationSystemSoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b13a15370b19583eef61fb36fda2d63fcb61989
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878069"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a>CIM \_ ApplicationSystemSoftwareFeature (classe)

La classe **CIM \_ ApplicationSystemSoftwareFeature** rappresenta un'associazione che identifica le funzionalità software che costituiscono un particolare sistema applicativo. Le funzionalità software possono essere incluse in prodotti diversi.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ApplicationSystemSoftwareFeature** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ApplicationSystemSoftwareFeature** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ApplicationSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Un [**\_ ApplicationSystem CIM**](cim-applicationsystem.md) che contiene il sistema padre nell'associazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ SoftwareFeature**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) che contiene l'elemento figlio che è un componente di un sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ ApplicationSystemSoftwareFeature** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).

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

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> </dl>

 

