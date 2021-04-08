---
description: L' \_ associazione CIM PackagedComponent rappresenta una relazione esplicita in cui un componente è in genere contenuto in un pacchetto fisico, ad esempio uno chassis o una scheda.
ms.assetid: ef0cdbc4-41ee-4517-92ca-61cfcbe64c36
ms.tgt_platform: multiple
title: Classe CIM_PackagedComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackagedComponent
- CIM_PackagedComponent.LocationWithinContainer
- CIM_PackagedComponent.PartComponent
- CIM_PackagedComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b95cbbea60bfbd6bb352e53cfecb8819d99ec24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877393"
---
# <a name="cim_packagedcomponent-class"></a>CIM \_ PackagedComponent (classe)

L'associazione **CIM \_ PackagedComponent** rappresenta una relazione esplicita in cui un componente è in genere contenuto in un pacchetto fisico, ad esempio uno chassis o una scheda.

**Nota**  Un componente può essere rimosso o non ancora inserito in, il pacchetto che lo contiene (ovvero la proprietà booleana **rimovibile** è **true**). È pertanto possibile che un componente non sia sempre associato a un contenitore.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B79-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackagedComponent : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalComponent REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ PackagedComponent** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ PackagedComponent** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalPackage**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Un [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) che descrive il pacchetto fisico che contiene i componenti.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico. Le informazioni relative agli elementi stazionari del contenitore (ad esempio, "seconda Bay Drive dalla parte superiore"), angoli, altezze e altri dati possono essere registrate in questa proprietà. Questa stringa può essere aggiunta o utilizzata al posto della creazione di un'istanza dell'oggetto [**\_ percorso CIM**](cim-location.md) .

Questa proprietà viene ereditata [**dal \_ contenitore CIM**](cim-container.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalComponent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md) che descrive il componente fisico contenuto nel pacchetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ PackagedComponent** è derivata dal [**\_ contenitore CIM**](cim-container.md).

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

[**\_Contenitore CIM**](cim-container.md)
</dt> </dl>

 

