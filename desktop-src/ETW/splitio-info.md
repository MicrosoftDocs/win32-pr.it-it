---
description: Questa classe è la classe del tipo di evento per gli eventi di I/O suddivisi. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 0eb1f712-8b1c-4de1-b701-5c7dbabb0f55
title: SplitIo_Info classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo_Info
- SplitIo_Info.ParentIrp
- SplitIo_Info.ChildIrp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5ae5623f4d05bc4c0e5460415656f59d8b91eeedfe1671cae6a36c7a33e0a86f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766421"
---
# <a name="splitio_info-class"></a>Classe SplitIo \_ Info

Questa classe è la classe del tipo di evento per gli eventi di I/O suddivisi.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{32}, EventTypeName{"VolMgr"}]
class SplitIo_Info : SplitIo
{
  uint32 ParentIrp;
  uint32 ChildIrp;
};
```

## <a name="members"></a>Members

La **classe SplitIo \_ Info** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SplitIo \_ Info** ha queste proprietà.

<dl> <dt>

**ChildIrp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Pointer
</dt> </dl>

Pacchetto di richiesta I/O figlio.

</dd> <dt>

**Elemento ParentIrp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Pointer
</dt> </dl>

Pacchetto di richiesta I/O padre.

</dd> </dl>

## <a name="remarks"></a>Commenti

Indica che gestione volumi ha suddiviso il IRP in due IRP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 




