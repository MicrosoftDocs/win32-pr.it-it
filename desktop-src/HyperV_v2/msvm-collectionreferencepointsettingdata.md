---
description: Fornisce informazioni aggiuntive da utilizzare con il metodo CreateReferencePoint della \_ classe CollectionReferencePointService di MSVM.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Classe Msvm_CollectionReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ac05518a3ea9512745e9d2391c2d8cf1d387c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130698"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a>\_Classe MSVM CollectionReferencePointSettingData

Fornisce informazioni aggiuntive da utilizzare con il metodo [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) della classe [**\_ CollectionReferencePointService di MSVM**](msvm-collectionreferencepointservice.md) .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a>Members

La **classe \_ CollectionReferencePointSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CollectionReferencePointSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Livello di coerenza del punto di riferimento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coerente** con l'applicazione (1)


</dt> <dd>

Il punto di riferimento indica un punto nel tempo in cui il sistema virtuale si trova in uno stato di arresto anomalo.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coerente con l'arresto anomalo** (2)


</dt> <dd>

Il punto di riferimento indica un punto nel tempo in cui il sistema virtuale era in uno stato coerente con l'applicazione.

</dd> </dl>

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

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




