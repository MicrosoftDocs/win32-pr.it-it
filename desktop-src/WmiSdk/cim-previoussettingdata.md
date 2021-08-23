---
description: Associazione tra un sistema virtuale e i dati di impostazione dello snapshot padre del sistema virtuale.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: CIM_PreviousSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 85f08f22409df8a17bdae33ae81c06cb8167996ecb477f6a2d207d9e0ce2acca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131763"
---
# <a name="cim_previoussettingdata-class"></a>Classe CIM \_ PreviousSettingData

Associazione tra un sistema virtuale e i dati di impostazione dello snapshot padre del sistema virtuale.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a>Members

La **classe CIM \_ PreviousSettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ PreviousSettingData** ha queste proprietà.

<dl> <dt>

**Oggetto precedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Dati dell'impostazione dello snapshot padre di questo computer.

</dd> <dt>

**Destinazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Sistema computer di destinazione dell'applicazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------|
| Spazio dei nomi<br/> | \\CIMV2 radice<br/> |



 

 




