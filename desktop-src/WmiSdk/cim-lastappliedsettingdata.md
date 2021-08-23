---
description: Associazione tra un oggetto e un altro oggetto a cui è stato applicato.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: CIM_LastAppliedSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 6c1e5174cb9fcaf9279d16eceda547e9e5060c4ca4f7deda09cc170cf3dd7653
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244651"
---
# <a name="cim_lastappliedsettingdata-class"></a>Classe CIM \_ LastAppliedSettingData

Associazione tra un oggetto e un altro oggetto a cui è stato applicato.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a>Members

La **classe CIM \_ LastAppliedSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ LastAppliedSettingData** ha queste proprietà.

<dl> <dt>

**AppliedObject**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Oggetto applicato all'oggetto di destinazione.

</dd> <dt>

**Destinazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Oggetto che rappresenta la destinazione dell'applicazione dell'oggetto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------|
| Spazio dei nomi<br/> | \\CIMV2 radice<br/> |



 

 




