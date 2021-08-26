---
description: La classe WMI di associazione WMIElementSetting Win32 mette in relazione un servizio in esecuzione nel sistema Windows e le impostazioni \_ WMI che può usare.
ms.assetid: 00e9f882-5f54-4042-a916-2f90ed9a37c0
ms.tgt_platform: multiple
title: Win32_WMIElementSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMIElementSetting
- Win32_WMIElementSetting.Element
- Win32_WMIElementSetting.Setting
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: f46a9d5fd7c3f0baace1f763b9912f49fbcf318ffd07fa7cbf3138d04d8621f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922541"
---
# <a name="win32_wmielementsetting-class"></a>Classe WMIElementSetting Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) **di associazione \_ WMIElementSetting Win32** mette in relazione un servizio in esecuzione nel sistema Windows e le impostazioni WMI che può usare.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("WBEMCORE"), UUID("{A83EF167-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMIElementSetting : CIM_ElementSetting
{
  Win32_Service    REF Element;
  Win32_WMISetting REF Setting;
};
```

## <a name="members"></a>Members

La **classe \_ WMIElementSetting Win32** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ WMIElementSetting Win32** dispone di queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **Servizio \_ Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Service")
</dt> </dl>

Riferimento all'istanza di che rappresenta il Windows utilizzando o indicando le proprietà WMI.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ WmiSetting Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ WMISetting")
</dt> </dl>

Riferimento all'istanza di che rappresenta le impostazioni WMI disponibili per il Windows servizio.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ WMIElementSetting Win32** è derivata da [**\_ ElementSetting CIM.**](cim-elementsetting.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ElementSetting**](cim-elementsetting.md)
</dt> <dt>

[Classi di gestione del servizio WMI](./wmi-service-management-classes.md)
</dt> </dl>

 

 
