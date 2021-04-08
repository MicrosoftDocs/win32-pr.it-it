---
description: La \_ classe CIM AggregateRedundancyComponent descrive l'extent fisico aggregato in un gruppo di ridondanza di archiviazione.
ms.assetid: 3407e888-e17c-4f65-a33f-056002accbf7
ms.tgt_platform: multiple
title: Classe CIM_AggregateRedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregateRedundancyComponent
- CIM_AggregateRedundancyComponent.PartComponent
- CIM_AggregateRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9a5e638730578bad8d64f35b29a5152898c23fd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748714"
---
# <a name="cim_aggregateredundancycomponent-class"></a>CIM \_ AggregateRedundancyComponent (classe)

La classe **CIM \_ AggregateRedundancyComponent** descrive l'extent fisico aggregato in un gruppo di ridondanza di archiviazione.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{154E66D8-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AggregateRedundancyComponent : CIM_RedundancyComponent
{
  CIM_AggregatePExtent       REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ AggregateRedundancyComponent** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ AggregateRedundancyComponent** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ StorageRedundancyGroup**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Un [**\_ StorageRedundancyGroup CIM**](cim-storageredundancygroup.md) che contiene il gruppo di ridondanza di archiviazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ AggregatePExtent**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un [**\_ AggregatePExtent CIM**](cim-aggregatepextent.md) che contiene l'extent fisico aggregato che partecipa al gruppo di ridondanza.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ AggregateRedundancyComponent** è derivata da [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md).

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

[**\_REDUNDANCYCOMPONENT CIM**](cim-redundancycomponent.md)
</dt> </dl>

 

