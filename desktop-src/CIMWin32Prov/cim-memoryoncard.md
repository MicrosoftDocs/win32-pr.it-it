---
description: La classe CIM MemoryOnCard associa la memoria fisica che si trova nelle schede di hosting, nelle \_ schede di scheda e così via. Questa associazione definisce in modo esplicito la relazione tra memoria e schede.
ms.assetid: 0d094cad-c542-4794-b6e1-87cdc8067668
ms.tgt_platform: multiple
title: CIM_MemoryOnCard classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryOnCard
- CIM_MemoryOnCard.LocationWithinContainer
- CIM_MemoryOnCard.PartComponent
- CIM_MemoryOnCard.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a07a8894e237be24a4c7b49e8491278ffb9e9ea82109fee00c27fc4eb9d5fcb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506791"
---
# <a name="cim_memoryoncard-class"></a>Classe CiM \_ MemoryOnCard

La **classe CIM \_ MemoryOnCard** associa la memoria fisica che si trova nelle schede di hosting, nelle schede di scheda e così via. Questa associazione definisce in modo esplicito la relazione tra memoria e schede.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B7C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryOnCard : CIM_PackagedComponent
{
  string                 LocationWithinContainer;
  CIM_PhysicalMemory REF PartComponent;
  CIM_Card           REF GroupComponent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ MemoryOnCard** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ MemoryOnCard** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **scheda \_ CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Scheda [**CIM \_ che descrive**](cim-card.md) la scheda che include o "contiene" memoria.

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

Tipo di dati: **CIM \_ PhysicalMemory**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Oggetto [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) che descrive la memoria fisica che si trova nella scheda.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ MemoryOnCard** è derivata da [**CIM \_ PackagedComponent.**](cim-packagedcomponent.md)

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

[**CIM \_ PackagedComponent**](cim-packagedcomponent.md)
</dt> </dl>

 

