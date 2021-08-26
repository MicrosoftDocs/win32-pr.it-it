---
description: L'associazione CiM PackageInChassis rappresenta la relazione in cui uno chassis può contenere altri pacchetti, ad esempio altri \_ chassis e schede.
ms.assetid: 3243bc0f-ce20-4108-b6e3-838bcb8f2fec
ms.tgt_platform: multiple
title: CIM_PackageInChassis classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInChassis
- CIM_PackageInChassis.LocationWithinContainer
- CIM_PackageInChassis.PartComponent
- CIM_PackageInChassis.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2dec66ed5ee930db9bff7917e942de44bdc9582ec130a987e83cbb9d633523cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921301"
---
# <a name="cim_packageinchassis-class"></a>Classe \_ CiM PackageInChassis

**L'associazione \_ CiM PackageInChassis** rappresenta la relazione in cui uno chassis può contenere altri pacchetti, ad esempio altri chassis e schede.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B74-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInChassis : CIM_Container
{
  string                  LocationWithinContainer;
  CIM_PhysicalPackage REF PartComponent;
  CIM_Chassis         REF GroupComponent;
};
```

## <a name="members"></a>Members

La **classe \_ CiM PackageInChassis** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CiM PackageInChassis** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ Chassis CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Chassis [**CIM \_ che**](cim-chassis.md) descrive lo chassis che contiene altri pacchetti fisici.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico. In questa proprietà è possibile registrare informazioni relative a elementi stazionari nel contenitore ,ad esempio "second drive bay from the top", angolazioni, altitudini e altri dati. Questa stringa può integrare o usare al posto della creazione di un'istanza [**dell'oggetto \_ Location CIM.**](cim-location.md)

Questa proprietà viene ereditata dal [**contenitore CIM. \_**](cim-container.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalPackage**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**PhysicalPackage \_ CIM**](cim-physicalpackage.md) che descrive il pacchetto fisico contenuto nello chassis.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ CiM PackageInChassis** è derivata dal [**contenitore CIM \_**](cim-container.md).

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[**Contenitore \_ CIM**](cim-container.md)
</dt> </dl>

 

