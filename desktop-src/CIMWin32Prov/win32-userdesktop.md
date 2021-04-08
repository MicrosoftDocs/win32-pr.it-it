---
description: La \_ classe WMI dell'associazione UserDesktop Win32 mette in correlazione un account utente e le impostazioni desktop specifiche.
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Classe Win32_UserDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserDesktop
- Win32_UserDesktop.Element
- Win32_UserDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 39b45ee7859fea9f1068123041a87309cf40c2d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877466"
---
# <a name="win32_userdesktop-class"></a>Win32 \_ UserDesktop (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ UserDesktop Win32** mette in correlazione un account utente e le impostazioni desktop specifiche.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserDesktop : CIM_ElementSetting
{
  Win32_UserAccount REF Element;
  Win32_Desktop     REF Setting;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ UserDesktop** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ UserDesktop** dispone di queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ AccountUtente**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ AccountUtente")
</dt> </dl>

Riferimento all'istanza di che rappresenta l'account utente il cui desktop può essere personalizzato tramite la proprietà **Settings** di questa classe.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ desktop Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("impostazione"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| desktop Win32 WMI \_ ")
</dt> </dl>

Riferimento all'istanza di che rappresenta le impostazioni desktop che consentono di personalizzare un desktop dell'account utente specifico.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ UserDesktop** è derivata da [**CIM \_ ElementSetting**](cim-elementsetting.md).

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

 

 
