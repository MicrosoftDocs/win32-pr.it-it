---
description: La classe CIM RedundancyComponent associa un gruppo di ridondanza costituito da elementi di sistema gestiti e indica che, insieme, gli elementi \_ forniscono ridondanza.
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: CIM_RedundancyComponent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bf2264d88a36f684c1ae198224a6e5543063bbf86ed3da77b0211f066eb080d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920791"
---
# <a name="cim_redundancycomponent-class"></a>Classe \_ CIM RedundancyComponent

La **classe CIM \_ RedundancyComponent** associa un gruppo di ridondanza costituito da elementi di sistema gestiti e indica che, insieme, gli elementi forniscono ridondanza. Tutti gli elementi aggregati in un gruppo di ridondanza devono essere istanze della stessa classe di oggetti.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ RedundancyComponent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ RedundancyComponent** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ RedundancyGroup**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

**L'associazione CIM \_ RedundancyComponent** indica che "questo set di ventole" o "questi extent fisici" fanno parte di un singolo gruppo di ridondanza.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Oggetto [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) che descrive l'elemento figlio nell'associazione.

Questa proprietà viene ereditata dal [**componente CIM. \_**](cim-component.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

**CIM \_ RedundancyComponent** deriva dal [**componente CIM \_**](cim-component.md).

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

[**Componente \_ CIM**](cim-component.md)
</dt> </dl>

 

