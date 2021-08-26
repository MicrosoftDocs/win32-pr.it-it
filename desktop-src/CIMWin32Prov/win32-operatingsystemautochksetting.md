---
description: Questa classe rappresenta l'associazione tra un sistema operativo e le impostazioni di autochk che si applicano ai dischi del computer. Si noti che l'impostazione è associata al sistema operativo anziché al sistema informatico, poiché nel computer possono essere installati uno o più sistemi operativi, ognuno con le proprie impostazioni di autochk.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Win32_OperatingSystemAutochkSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cfa6e90828935dda8aa163967985813526042b8800f91cb01825fbd158f8a63d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972541"
---
# <a name="win32_operatingsystemautochksetting-class"></a>Classe \_ OperatingSystemAutochkSetting Win32

Questa classe rappresenta l'associazione tra un sistema operativo e le impostazioni di autochk che si applicano ai dischi del computer. Si noti che l'impostazione è associata al sistema operativo anziché al sistema informatico, poiché nel computer possono essere installati uno o più sistemi operativi, ognuno con le proprie impostazioni di autochk.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ OperatingSystemAutochkSetting** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ OperatingSystemAutochkSetting** ha queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **Sistema operativo \_ Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**chiave**](../wmisdk/key-qualifier.md)
</dt> </dl>

DA DEFINIRE

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ AutochkSetting**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**chiave**](../wmisdk/key-qualifier.md)
</dt> </dl>

DA DEFINIRE

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento \_ CIMSetting**](cim-elementsetting.md)
</dt> </dl>

 

 
