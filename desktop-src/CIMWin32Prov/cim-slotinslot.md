---
description: La \_ relazione CIM SlotInSlot rappresenta la capacità di un adattatore speciale di estendere la struttura degli slot esistente per consentire l'inserimento di schede altrimenti incompatibili in un frame o in una lavagna di hosting.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: Classe CIM_SlotInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304491"
---
# <a name="cim_slotinslot-class"></a>CIM \_ SlotInSlot (classe)

La relazione **CIM \_ SlotInSlot** rappresenta la capacità di un adattatore speciale di estendere la struttura degli slot esistente per consentire l'inserimento di schede altrimenti incompatibili in un frame o in una lavagna di hosting. Gli slot sono tipi speciali di connettori in cui vengono in genere inserite le schede scheda. L'adapter crea in modo efficace un nuovo slot e può essere considerato (concettualmente) come uno slot in uno slot. Le schede che altrimenti sarebbero fisicamente o elettricamente incompatibili con gli slot esistenti sarebbero supportate dall'interazione con lo slot fornito dall'adapter. Le schede di rete, ad esempio, sono molto costose. Quando diventa disponibile un nuovo hardware, le configurazioni dello chassis e della scheda cambiano. Per proteggere l'investimento dei clienti, i fornitori di reti produrrà adattatori speciali che consentono alle vecchie schede di rientrare in nuovi chassis o lavagne di hosting o nuove schede per adattarle a schede obsolete usando un adattatore speciale che si adatta a uno o più slot esistenti e presenta un nuovo slot in cui è possibile adattare la scheda.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ SlotInSlot** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ SlotInSlot** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ slot CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Uno [**\_ slot CIM**](cim-slot.md) che descrive gli slot esistenti della lavagna di hosting o il frame che viene adattato per contenere una scheda che altrimenti non sarebbe fisicamente e/o elettricamente compatibile con essa.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ slot CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Uno [**\_ slot CIM**](cim-slot.md) che descrive il nuovo slot fornito dalla scheda adapter.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ SlotInSlot** è derivata da [**CIM \_ ConnectedTo**](cim-connectedto.md).

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

[**\_CONNECTEDTO CIM**](cim-connectedto.md)
</dt> </dl>

 

