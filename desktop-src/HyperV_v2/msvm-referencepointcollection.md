---
description: Rappresenta una raccolta di punti di riferimento del sistema virtuale.
ms.assetid: dc293f94-a683-468f-af05-ba99824d773e
title: Classe Msvm_ReferencePointCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointCollection
- Msvm_ReferencePointCollection.CollectionID
- Msvm_ReferencePointCollection.ElementName
- Msvm_ReferencePointCollection.ReferencePointType
- Msvm_ReferencePointCollection.ConsistencyLevel
- Msvm_ReferencePointCollection.VirtualSystemCollectionId
- Msvm_ReferencePointCollection.HasAssociatedLog
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 570590221ee8568d78e150fec3c359365c8434cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882169"
---
# <a name="msvm_referencepointcollection-class"></a>\_Classe MSVM ReferencePointCollection

Rappresenta una raccolta di punti di riferimento del sistema virtuale.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointCollection : CIM_Collection
{
  string  CollectionID;
  string  ElementName;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemCollectionId;
  boolean HasAssociatedLog;
};
```

## <a name="members"></a>Members

La **classe \_ ReferencePointCollection di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ReferencePointCollection di MSVM** dispone di queste proprietà.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificazione univoca dell'oggetto raccolta.

</dd> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Livello di coerenza del punto di riferimento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coerente con l'arresto anomalo** (1)


</dt> <dd>

Il punto di riferimento indica un punto nel tempo in cui il sistema virtuale si trova in uno stato di arresto anomalo.

</dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coerente** con l'applicazione (2)


</dt> <dd>

Il punto di riferimento indica un punto nel tempo in cui il sistema virtuale era in uno stato coerente con l'applicazione.

</dd> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Nome definito dall'utente per la raccolta. Si noti che non è garantito che sia univoco.

</dd> <dt>

**HasAssociatedLog**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

**true** se a tutti i punti di riferimento del membro sono associati log. Questa operazione è valida solo per i punti di riferimento basati su log. Per i punti di riferimento basati su RCT, **HasAssociatedLog** è impostato su **false**. Per i punti di riferimento basati su log, dopo l'eliminazione del log **HasAssociatedLog** diventa **false**.

</dd> <dt>

**ReferencePointType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **in**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Indica il tipo del punto di riferimento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basato su log** (1)


</dt> <dd>

Rilevamento del log della replica Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basato su RCT** (2)


</dt> <dd>

Basato su Rilevamento modifiche resiliente di dischi virtuali.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Specifico del fornitore** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualSystemCollectionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionID**")
</dt> </dl>

Identificatore del [**\_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) a cui appartiene il punto di riferimento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Raccolta CIM**](cim-collection.md)
</dt> </dl>

 

