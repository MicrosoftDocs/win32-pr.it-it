---
description: La \_ classe CIM ElementSetting rappresenta l'associazione tra gli elementi di sistema gestiti e la classe di impostazione definita.
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: Classe CIM_ElementSetting (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304920"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a>Classe CIM_ElementSetting (provider WMI CIMWin32)

La classe **CIM \_ ElementSetting** rappresenta l'associazione tra gli elementi di sistema gestiti e la classe di impostazione definita.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ElementSetting** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ElementSetting** dispone di queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al ruolo dell'oggetto [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) dell'associazione **CIM \_ ElementSetting** . L'elemento del sistema gestito associato fornisce l'elemento che implementa l'impostazione dell'elemento.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ impostazione CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al ruolo dell'oggetto [**\_ impostazione CIM**](cim-setting.md) dell'associazione **CIM \_ ElementSetting** . L'impostazione associata fornisce l'impostazione che implementa l'impostazione dell'elemento.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per le classi derivate da **CIM \_ ElementSetting**, vedere [Win32 Classes](win32-provider.md).

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




