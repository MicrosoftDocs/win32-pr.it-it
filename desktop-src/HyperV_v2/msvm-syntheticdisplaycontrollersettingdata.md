---
description: Descrive i dati di impostazione per un controller di visualizzazione sintetico virtuale.
ms.assetid: cea79b24-4175-49db-a8b4-a9efb1fd0b96
title: Msvm_SyntheticDisplayControllerSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayControllerSettingData
- Msvm_SyntheticDisplayControllerSettingData.ResolutionType
- Msvm_SyntheticDisplayControllerSettingData.HorizontalResolution
- Msvm_SyntheticDisplayControllerSettingData.VerticalResolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3adb39294af6dab153338aff17d16d8e44e3f4977617e9ee34e1686534bc35c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949840"
---
# <a name="msvm_syntheticdisplaycontrollersettingdata-class"></a>Classe Msvm \_ SyntheticDisplayControllerSettingData

Descrive i dati di impostazione per un controller di visualizzazione sintetico virtuale.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  uint8  ResolutionType;
  uint16 HorizontalResolution;
  uint16 VerticalResolution;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SyntheticDisplayControllerSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SyntheticDisplayControllerSettingData** ha queste proprietà.

<dl> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Risoluzione orizzontale.

</dd> <dt>

**ResolutionType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di risoluzione.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Massimo** (2)


</dt> <dd></dd> <dt>

<span id="Single"></span><span id="single"></span><span id="SINGLE"></span>

<span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Singolo** (3)


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Impostazione** predefinita (4)


</dt> <dd>

> [!Note]  
> Aggiunta in Windows 10, versione 1703.

 

</dd> </dl>

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Risoluzione verticale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




