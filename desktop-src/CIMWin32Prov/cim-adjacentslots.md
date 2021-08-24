---
description: L'associazione CIM AdjacentSlots descrive il layout degli slot in una scheda di scheda o \_ scheda di hosting.
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: CIM_AdjacentSlots classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a219c2bbe95d8ccf3f89c029b4cb9f417ef8e2f0633a058c736b1339a41d7571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701301"
---
# <a name="cim_adjacentslots-class"></a>Classe CIM \_ AdjacentSlots

**L'associazione CIM \_ AdjacentSlots** descrive il layout degli slot in una scheda di scheda o scheda di hosting. Le informazioni, ad esempio la distanza tra gli slot e se sono "condivise" (se ne viene popolato uno, l'altro slot non può essere usato), vengono trasmesse come proprietà di associazione.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a>Members

La **classe CIM \_ AdjacentSlots** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ AdjacentSlots** ha queste proprietà.

<dl> <dt>

**DistanceBetweenSlots**
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")
</dt> </dl>

Distanza, in pollici, tra gli slot adiacenti.

</dd> <dt>

**SharedSlots**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** uno degli slot viene popolato da una scheda dell'adapter. l'altro slot deve essere lasciato vuoto.

</dd> <dt>

**SlotA**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ slot CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fare riferimento a uno degli slot adiacenti.

</dd> <dt>

**SlotB**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ slot CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'altro slot adiacente.

</dd> </dl>

## <a name="remarks"></a>Commenti

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

[Classi CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

