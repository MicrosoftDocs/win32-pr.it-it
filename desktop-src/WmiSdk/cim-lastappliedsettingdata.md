---
description: Associazione tra un oggetto e un altro oggetto a cui è stato applicato.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: Classe CIM_LastAppliedSettingData
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
ms.openlocfilehash: fbad71cd88992673af5dd60c04b92dd3c833e5b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324712"
---
# <a name="cim_lastappliedsettingdata-class"></a>CIM \_ LastAppliedSettingData (classe)

Associazione tra un oggetto e un altro oggetto a cui è stato applicato.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

La classe **CIM \_ LastAppliedSettingData** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ LastAppliedSettingData** dispone di queste proprietà.

<dl> <dt>

**AppliedObject**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ Managed**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Oggetto applicato all'oggetto di destinazione.

</dd> <dt>

**Destinazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ Managed**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Oggetto che era la destinazione dell'applicazione dell'oggetto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------|
| Spazio dei nomi<br/> | \\CIMV2 radice<br/> |



 

 




