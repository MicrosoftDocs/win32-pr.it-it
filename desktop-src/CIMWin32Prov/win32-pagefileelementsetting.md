---
description: La \_ classe WMI dell'associazione PageFileElementSetting Win32 mette in relazione le impostazioni iniziali di un file di paging e lo stato di tali impostazioni durante il normale utilizzo.
ms.assetid: efc1f20d-166e-4e27-9767-f6ec0bbd6c14
ms.tgt_platform: multiple
title: Classe Win32_PageFileElementSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileElementSetting
- Win32_PageFileElementSetting.Element
- Win32_PageFileElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfc1087225894cef2895cf41af5e5297769a4041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966291"
---
# <a name="win32_pagefileelementsetting-class"></a>Win32 \_ PageFileElementSetting (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PageFileElementSetting Win32** mette in relazione le impostazioni iniziali di un file di paging e lo stato di tali impostazioni durante il normale utilizzo.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8E7F70E8-C856-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileElementSetting : CIM_ElementSetting
{
  Win32_PageFileUsage   REF Element;
  Win32_PageFileSetting REF Setting;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ PageFileElementSetting** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PageFileElementSetting** dispone di queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ PageFileUsage**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileUsage")
</dt> </dl>

Riferimento all'istanza di che rappresenta le proprietà di un file di paging mentre il sistema Win32 è in uso.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ PageFileSetting**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileSetting")
</dt> </dl>

Riferimento all'istanza di che rappresenta le impostazioni iniziali di un file di paging all'avvio del sistema Win32.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ PageFileElementSetting** è derivata da [**CIM \_ ElementSetting**](cim-elementsetting.md).

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

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
